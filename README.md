# Kraus Tech Solutions Website

> Custom AI/ML Architecture & Agent Development

A professional freelance business website built with Matrix-inspired black/lime green aesthetic. Designed to attract CTOs, founders, and decision-makers seeking custom ML solutions.

## 🎨 Design Specifications

**Color Scheme:**
- Black background (90%)
- Lime green (#00ff41) accents and headings (10%)
- White body text
- Matrix/terminal-inspired aesthetic

**Tone:**
- Professional but relatable
- Technical depth ("the guy knows his shit")
- Data-driven with metrics
- Business entity (not personal brand)

## 📁 File Structure

```
/
├── index.html                      # Homepage
├── about.html                      # About page
├── contact.html                    # Contact page with pricing
├── case-studies.html               # Case studies overview
├── case-dynamic-pricing.html       # Individual case study
├── blog.html                       # Blog landing page
├── styles.css                      # Main stylesheet
├── script.js                       # JavaScript interactions
└── README.md                       # This file
```

## 🚀 Quick Start - GitHub Pages Deployment

### Option 1: Deploy to GitHub Pages (Free)

1. **Create a GitHub repository:**
   ```bash
   # On GitHub, create a new repository named: yourusername.github.io
   ```

2. **Clone and add files:**
   ```bash
   git clone https://github.com/yourusername/yourusername.github.io.git
   cd yourusername.github.io
   
   # Copy all website files here
   git add .
   git commit -m "Initial Kraus Tech Solutions website"
   git push origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Source: Deploy from branch `main`
   - Folder: `/ (root)`
   - Save

4. **Access your site:**
   ```
   https://yourusername.github.io
   ```

### Option 2: Custom Domain Setup

1. **Purchase domain** (recommended: .com or .dev)
   - Namecheap, Google Domains, Cloudflare, etc.

2. **Configure DNS:**
   Add these records in your domain provider:
   ```
   Type    Name    Value
   A       @       185.199.108.153
   A       @       185.199.109.153
   A       @       185.199.110.153
   A       @       185.199.111.153
   CNAME   www     yourusername.github.io
   ```

3. **Add CNAME file to repository:**
   ```bash
   echo "kraustechsolutions.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

4. **Wait for DNS propagation** (15 minutes - 48 hours)

## ✏️ Customization Guide

### 1. Update Contact Information

**In all HTML files, replace:**
- `contact@kraustechsolutions.com` → Your actual email
- `https://linkedin.com/in/yourprofile` → Your LinkedIn
- `https://github.com/yourusername` → Your GitHub
- `https://calendly.com/yourname/discovery-call` → Your Calendly link

**Files to update:**
- `index.html` (footer)
- `contact.html` (contact methods, Calendly link)
- `about.html` (footer)
- `case-studies.html` (footer)
- `blog.html` (footer and social links)

### 2. Add More Case Study Pages

**Copy `case-dynamic-pricing.html` and modify:**
- Update title, description, meta tags
- Change Purpose, How, Results sections
- Update metrics and tech stack
- Save as `case-[project-name].html`

**Link from `case-studies.html`:**
```html
<a href="case-[project-name].html" class="case-card">
    <!-- Case details -->
</a>
```

### 3. Create Blog Posts

**Create new file:** `blog-[post-slug].html`

**Template structure:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Article Title | Kraus Tech Solutions</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Copy nav from blog.html -->
    
    <article style="max-width: 800px; margin: 0 auto; padding: 8rem 2rem 4rem;">
        <div class="blog-category">Category</div>
        <h1>Your Article Title</h1>
        <div class="blog-meta">
            <span>📅 Date</span>
            <span>⏱️ X min read</span>
        </div>
        
        <!-- Article content -->
        
    </article>
    
    <!-- Copy footer from blog.html -->
</body>
</html>
```

**Update `blog.html`:**
Replace "coming-soon" cards with links to actual articles.

### 4. Adjust Pricing

**In `contact.html`, modify:**
- Discovery call duration/pricing
- Extended consultation rate
- Project minimum amount

**In `index.html`, update:**
- "How We Work" section pricing mentions

### 5. Update Portfolio Metrics

**Replace demo metrics with your actual data:**
- Revenue impact numbers
- Accuracy percentages
- Time savings
- Tech stack details

## 🎯 SEO Optimization

### Add to Each Page

```html
<head>
    <!-- Primary Meta Tags -->
    <title>Page Title | Kraus Tech Solutions</title>
    <meta name="title" content="Page Title">
    <meta name="description" content="Page description">
    
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://kraustechsolutions.com/">
    <meta property="og:title" content="Page Title">
    <meta property="og:description" content="Page description">
    
    <!-- Twitter -->
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:title" content="Page Title">
    <meta property="twitter:description" content="Page description">
</head>
```

### Create `sitemap.xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url>
        <loc>https://kraustechsolutions.com/</loc>
        <priority>1.0</priority>
    </url>
    <url>
        <loc>https://kraustechsolutions.com/about.html</loc>
        <priority>0.8</priority>
    </url>
    <!-- Add all pages -->
</urlset>
```

## 📧 Email Integration

### Option 1: Formspree (Easiest)

1. Sign up at [formspree.io](https://formspree.io)
2. Get your form endpoint
3. In `contact.html`, update form:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

### Option 2: EmailJS

1. Sign up at [emailjs.com](https://www.emailjs.com/)
2. Get API keys
3. Add EmailJS script to `contact.html`
4. Configure email template

### Option 3: Backend Integration

Build custom backend with:
- Node.js + Nodemailer
- Python + Flask + SMTP
- Netlify Functions
- AWS Lambda

## 📅 Calendly Integration

1. Create [Calendly account](https://calendly.com)
2. Set up event types:
   - "Discovery Call" (15 min, free)
   - "Extended Consultation" (30 min, paid)
3. Get embed code
4. Replace in `contact.html`:
   ```html
   <!-- Replace button with Calendly embed -->
   <div class="calendly-inline-widget" 
        data-url="https://calendly.com/yourname/discovery-call"
        style="min-width:320px;height:630px;">
   </div>
   <script src="https://assets.calendly.com/assets/external/widget.js"></script>
   ```

## 🎨 Design Customization

### Change Colors

In `styles.css`, modify:
```css
:root {
    --color-lime: #00ff41;      /* Change accent color */
    --color-black: #000000;     /* Change background */
}
```

### Disable Matrix Rain Effect

In `script.js`, comment out:
```javascript
// document.addEventListener('DOMContentLoaded', createMatrixRain);
```

### Add Dark/Light Mode Toggle

```javascript
// Add to script.js
function toggleTheme() {
    document.body.classList.toggle('light-mode');
    // Save preference
    localStorage.setItem('theme', 
        document.body.classList.contains('light-mode') ? 'light' : 'dark'
    );
}
```

## 📊 Analytics Setup

### Google Analytics

1. Create GA4 property
2. Add to all pages before `</head>`:
```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'G-XXXXXXXXXX');
</script>
```

### Plausible Analytics (Privacy-Friendly Alternative)

```html
<script defer data-domain="kraustechsolutions.com" 
    src="https://plausible.io/js/script.js">
</script>
```

## 🔒 Security Best Practices

1. **Never commit sensitive data**
   - API keys
   - Email credentials
   - Private information

2. **Use environment variables** for:
   - Form backend URLs
   - API endpoints
   - Analytics IDs

3. **Add `.gitignore`:**
   ```
   .env
   .DS_Store
   node_modules/
   ```

## 📱 Social Media Integration

### LinkedIn Posts
- Share blog articles
- Announce case studies
- Post project updates

### Instagram
- Visual case study highlights
- ML concept explanations
- Behind-the-scenes development

### Cross-Posting
Use tools like:
- Buffer
- Hootsuite
- Later

## ⚡ Performance Optimization

1. **Minify CSS/JS:**
   ```bash
   # Use online tools or:
   npm install -g clean-css-cli uglify-js
   cleancss -o styles.min.css styles.css
   uglifyjs script.js -o script.min.js
   ```

2. **Optimize images:**
   - Use WebP format
   - Compress with TinyPNG
   - Add lazy loading

3. **Enable caching:**
   Add `_headers` file (for Netlify) or configure in GitHub Pages

## 🐛 Troubleshooting

**Site not loading?**
- Check GitHub Pages is enabled
- Verify `index.html` is in root directory
- Clear browser cache

**Custom domain not working?**
- Wait 24-48 hours for DNS propagation
- Verify DNS records are correct
- Check CNAME file exists

**Forms not submitting?**
- Integrate form backend (Formspree/EmailJS)
- Check console for JavaScript errors

**Mobile layout issues?**
- Test on multiple devices
- Use Chrome DevTools mobile view
- Check viewport meta tag

## 📝 Content Strategy

### Blog Post Schedule
- **Week 1-2:** "Building a Deep Learning Framework from Scratch"
- **Week 3-4:** "RAG vs Fine-Tuning: When to Use Each"
- **Week 5-6:** "The Real Cost of Building vs Buying ML"
- **Week 7-8:** "From Jupyter Notebook to Production"

### Case Study Updates
- Add full write-ups for remaining 8 projects
- Include technical details + business impact
- Update metrics with real client data (when available)

### LinkedIn Strategy
- Post blog articles immediately
- Share technical insights 2-3x/week
- Engage with ML community

## 🎯 Next Steps

### Week 1:
- [ ] Deploy to GitHub Pages
- [ ] Purchase custom domain
- [ ] Set up email integration
- [ ] Configure Calendly
- [ ] Add Google Analytics

### Week 2:
- [ ] Write first blog post
- [ ] Complete remaining case studies
- [ ] Set up social media cross-posting
- [ ] Test all forms and links
- [ ] Get feedback from 3-5 people

### Ongoing:
- [ ] Publish bi-weekly blog posts
- [ ] Update case studies with real client work
- [ ] Monitor analytics and iterate
- [ ] Build email list
- [ ] Engage on LinkedIn/Instagram

## 💡 Tips for Success

1. **Consistency:** Stick to bi-weekly blog schedule
2. **Authenticity:** Write in your own voice, not corporate speak
3. **Value First:** Provide actual insights, not just promotion
4. **Network:** Engage with ML community on LinkedIn
5. **Iterate:** Use analytics to improve content
6. **Patience:** Building authority takes 3-6 months

## 📞 Support

For questions about this website:
- Email: contact@kraustechsolutions.com
- LinkedIn: [Your Profile]
- GitHub: [Your Repo]

---

**Built with ❤️ using HTML, CSS, and JavaScript**
**No frameworks. No dependencies. Just clean, fast code.**
