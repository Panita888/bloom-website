# Bloom Website

Where Businesses Bloom - Helping clinics capture every enquiry with instant Instagram responses.

## Website Structure

- `index.html` - Home page
- `about.html` - About page
- `contact.html` - Contact/Get Started page
- `Bloom_logo.png` - Logo file

## Setup

1. Clone this repository
2. Open `index.html` in your browser
3. For the contact form to work, replace `YOUR_FORM_ID` in `contact.html` with your actual form service ID (Formspree, etc.)

## Deployment

### GitHub Pages (Free Hosting)

1. Go to repository Settings
2. Click "Pages" in the left sidebar
3. Under "Source", select "main" branch
4. Click "Save"
5. Your site will be live at `https://yourusername.github.io/bloom-website/`

### Custom Domain (joinbloom.tech)

Once GitHub Pages is enabled:

1. In your domain registrar (GoDaddy, etc.), add these DNS records:
   ```
   A Record: 185.199.108.153
   A Record: 185.199.109.153
   A Record: 185.199.110.153
   A Record: 185.199.111.153
   CNAME Record: www -> yourusername.github.io
   ```

2. Create a file named `CNAME` in your repository with this content:
   ```
   joinbloom.tech
   ```

3. Wait 24-48 hours for DNS propagation

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript
- Inter font family (Google Fonts)

## License

© 2026 Bloom. All rights reserved.
