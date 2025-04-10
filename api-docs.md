# API Documentation

## Base URL
```
http://localhost:3000
```

## Endpoints

### Send Email

Send an email through the Gmail SMTP server.

**URL:** `/send-email`
**Method:** `POST`
**Content-Type:** `application/json`

#### Request Body Parameters

| Parameter | Type   | Required | Description                    |
|-----------|--------|----------|--------------------------------|
| to        | string | Yes      | Recipient's email address      |
| subject   | string | Yes      | Subject line of the email     |
| text      | string | Yes      | Body content of the email     |

#### Example Request
```curl
curl -X POST http://localhost:3000/send-email \
  -H "Content-Type: application/json" \
  -d '{
    "to": "recipient@example.com",
    "subject": "Test Email",
    "text": "Hello from Nodemailer!"
  }'
```

#### Success Response

**Code:** 200
**Content:**
```json
{
    "message": "Email sent successfully"
}
```

#### Error Response

**Code:** 500
**Content:**
```json
{
    "error": "Failed to send email"
}
```

## Error Handling
The API implements basic error handling for:
- Invalid email addresses
- SMTP server connection issues
- Missing required fields
