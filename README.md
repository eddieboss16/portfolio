# Personal Portfolio Project

## Overview
A full-stack personal portfolio website with a Node.js/Express backend to handle contact form submissions.

## Project Structure
```
portfolio/
├── backend/                 # Backend API server
│   ├── server.js           # Main server file
│   ├── package.json        # Backend dependencies
│   ├── .env               # Environment variables
│   └── routes/            # API routes (future)
├── frontend/               # Frontend website
│   ├── index.html         # Main HTML file
│   ├── script.js          # Frontend JavaScript
│   ├── style.css          # CSS styles
│   └── assets/
│       └── images/        # Images and media
├── package.json           # Root package.json
└── README.md             # This file
```

## Backend API Endpoints
- `POST /api/contact`: Accepts JSON { name, email, phone?, subject, message }. If SMTP is configured, sends an email; otherwise logs to the server.
- `GET /api/health`: Health check endpoint.

## Environment Configuration
The backend uses a `.env` file located in the `backend/` directory:

```env
PORT=3000
CORS_ORIGIN=http://localhost:3000
SMTP_HOST=
SMTP_PORT=587
SMTP_SECURE=false
SMTP_USER=
SMTP_PASS=
MAIL_FROM=
MAIL_TO=
```

## Getting Started

### Install Dependencies
```bash
npm run install-all
```

### Development
```bash
npm run dev
```

### Production
```bash
npm start
```

## Notes
- The server serves static files from the `frontend/` directory
- If you don't set SMTP_* variables, contact messages will be printed to the server console instead of being emailed
- The backend runs on port 3000 by default

