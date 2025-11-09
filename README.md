# Portfolio - Sanni Muhammed Arafat

Modern single-page portfolio (light theme) with a separate contact page.
Technology: HTML, CSS, JavaScript (frontend) + Node.js, Express, MongoDB (Atlas), Nodemailer (backend).

## What is included
- `public/` - frontend files:
  - `index.html` (single-page portfolio)
  - `contact.html` (separate contact page)
  - `styles.css`
  - `app.js`
- `server.js` - Express server that serves frontend, stores contact messages to MongoDB, and sends email via Nodemailer.
- `.env.example` - example environment variables.
- `package.json`
- `models/Contact.js` - Mongoose model
- `README.md` (this file)

## Quick setup (local)
1. Install Node 18+ and npm.
2. Copy `.env.example` to `.env` and fill values:
   - `MONGODB_URI` - your MongoDB Atlas connection string (replace `<password>` and DB name)
   - `EMAIL_USER` - your Gmail (e.g. sanniwahab23@gmail.com)
   - `EMAIL_PASS` - Gmail app password (or SMTP password)
   - `PORT` - optional (default 3000)
3. Whitelist your local IP / 0.0.0.0/0 in MongoDB Atlas Network Access (for testing) or add your app IP.
4. Install and run:
   ```bash
   npm install
   npm start
   ```
5. Open your browser:
   - Portfolio: http://localhost:3000/
   - Contact page: http://localhost:3000/contact.html

## Notes
- The contact form posts to `/api/contact`. Server stores message in MongoDB and sends an email to `EMAIL_USER`.
- The `.env.example` contains placeholders; replace them before starting.
- For Gmail SMTP, you should create an App Password (if using 2FA) and put it into `EMAIL_PASS`.
