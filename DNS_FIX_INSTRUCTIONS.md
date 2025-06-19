# DNS Configuration Fix

## The Issue
Your main domain DNS is properly configured in Netlify, but the blog subdomain A record is causing conflicts.

## Current DNS Records (from screenshots):
- `singlelifeannuity.co.uk` → `singlelifeannuity.netlify.app` ✅
- `www.singlelifeannuity.co.uk` → `singlelifeannuity.netlify.app` ✅  
- `blog.singlelifeannuity.co.uk` → `104.168.134.21` ❌ (Causing conflict)

## Immediate Fix Steps:

### 1. Check DNS Propagation
The issue might be DNS propagation delay. Check if your domain is resolving correctly:
- Visit: https://dnschecker.org/
- Enter: `singlelifeannuity.co.uk`
- Check if it's pointing to Netlify's servers globally

### 2. Clear DNS Cache
The blog A record addition may have caused DNS cache issues:

**On Windows:**
```cmd
ipconfig /flushdns
```

**On Mac:**
```bash
sudo dscacheutil -flushcache
```

**On Linux:**
```bash
sudo systemctl restart systemd-resolved
```

### 3. Verify Netlify Configuration
In your Netlify dashboard:
1. Go to Site Settings → Domain Management
2. Ensure `singlelifeannuity.co.uk` is set as primary domain
3. Check that SSL certificate is active
4. Verify "Force HTTPS" is enabled

### 4. Temporary Workaround
If the issue persists, temporarily remove the blog A record:
1. Delete the `blog.singlelifeannuity.co.uk` A record
2. Wait 1-2 hours for DNS propagation
3. Test if main domain works
4. Re-add blog record if needed

### 5. Alternative Blog Setup
Instead of an A record, consider:
- CNAME record: `blog.singlelifeannuity.co.uk` → `your-blog-host.com`
- Or use a subdirectory: `singlelifeannuity.co.uk/blog`

## Expected Timeline
- DNS changes: 15 minutes - 2 hours
- Full global propagation: Up to 48 hours
- Cache clearing: Immediate

## Test Commands
```bash
# Check current DNS resolution
nslookup singlelifeannuity.co.uk

# Check with different DNS servers
nslookup singlelifeannuity.co.uk 8.8.8.8
nslookup singlelifeannuity.co.uk 1.1.1.1
```

## If Still Not Working
1. Contact your domain registrar to verify DNS settings
2. Check if there are any domain forwarding rules
3. Ensure domain isn't locked or suspended
4. Verify domain hasn't expired

The Netlify deployment is working perfectly - this is purely a DNS routing issue that should resolve once the blog record conflict is addressed.