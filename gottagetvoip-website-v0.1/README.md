# GottaGetVoIP Website v0.1

Initial static-site build based on the approved homepage visual direction.

## Preview locally
From this directory run:

    python3 -m http.server 8080

Then open http://localhost:8080

## Recommended production stack
- Debian 12 or Ubuntu LTS
- Nginx
- Let's Encrypt / Certbot
- Static HTML/CSS/JS

## Suggested server path
    /var/www/gottagetvoip

## Basic Nginx site
    server {
        listen 80;
        server_name gottagetvoip.com www.gottagetvoip.com;
        root /var/www/gottagetvoip;
        index index.html;

        location / {
            try_files $uri $uri/ =404;
        }
    }

After DNS is pointed at the server, install SSL with Certbot and redirect HTTP to HTTPS.

## Status
- Homepage: functional v0.1
- Responsive navigation: functional
- SEO title/description/canonical: started
- robots.txt / sitemap.xml: started
- Service/article directories: scaffolded
- Contact form: not yet implemented
- Real logo/product/install photography: needed
- Reviews: placeholders only; use genuine reviews
- Subpages: next phase

## Design reference
`assets/images/design-reference.png` contains the concept image used as the visual target.
