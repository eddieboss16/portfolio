Personal Portfolio Backend

Overview
This adds a minimal Node/Express backend to handle contact form submissions from the portfolio.

Endpoints
- POST /api/contact: Accepts JSON { name, email, phone?, subject, message }. If SMTP is configured, sends an email; otherwise logs to the server.
- GET /api/health: Health check.

Environment
Create a .env file (you can copy from below):

PORT=3000
CORS_ORIGIN=http://localhost:3000
SMTP_HOST=
SMTP_PORT=587
SMTP_SECURE=false
SMTP_USER=
SMTP_PASS=
MAIL_FROM=
MAIL_TO=

Run
- Development: npm run dev
- Production: npm start

Notes
- If you don’t set SMTP_* variables, messages will be printed to the server console instead of being emailed.

