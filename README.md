# Nodemailer Email Service

A simple email service built with Express and Nodemailer that allows sending emails through Gmail SMTP.

## Setup

1. Clone the repository
2. Install dependencies:
```bash
npm install
```
3. Create a `.env` file in the root directory with the following variables:
```env
EMAIL=your-gmail@gmail.com
APP_PASSWORD=your-gmail-app-password
PORT=3000
```

### Gmail App Password Setup

1. Go to your Google Account settings
2. Navigate to Security > 2-Step Verification
3. Scroll down and select "App passwords"
4. Generate a new app password for this application
5. Copy the generated password to your `.env` file

## API Documentation

### Send Email
Send an email using the service.

**Endpoint:** POST `/send-email`

**Request Body:**
```json
{
    "to": "recipient@example.com",
    "subject": "Email Subject",
    "text": "Email content goes here"
}
```

**Response Success (200):**
```json
{
    "message": "Email sent successfully"
}
```

**Response Error (500):**
```json
{
    "error": "Failed to send email"
}
```

## Running the Application

Development mode:
```bash
npm run dev
```

Production mode:
```bash
npm start
```

## Environment Variables

- `EMAIL`: Your Gmail address
- `APP_PASSWORD`: Your Gmail app password
- `PORT`: Server port (defaults to 3000)
