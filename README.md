# WhatsApp Cloud API setup for InteriorDesign

This project includes a lightweight Node.js backend that sends selected design images through the WhatsApp Cloud API.

## 1) Install dependencies

npm install

## 2) Configure WhatsApp Cloud API

Create a `.env` file in the project root using the example below:

```
PORT=3000
WHATSAPP_TOKEN=your_whatsapp_cloud_api_token
WHATSAPP_PHONE_NUMBER_ID=your_phone_number_id
WHATSAPP_SENDER_NUMBER=919916511599
```

Notes:
- Get `WHATSAPP_TOKEN` from Meta for Developers > WhatsApp > API Setup
- Get `WHATSAPP_PHONE_NUMBER_ID` from your WhatsApp business account
- `WHATSAPP_SENDER_NUMBER` must be in international format without `+`

## 3) Start the app

npm start

Then open the site at:

http://localhost:3000

## 4) Frontend behavior

The page will send selected design images to the backend using `/api/send-whatsapp`.
The backend fetches the public image URLs, uploads them to WhatsApp, and sends them to the configured phone number.

## 5) Important caveat

The selected images must be publicly accessible via HTTPS URLs.
The project already uses GitHub Pages image URLs, which are public and work for this flow.

## 6) Production hosting

If you deploy it on Render, Railway, Vercel, or another host, make sure the `.env` values are set in the hosting dashboard.
