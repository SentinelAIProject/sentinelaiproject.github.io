# Sentinel AI Project Website

Custom automation solutions for New Zealand businesses.

## Quick Start - Deploy to GitHub Pages

### Step 1: Create GitHub Account
1. Go to https://github.com
2. Sign up (if you don't have an account)
3. Verify your email

### Step 2: Create Repository
1. Click the "+" icon in top right → "New repository"
2. Repository name: `sentinelaiproject.github.io` (exactly this)
3. Description: "Sentinel AI Project - Business Automation Solutions"
4. Make it Public
5. Click "Create repository"

### Step 3: Upload Your Files
1. On your repository page, click "uploading an existing file"
2. Drag and drop ALL files from this folder:
   - index.html
   - services.html
   - how-it-works.html
   - contact.html
   - images/ folder (with all images)
   - assets/ folder (with css subfolder)
3. Scroll down, click "Commit changes"

### Step 4: Enable GitHub Pages
1. Go to repository "Settings"
2. Scroll to "Pages" in left sidebar
3. Under "Source", select "main" branch
4. Click "Save"
5. Wait 1-2 minutes

### Step 5: Visit Your Site
Your site will be live at: `https://sentinelaiproject.github.io`

## Important: Set Up Contact Forms

The contact forms currently use placeholder Formspree URLs. To make them work:

1. Go to https://formspree.io
2. Sign up for free account
3. Create a new form
4. Copy your form endpoint URL
5. Edit these files and replace `YOUR_FORM_ID`:
   - index.html (line ~200, the Coming Soon email signup)
   - contact.html (line ~48, the main contact form)

Replace:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

With:
```html
<form action="https://formspree.io/f/YOUR_ACTUAL_FORM_ID" method="POST">
```

## Customization

### Change Colors
Edit `assets/css/main.css`, lines 5-10:
```css
:root {
    --primary-color: #2196F3;  /* Main blue */
    --secondary-color: #1976D2; /* Darker blue */
    --dark: #212121;            /* Dark gray */
    --light: #f5f5f5;           /* Light gray */
    --text: #333;               /* Text color */
}
```

### Add Your City/Location
Search for "Based in New Zealand" and replace with your specific city.

### Update Copyright Year
Search for "2024" and update to current year.

## File Structure

```
sentinel-ai-project/
├── index.html              # Homepage
├── services.html           # Services page
├── how-it-works.html       # Process & FAQ
├── contact.html            # Contact form
├── README.md               # This file
├── images/
│   ├── hero-home.png       # Homepage hero image
│   ├── hero-services.jpg   # Services page hero
│   └── hero-how-it-works.jpg # How it works hero
└── assets/
    └── css/
        └── main.css        # All styles
```

## Adding a Custom Domain (Later)

Once you want a proper domain like sentinelaiproject.co.nz:

1. Buy domain from registrar (Cloudflare, Namecheap, etc.)
2. In your domain settings, add these DNS records:
   - Type: CNAME, Name: www, Value: sentinelaiproject.github.io
   - Type: A, Name: @, Value: 185.199.108.153
   - Type: A, Name: @, Value: 185.199.109.153
   - Type: A, Name: @, Value: 185.199.110.153
   - Type: A, Name: @, Value: 185.199.111.153
3. In GitHub repository settings → Pages → Custom domain
4. Enter your domain, click Save
5. Wait 24-48 hours for DNS to propagate

## Testing Locally (Optional)

If you want to test changes before publishing:

```bash
# Python 3
python -m http.server 8000

# Then open browser to: http://localhost:8000
```

## Support

For issues or questions about the website:
- Email: sentinelaiproject@outlook.com

## License

All content © 2024 Sentinel AI Project. All rights reserved.
