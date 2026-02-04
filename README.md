# Adora Construction Website 🏗️

 live business site: https://adora-construction.co.uk

Flask app I threw together for the company – handles everything from showing off services and project photos to taking inquiries and letting me manage content from the backend.

Site's fully up and running: https://adora-construction.co.uk

## What it's got

- **Home page** – quick overview of what we do, highlights popular services with small gallery previews, customer reviews, and a call-to-action contact button
- **Services pages** – dedicated page for each service (kitchen renos, bathrooms, wardrobes, plumbing, etc.) with detailed descriptions and a scrolling gallery of example work
- **Gallery section** – full project gallery with all photos, plus separate pages for each category so people can browse kitchens, bathrooms, whatever they're interested in 📸
- **Contact form** – proper form where customers can write their message, pick reference images from our gallery, upload their own photos if they want, and it automatically bundles everything into neat PDFs then emails it straight to me
- **Admin panel** – login area where I can add new services, upload fresh project images, approve/edit testimonials, add tips, all without touching code
- **Customer reviews** – section showing real feedback, plus a form for new reviews to come in

Had a massive headache for ages where all gallery images would vanish every time I pushed an update (Render wipes the filesystem). Finally sorted it by shifting everything over to Supabase Storage – created a public bucket called "gallery". Images are permanent now, no more re-uploading after every deploy.

## Tech behind it

- Flask running the whole thing
- Supabase handling the database and all image storage now
- SQLAlchemy for the models
- Flask-Admin for the backend interface
- Bootstrap 5 keeping it looking clean and working properly on phones
- ReportLab + Pillow to generate those PDF attachments from the contact form
- Hosted on Render with gunicorn

Site's stable, loads quick, and does exactly what I need for the business. If something looks off or you've got suggestions, drop an issue.
