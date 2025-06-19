# Custom Domain Setup Instructions

## The Issue
Your custom domain `singlelifeannuity.co.uk` is not pointing to your Netlify deployment. The Netlify site is working fine at `singlelifeannuity.netlify.app`, but the custom domain shows a different website.

## Solution Steps

### 1. Configure Domain in Netlify
1. Go to your Netlify dashboard
2. Select your site (singlelifeannuity)
3. Go to **Site settings** > **Domain management**
4. Click **Add custom domain**
5. Enter: `singlelifeannuity.co.uk`
6. Also add: `www.singlelifeannuity.co.uk`

### 2. Update DNS Records
You need to update your DNS settings where your domain is registered:

**For Apex Domain (singlelifeannuity.co.uk):**
- Type: `A`
- Name: `@` or leave blank
- Value: `75.2.60.5` (Netlify's load balancer IP)

**For WWW Subdomain:**
- Type: `CNAME`
- Name: `www`
- Value: `singlelifeannuity.netlify.app`

### 3. Alternative: Use Netlify DNS
If you want to use Netlify's DNS:
1. In Netlify, go to **Domains** > **DNS**
2. Add your domain
3. Update your domain registrar to use Netlify's nameservers

### 4. SSL Certificate
Once DNS propagates (can take up to 48 hours):
1. Netlify will automatically provision an SSL certificate
2. Enable **Force HTTPS** in domain settings

## Current Status
- ✅ Netlify site working: https://singlelifeannuity.netlify.app
- ❌ Custom domain not configured: https://singlelifeannuity.co.uk

## Next Steps
1. Configure the custom domain in Netlify
2. Update DNS records with your domain registrar
3. Wait for DNS propagation (up to 48 hours)
4. Test the custom domain

The updated site with all the legal compliance changes and SEO improvements is ready and deployed to Netlify - it just needs the custom domain properly connected.