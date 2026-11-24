SUPER AI ACADEMY - STATIC WEBSITE (HTML + CSS)
==============================================

Files
  index.html     Home page
  about.html     About Us + FAQ
  courses.html   Courses
  contact.html   Contact page with enquiry form (opens visitor's email app)
  404.html       Custom "page not found" page
  css/style.css  All styling (responsive, no frameworks)
  images/        Logo, favicon and founder photos
  .htaccess      Apache config: clean URLs, 404 page, gzip, caching, security headers
  robots.txt     Search engine rules

Deploy on Apache (cPanel / shared hosting)
  1. Upload the ZIP to public_html (or your domain's folder) via File Manager.
  2. Extract it so index.html sits directly inside public_html.
  3. Make sure hidden files are shown so .htaccess is uploaded too.
  4. Visit your domain.

Deploy on your own Apache server (Ubuntu)
  sudo unzip superai-academy-website.zip -d /var/www/html/
  sudo a2enmod rewrite headers expires deflate
  # In your site config set:  AllowOverride All   for /var/www/html
  sudo systemctl restart apache2

Customise
  - "Enroll Now" buttons link to the payment page (search "checkout" to change it).
  - Replace the placeholder phone, email and address (search "90000" and "info@superaiacademy.com").
  - Replace "Learner Name" testimonials with real ones.
  - Colours are variables at the top of css/style.css.
  - If you install the site in a sub-folder, change "ErrorDocument 404 /404.html"
    in .htaccess to "/your-folder/404.html".
