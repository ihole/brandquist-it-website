# Business Website

A professional, responsive website for your business featuring Home, Services, and Contact sections.

## Features

- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Modern UI**: Clean and professional design with smooth animations
- **Contact Form**: Functional contact form with validation
- **Navigation**: Smooth scrolling navigation with mobile hamburger menu
- **SEO Ready**: Semantic HTML structure and proper meta tags
- **Fast Loading**: Optimized CSS and JavaScript for quick page loads

## File Structure

```
brandquistit/
├── index.html          # Main HTML file
├── styles.css          # CSS styles and responsive design
├── script.js           # JavaScript functionality
├── .github/
│   └── copilot-instructions.md
└── README.md           # This file
```

## Customization

### 1. Update Business Information

Edit `index.html` to replace placeholder content:

- **Business Name**: Replace "Your Business" with your actual business name
- **Services**: Update the 4 service cards with your actual services
- **Contact Information**: Update address, phone, email, and business hours
- **Social Media**: Add your actual social media links

### 2. Styling

- Modify `styles.css` to change colors, fonts, or layout
- Current color scheme uses blue (#3498db) as primary color
- Font family is set to 'Inter' from Google Fonts

### 3. Content

- Add your business logo (replace the placeholder in the hero section)
- Update service descriptions and icons
- Customize the hero section messaging

## Deploying to GoDaddy

### Method 1: File Manager (Recommended for beginners)

1. **Log into your GoDaddy hosting account**
2. **Access File Manager**:
   - Go to your hosting dashboard
   - Find "File Manager" or "Files" section
   - Click to open

3. **Navigate to public folder**:
   - Look for `public_html` or `www` folder
   - This is where your website files go

4. **Upload your files**:
   - Upload `index.html`, `styles.css`, and `script.js`
   - Make sure `index.html` is in the root of the public folder

5. **Test your website**:
   - Visit your domain in a browser
   - Your website should now be live!

### Method 2: FTP Upload

1. **Get FTP credentials from GoDaddy**:
   - Host: Your domain or FTP server address
   - Username: Your hosting username
   - Password: Your hosting password
   - Port: Usually 21

2. **Use an FTP client** (like FileZilla):
   - Connect to your server using the credentials
   - Navigate to the `public_html` or `www` folder
   - Upload `index.html`, `styles.css`, and `script.js`

### Method 3: GoDaddy Website Builder (Alternative)

If you prefer a visual editor:
1. Use GoDaddy's Website Builder
2. Choose a template and customize it
3. Copy content and styling concepts from this project

## Important Notes

- **Domain Configuration**: Make sure your domain is pointed to your hosting account
- **File Names**: Keep `index.html` as the main file name (GoDaddy automatically serves this as the homepage)
- **Case Sensitivity**: Some servers are case-sensitive, so keep file names lowercase
- **Testing**: Always test your website after uploading

## Contact Form Setup

The contact form currently shows a success message but doesn't actually send emails. To make it functional:

1. **Use GoDaddy's form handling service** (if available)
2. **Add server-side processing** (PHP, Node.js, etc.)
3. **Use a third-party service** like Formspree, Netlify Forms, or EmailJS

### Simple PHP Contact Form (for GoDaddy hosting with PHP support)

Create a `contact.php` file:

```php
<?php
if ($_POST['name'] && $_POST['email'] && $_POST['message']) {
    $to = "your-email@domain.com";
    $subject = "Contact Form: " . $_POST['subject'];
    $message = "From: " . $_POST['name'] . "\n";
    $message .= "Email: " . $_POST['email'] . "\n\n";
    $message .= $_POST['message'];
    
    mail($to, $subject, $message);
    echo "Message sent successfully!";
} else {
    echo "Please fill all fields.";
}
?>
```

Then update the form action in `index.html`:
```html
<form id="contactForm" action="contact.php" method="POST">
```

## Support

For hosting-specific issues:
- Contact GoDaddy support
- Check GoDaddy's help documentation
- Use GoDaddy's community forums

For website customization:
- Modify the HTML, CSS, and JavaScript files
- Test changes locally before uploading
- Keep backups of your files

## Browser Compatibility

This website works with:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Performance Tips

- Images should be optimized (use WebP format when possible)
- Keep file sizes small for faster loading
- Test website speed using tools like Google PageSpeed Insights
- Consider using a CDN for better global performance

---

**Need Help?** Contact your web developer or GoDaddy support for assistance with deployment or customization.