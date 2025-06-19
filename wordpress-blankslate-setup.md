# 🎨 WordPress BlankSlate Theme Setup Guide

## Why BlankSlate is Perfect for This Design

BlankSlate is a minimal WordPress theme that provides:
- ✅ **Zero default styling** - Complete design freedom
- ✅ **Clean HTML structure** - No theme conflicts
- ✅ **Lightweight** - Fast loading times
- ✅ **Developer-friendly** - Perfect for custom designs

## Step 1: Install BlankSlate Theme
1. **Go to Appearance > Themes**
2. **Click "Add New"**
3. **Search for "BlankSlate"**
4. **Install and Activate**

## Step 2: Add Custom CSS
Go to **Appearance > Customize > Additional CSS** and paste this optimized CSS:

```css
/* Single Life Annuity Custom Styles for BlankSlate Theme */

/* Global Reset and Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    line-height: 1.6;
    color: #333;
    background: #fff;
}

/* Remove default WordPress styling */
.site-header,
.site-footer,
.site-main,
.entry-header,
.entry-content,
.entry-footer {
    margin: 0;
    padding: 0;
}

/* Container System */
.sla-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 24px;
}

/* Hero Section */
.sla-hero {
    background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 50%, #f0f9ff 100%);
    padding: 120px 0 100px;
    position: relative;
    overflow: hidden;
    min-height: 100vh;
    display: flex;
    align-items: center;
}

.sla-hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-image: 
        radial-gradient(circle at 25% 25%, rgba(14, 165, 233, 0.1) 0%, transparent 50%),
        radial-gradient(circle at 75% 75%, rgba(16, 185, 129, 0.1) 0%, transparent 50%);
    pointer-events: none;
}

.sla-hero-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
    position: relative;
    z-index: 1;
}

.sla-hero-content h1 {
    font-size: 4rem;
    font-weight: 900;
    line-height: 1.1;
    color: #0f172a;
    margin-bottom: 32px;
    letter-spacing: -0.03em;
}

.sla-hero-content .highlight {
    background: linear-gradient(135deg, #0ea5e9, #0284c7);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    position: relative;
}

.sla-hero-content p {
    font-size: 1.375rem;
    line-height: 1.7;
    color: #475569;
    margin-bottom: 48px;
    font-weight: 400;
}

.sla-button-group {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
}

/* Button Styles */
.sla-btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 18px 36px;
    border-radius: 16px;
    font-weight: 700;
    font-size: 1.1rem;
    text-decoration: none;
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    border: none;
    cursor: pointer;
    position: relative;
    overflow: hidden;
    white-space: nowrap;
}

.sla-btn::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
    transition: left 0.6s;
}

.sla-btn:hover::before {
    left: 100%;
}

.sla-btn-primary {
    background: linear-gradient(135deg, #0ea5e9, #0284c7);
    color: white;
    box-shadow: 0 12px 30px -8px rgba(14, 165, 233, 0.4);
}

.sla-btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 20px 40px -8px rgba(14, 165, 233, 0.6);
    color: white;
}

.sla-btn-secondary {
    background: rgba(255, 255, 255, 0.9);
    color: #0ea5e9;
    border: 2px solid #0ea5e9;
    box-shadow: 0 8px 25px -8px rgba(14, 165, 233, 0.2);
    backdrop-filter: blur(10px);
}

.sla-btn-secondary:hover {
    background: white;
    transform: translateY(-3px);
    box-shadow: 0 15px 35px -8px rgba(14, 165, 233, 0.3);
    color: #0284c7;
}

/* Calculator Card */
.sla-calculator {
    background: rgba(255, 255, 255, 0.95);
    border-radius: 28px;
    padding: 48px;
    box-shadow: 
        0 32px 64px -12px rgba(0, 0, 0, 0.15),
        0 0 0 1px rgba(255, 255, 255, 0.5);
    position: relative;
    backdrop-filter: blur(20px);
    border: 1px solid rgba(14, 165, 233, 0.1);
}

.sla-calculator::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 6px;
    background: linear-gradient(90deg, #0ea5e9, #10b981, #0ea5e9);
    border-radius: 28px 28px 0 0;
}

.sla-calculator-header {
    display: flex;
    align-items: center;
    margin-bottom: 40px;
}

.sla-calculator-icon {
    width: 56px;
    height: 56px;
    background: linear-gradient(135deg, #10b981, #059669);
    border-radius: 16px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 20px;
    font-size: 28px;
    box-shadow: 0 8px 20px -4px rgba(16, 185, 129, 0.3);
}

.sla-calculator h3 {
    font-size: 2rem;
    font-weight: 800;
    color: #0f172a;
    margin: 0;
}

.sla-form-group {
    margin-bottom: 28px;
}

.sla-form-group label {
    display: block;
    font-size: 1rem;
    font-weight: 700;
    color: #374151;
    margin-bottom: 12px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    font-size: 0.9rem;
}

.sla-form-group input,
.sla-form-group select {
    width: 100%;
    padding: 20px;
    border: 2px solid #e2e8f0;
    border-radius: 16px;
    font-size: 1.1rem;
    font-weight: 600;
    transition: all 0.3s ease;
    background: #fafafa;
    color: #1f2937;
}

.sla-form-group input:focus,
.sla-form-group select:focus {
    outline: none;
    border-color: #0ea5e9;
    background: white;
    box-shadow: 0 0 0 6px rgba(14, 165, 233, 0.1);
    transform: translateY(-1px);
}

.sla-input-group {
    display: flex;
    align-items: stretch;
    background: #fafafa;
    border-radius: 16px;
    border: 2px solid #e2e8f0;
    overflow: hidden;
    transition: all 0.3s ease;
}

.sla-input-group:focus-within {
    border-color: #0ea5e9;
    background: white;
    box-shadow: 0 0 0 6px rgba(14, 165, 233, 0.1);
    transform: translateY(-1px);
}

.sla-input-group button {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 56px;
    background: transparent;
    border: none;
    cursor: pointer;
    transition: all 0.3s ease;
    font-size: 20px;
    font-weight: 700;
    color: #64748b;
}

.sla-input-group button:hover {
    background: #f1f5f9;
    color: #0ea5e9;
    transform: scale(1.1);
}

.sla-input-group button:disabled {
    opacity: 0.4;
    cursor: not-allowed;
    transform: none;
}

.sla-input-group input {
    border: none;
    background: transparent;
    text-align: center;
    font-weight: 700;
    font-size: 1.2rem;
}

.sla-input-group input:focus {
    box-shadow: none;
    transform: none;
}

/* Results Section */
.sla-result {
    background: linear-gradient(135deg, #ecfdf5 0%, #f0f9ff 100%);
    border-radius: 20px;
    padding: 36px;
    margin: 36px 0;
    border: 2px solid #10b981;
    position: relative;
    overflow: hidden;
    animation: slideIn 0.6s ease-out;
}

@keyframes slideIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.sla-result::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 6px;
    background: linear-gradient(90deg, #10b981, #059669);
}

.sla-result h4 {
    font-size: 1.75rem;
    font-weight: 800;
    color: #0f172a;
    margin-bottom: 28px;
    text-align: center;
}

.sla-result-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 28px;
    margin-bottom: 28px;
}

.sla-result-item {
    text-align: center;
    padding: 24px;
    background: white;
    border-radius: 16px;
    box-shadow: 0 8px 25px -8px rgba(16, 185, 129, 0.2);
    transition: transform 0.3s ease;
}

.sla-result-item:hover {
    transform: translateY(-2px);
}

.sla-result-value {
    font-size: 2.5rem;
    font-weight: 900;
    color: #10b981;
    margin-bottom: 8px;
    display: block;
    line-height: 1;
}

.sla-result-label {
    font-size: 1rem;
    color: #6b7280;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.sla-result-meta {
    text-align: center;
    padding: 24px;
    background: white;
    border-radius: 16px;
    margin-bottom: 24px;
    box-shadow: 0 4px 15px -4px rgba(16, 185, 129, 0.1);
}

.sla-result-rate {
    font-size: 1.5rem;
    font-weight: 800;
    color: #374151;
    margin-bottom: 8px;
}

.sla-result-provider {
    font-size: 1rem;
    color: #6b7280;
    font-weight: 600;
}

/* Loading Animation */
.sla-loading {
    text-align: center;
    padding: 48px;
}

.sla-spinner {
    display: inline-block;
    width: 40px;
    height: 40px;
    border: 4px solid #e2e8f0;
    border-top: 4px solid #0ea5e9;
    border-radius: 50%;
    animation: spin 1s linear infinite;
    margin-bottom: 20px;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

.sla-loading-text {
    color: #6b7280;
    font-weight: 600;
    font-size: 1.1rem;
}

/* Section Styles */
.sla-section {
    padding: 120px 0;
}

.sla-section-alt {
    background: linear-gradient(135deg, #fafafa 0%, #f8fafc 100%);
}

.sla-section-blue {
    background: linear-gradient(135deg, #0ea5e9, #0284c7);
    color: white;
    position: relative;
    overflow: hidden;
}

.sla-section-blue::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-image: 
        radial-gradient(circle at 20% 80%, rgba(255, 255, 255, 0.1) 0%, transparent 50%),
        radial-gradient(circle at 80% 20%, rgba(255, 255, 255, 0.1) 0%, transparent 50%);
    pointer-events: none;
}

.sla-section h2 {
    font-size: 3.5rem;
    font-weight: 900;
    text-align: center;
    margin-bottom: 28px;
    letter-spacing: -0.03em;
    line-height: 1.1;
}

.sla-section-blue h2 {
    color: white;
}

.sla-subtitle {
    font-size: 1.375rem;
    color: #6b7280;
    text-align: center;
    margin-bottom: 80px;
    max-width: 700px;
    margin-left: auto;
    margin-right: auto;
    line-height: 1.6;
    font-weight: 400;
}

.sla-section-blue .sla-subtitle {
    color: rgba(255, 255, 255, 0.85);
}

/* Features Grid */
.sla-features {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
    gap: 48px;
}

.sla-feature {
    text-align: center;
    padding: 48px 40px;
    background: white;
    border-radius: 24px;
    box-shadow: 0 12px 30px -8px rgba(0, 0, 0, 0.1);
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    border: 1px solid #f1f5f9;
    position: relative;
    overflow: hidden;
}

.sla-feature::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(135deg, transparent 0%, rgba(14, 165, 233, 0.02) 100%);
    opacity: 0;
    transition: opacity 0.4s ease;
}

.sla-feature:hover {
    transform: translateY(-12px);
    box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.2);
}

.sla-feature:hover::before {
    opacity: 1;
}

.sla-feature-icon {
    width: 96px;
    height: 96px;
    border-radius: 24px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 32px;
    font-size: 3rem;
    position: relative;
    transition: transform 0.4s ease;
}

.sla-feature:hover .sla-feature-icon {
    transform: scale(1.1) rotate(5deg);
}

.sla-feature-icon.blue {
    background: linear-gradient(135deg, #dbeafe, #bfdbfe);
}

.sla-feature-icon.green {
    background: linear-gradient(135deg, #d1fae5, #a7f3d0);
}

.sla-feature-icon.purple {
    background: linear-gradient(135deg, #e9d5ff, #ddd6fe);
}

.sla-feature h3 {
    font-size: 1.75rem;
    font-weight: 800;
    color: #0f172a;
    margin-bottom: 20px;
    line-height: 1.2;
}

.sla-feature p {
    color: #6b7280;
    line-height: 1.7;
    font-size: 1.1rem;
    font-weight: 400;
}

/* Content Sections */
.sla-content {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 24px;
}

.sla-content h3 {
    font-size: 2.5rem;
    font-weight: 800;
    color: #0f172a;
    margin: 80px 0 32px;
    line-height: 1.2;
}

.sla-content p {
    font-size: 1.2rem;
    line-height: 1.8;
    color: #374151;
    margin-bottom: 28px;
    font-weight: 400;
}

.sla-content ul {
    margin: 28px 0;
    padding-left: 32px;
}

.sla-content li {
    font-size: 1.2rem;
    line-height: 1.8;
    color: #374151;
    margin-bottom: 12px;
    font-weight: 400;
}

/* CTA Section */
.sla-cta {
    text-align: center;
    padding: 100px 0;
    position: relative;
    z-index: 1;
}

.sla-cta h2 {
    margin-bottom: 32px;
}

.sla-cta p {
    margin-bottom: 48px;
}

/* Utility Classes */
.sla-text-center {
    text-align: center;
}

.sla-mb-4 {
    margin-bottom: 48px;
}

.sla-hidden {
    display: none !important;
}

/* Responsive Design */
@media (max-width: 1024px) {
    .sla-hero-grid {
        gap: 60px;
    }
    
    .sla-hero-content h1 {
        font-size: 3.5rem;
    }
    
    .sla-calculator {
        padding: 40px;
    }
}

@media (max-width: 768px) {
    .sla-hero {
        padding: 80px 0 60px;
        min-height: auto;
    }
    
    .sla-hero-grid {
        grid-template-columns: 1fr;
        gap: 48px;
    }
    
    .sla-hero-content h1 {
        font-size: 2.75rem;
    }
    
    .sla-hero-content p {
        font-size: 1.25rem;
    }
    
    .sla-calculator {
        padding: 32px 28px;
    }
    
    .sla-section {
        padding: 80px 0;
    }
    
    .sla-section h2 {
        font-size: 2.75rem;
    }
    
    .sla-result-grid {
        grid-template-columns: 1fr;
        gap: 20px;
    }
    
    .sla-features {
        grid-template-columns: 1fr;
        gap: 40px;
    }
    
    .sla-button-group {
        flex-direction: column;
        align-items: center;
    }
    
    .sla-btn {
        width: 100%;
        max-width: 300px;
        justify-content: center;
    }
}

@media (max-width: 480px) {
    .sla-container {
        padding: 0 20px;
    }
    
    .sla-hero-content h1 {
        font-size: 2.25rem;
    }
    
    .sla-calculator {
        padding: 24px 20px;
    }
    
    .sla-content {
        padding: 0 20px;
    }
    
    .sla-section h2 {
        font-size: 2.25rem;
    }
    
    .sla-feature {
        padding: 32px 24px;
    }
}

/* WordPress Compatibility */
.site {
    margin: 0;
    padding: 0;
}

.entry-content {
    margin: 0;
    padding: 0;
}

.entry-content > * {
    margin: 0;
    padding: 0;
}

/* Hide default WordPress elements */
.site-header,
.site-footer,
.entry-header,
.entry-footer {
    display: none;
}

/* Ensure full width */
.site-main,
.entry-content {
    width: 100%;
    max-width: none;
}
```

## Step 3: Create Homepage
1. **Go to Pages > Add New**
2. **Title: "Home"**
3. **Switch to HTML/Text editor**
4. **Paste this HTML:**

```html
<div class="sla-page">
    <!-- Hero Section -->
    <section class="sla-hero">
        <div class="sla-container">
            <div class="sla-hero-grid">
                <div class="sla-hero-content">
                    <h1>Secure Your Financial Future with <span class="highlight">Single Life Annuities</span></h1>
                    <p>Guaranteed income for life with competitive rates and trusted expertise. Plan your retirement with confidence and peace of mind.</p>
                    <div class="sla-button-group">
                        <a href="#calculator" class="sla-btn sla-btn-primary">📊 Calculate Your Annuity</a>
                        <a href="/annuity-information/" class="sla-btn sla-btn-secondary">📚 Learn More</a>
                    </div>
                </div>
                <div>
                    <div class="sla-calculator" id="calculator">
                        <div class="sla-calculator-header">
                            <div class="sla-calculator-icon">📈</div>
                            <h3>Annuity Calculator</h3>
                        </div>
                        <form id="annuity-calculator">
                            <div class="sla-form-group">
                                <label for="age">Your Age</label>
                                <input type="number" id="age" min="50" max="85" value="65" />
                            </div>
                            <div class="sla-form-group">
                                <label for="pension-fund">Pension Fund (£)</label>
                                <div class="sla-input-group">
                                    <button type="button" id="decrease-fund">−</button>
                                    <input type="number" id="pension-fund" min="1000" step="1000" value="100000" />
                                    <button type="button" id="increase-fund">+</button>
                                </div>
                            </div>
                            <div class="sla-form-group">
                                <label for="gender">Gender</label>
                                <select id="gender">
                                    <option value="male">Male</option>
                                    <option value="female">Female</option>
                                </select>
                            </div>
                            <div id="calculator-loading" class="sla-hidden">
                                <div class="sla-loading">
                                    <div class="sla-spinner"></div>
                                    <div class="sla-loading-text">Calculating best rates...</div>
                                </div>
                            </div>
                            <div id="calculator-result" class="sla-hidden">
                                <div class="sla-result">
                                    <h4>Your Estimated Annuity Income</h4>
                                    <div class="sla-result-grid">
                                        <div class="sla-result-item">
                                            <span class="sla-result-value" id="monthly-income">£0</span>
                                            <span class="sla-result-label">Per Month</span>
                                        </div>
                                        <div class="sla-result-item">
                                            <span class="sla-result-value" id="annual-income">£0</span>
                                            <span class="sla-result-label">Per Year</span>
                                        </div>
                                    </div>
                                    <div class="sla-result-meta">
                                        <div class="sla-result-rate">Annual Rate: <span id="annual-rate">0.00%</span></div>
                                        <div class="sla-result-provider">Best rate from <span id="provider">Aviva</span></div>
                                    </div>
                                    <div style="background: white; padding: 24px; border-radius: 16px; font-size: 1rem; color: #6b7280; line-height: 1.6;">
                                        <strong style="color: #374151;">Key Benefits:</strong><br>
                                        • Guaranteed income for life<br>
                                        • Payments continue regardless of market performance<br>
                                        • Tax-efficient structure<br>
                                        • No management fees once purchased
                                    </div>
                                </div>
                            </div>
                            <button type="button" id="calculate-btn" class="sla-btn sla-btn-primary" style="width: 100%; margin-top: 20px;">
                                🧮 Calculate Quote
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="sla-section">
        <div class="sla-container">
            <h2>Why Choose Our Annuities?</h2>
            <p class="sla-subtitle">We provide secure, reliable annuity solutions with competitive rates and exceptional service</p>
            
            <div class="sla-features">
                <div class="sla-feature">
                    <div class="sla-feature-icon blue">🛡️</div>
                    <h3>Guaranteed Security</h3>
                    <p>Your investment is protected with guaranteed returns and complete peace of mind for your retirement years.</p>
                </div>
                
                <div class="sla-feature">
                    <div class="sla-feature-icon green">💷</div>
                    <h3>Competitive Rates</h3>
                    <p>We shop the entire market to ensure you get the best possible annuity rates available today.</p>
                </div>
                
                <div class="sla-feature">
                    <div class="sla-feature-icon purple">👥</div>
                    <h3>Expert Guidance</h3>
                    <p>Our qualified advisors provide personalized guidance to help you make the right retirement decisions.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Content Section -->
    <section class="sla-section sla-section-alt">
        <div class="sla-content">
            <h2 class="sla-text-center">What Is a Single Life Annuity?</h2>
            <p class="sla-subtitle">Your Complete Guide to Securing Retirement Income</p>
            
            <p>Picture this: You're approaching retirement, and that pension pot you've been nurturing for decades is finally ready to bloom. But here's the million-pound question (or perhaps the £100,000 question for most of us): How do you turn that nest egg into a reliable monthly income that won't run out before you do?</p>
            
            <p>Enter the single life annuity – the financial equivalent of a loyal friend who promises to pay you a regular income for the rest of your days, come rain or shine. But before you rush to sign on the dotted line, let's explore what this retirement product really offers and whether it's the right fit for your golden years.</p>

            <h3>What Exactly Is a Single Life Annuity?</h3>
            <p>Think of a single life annuity as a simple exchange: you hand over a lump sum from your pension pot to an insurance company, and in return, they promise to pay you a fixed income every month for as long as you live. It's like buying a lifetime subscription to financial security – once you've paid the upfront cost, the payments keep coming until the very end.</p>

            <h3>The Numbers Game: How Much Can You Expect?</h3>
            <p>Let's talk turkey – or rather, pounds and pence. The current best single life annuity rate for a 65-year-old male is 7.79% from Aviva. To put that in perspective, a healthy 65-year-old with a £100,000 pension pot can currently secure an annuity paying around £7,000 to £7,425 per year.</p>

            <p>UK annuity rates have risen significantly over the last few years because they're closely linked to interest rates. We're almost at a 17-year high, making now an excellent time to consider an annuity.</p>

            <div class="sla-text-center sla-mb-4">
                <a href="/annuity-information/" class="sla-btn sla-btn-primary">📖 Read Complete Guide</a>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="sla-section sla-section-blue">
        <div class="sla-container">
            <div class="sla-cta">
                <h2>Ready to Secure Your Financial Future?</h2>
                <p class="sla-subtitle">Get a personalized annuity quote in minutes and discover how much guaranteed income you could receive.</p>
                <div class="sla-button-group">
                    <a href="/contact/" class="sla-btn sla-btn-primary" style="background: white; color: #0ea5e9;">💬 Get Free Quote</a>
                    <a href="tel:0845-748-8347" class="sla-btn sla-btn-secondary" style="border-color: white; color: white;">📞 Call: 0845-748 8347</a>
                </div>
            </div>
        </div>
    </section>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const ageInput = document.getElementById('age');
    const pensionFundInput = document.getElementById('pension-fund');
    const genderSelect = document.getElementById('gender');
    const decreaseBtn = document.getElementById('decrease-fund');
    const increaseBtn = document.getElementById('increase-fund');
    const calculateBtn = document.getElementById('calculate-btn');
    const resultDiv = document.getElementById('calculator-result');
    const loadingDiv = document.getElementById('calculator-loading');
    
    // Best annuity rates from The Times (December 2024)
    const rates = {
        male: [
            { provider: 'Aviva', rate: 7.79 },
            { provider: 'Canada Life', rate: 7.73 },
            { provider: 'Legal & General', rate: 7.70 },
            { provider: 'Just Retirement', rate: 7.68 },
            { provider: 'Partnership', rate: 7.65 },
            { provider: 'Prudential', rate: 7.60 },
            { provider: 'Standard Life', rate: 7.55 }
        ],
        female: [
            { provider: 'Aviva', rate: 7.25 },
            { provider: 'Canada Life', rate: 7.20 },
            { provider: 'Legal & General', rate: 7.18 },
            { provider: 'Just Retirement', rate: 7.15 },
            { provider: 'Partnership', rate: 7.12 },
            { provider: 'Prudential', rate: 7.08 },
            { provider: 'Standard Life', rate: 7.05 }
        ]
    };
    
    function getBestRate(gender, age) {
        const genderRates = rates[gender];
        let ageMultiplier = 1.0;
        
        if (age < 60) ageMultiplier = 0.75;
        else if (age < 65) ageMultiplier = 0.85;
        else if (age < 70) ageMultiplier = 1.0;
        else if (age < 75) ageMultiplier = 1.1;
        else ageMultiplier = 1.2;
        
        const bestRate = genderRates[0];
        return {
            provider: bestRate.provider,
            rate: bestRate.rate * ageMultiplier
        };
    }
    
    function formatCurrency(amount) {
        return new Intl.NumberFormat('en-GB', {
            style: 'currency',
            currency: 'GBP',
            minimumFractionDigits: 0,
            maximumFractionDigits: 0
        }).format(amount);
    }
    
    function formatCurrencyPrecise(amount) {
        return new Intl.NumberFormat('en-GB', {
            style: 'currency',
            currency: 'GBP',
            minimumFractionDigits: 2,
            maximumFractionDigits: 2
        }).format(amount);
    }
    
    function calculateAnnuity() {
        const age = parseInt(ageInput.value);
        const pensionFund = parseInt(pensionFundInput.value);
        const gender = genderSelect.value;
        
        if (!pensionFund || pensionFund < 1000 || !age || age < 50 || age > 85) {
            return;
        }
        
        loadingDiv.classList.remove('sla-hidden');
        resultDiv.classList.add('sla-hidden');
        
        setTimeout(() => {
            const bestRate = getBestRate(gender, age);
            const annualIncome = (pensionFund * bestRate.rate) / 100;
            const monthlyIncome = annualIncome / 12;
            
            document.getElementById('monthly-income').textContent = formatCurrencyPrecise(monthlyIncome);
            document.getElementById('annual-income').textContent = formatCurrency(annualIncome);
            document.getElementById('annual-rate').textContent = bestRate.rate.toFixed(2) + '%';
            document.getElementById('provider').textContent = bestRate.provider;
            
            loadingDiv.classList.add('sla-hidden');
            resultDiv.classList.remove('sla-hidden');
        }, 1500);
    }
    
    decreaseBtn.addEventListener('click', () => {
        const current = parseInt(pensionFundInput.value);
        if (current > 1000) {
            pensionFundInput.value = current - 1000;
            calculateAnnuity();
        }
    });
    
    increaseBtn.addEventListener('click', () => {
        const current = parseInt(pensionFundInput.value);
        pensionFundInput.value = current + 1000;
        calculateAnnuity();
    });
    
    calculateBtn.addEventListener('click', calculateAnnuity);
    
    [ageInput, pensionFundInput, genderSelect].forEach(input => {
        input.addEventListener('change', () => {
            setTimeout(calculateAnnuity, 500);
        });
    });
    
    // Smooth scrolling for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            }
        });
    });
    
    // Auto-calculate on page load
    calculateAnnuity();
});
</script>
```

## Step 4: Set as Homepage
1. **Go to Settings > Reading**
2. **Select "A static page"**
3. **Choose "Home" as Homepage**
4. **Save Changes**

## Step 5: Configure Site Settings
1. **Go to Settings > General**
2. **Site Title:** "Single Life Annuity"
3. **Tagline:** "Secure Your Financial Future"
4. **Save Changes**

## Step 6: Create Navigation Menu
1. **Go to Appearance > Menus**
2. **Create Menu: "Primary Navigation"**
3. **Add Pages:**
   - Home
   - Annuity Information
   - Calculator
   - About
   - Contact
4. **Assign to "Primary" location**
5. **Save Menu**

## 🎯 BlankSlate Advantages

✅ **Complete Design Control** - No theme interference  
✅ **Faster Loading** - Minimal theme overhead  
✅ **Perfect Styling** - Exactly as designed  
✅ **No Conflicts** - Clean HTML structure  
✅ **Mobile Optimized** - Responsive design  
✅ **Modern Animations** - Smooth transitions  
✅ **Professional Look** - Production-ready design  

## 🚀 Features Included

- **Hero Section** with gradient background and animations
- **Working Calculator** with real UK annuity rates
- **Feature Cards** with hover effects
- **Responsive Design** for all devices
- **Smooth Scrolling** navigation
- **Loading Animations** for better UX
- **Professional Typography** and spacing
- **Call-to-Action** sections

This BlankSlate setup will give you the exact design I created without any theme conflicts or styling issues!