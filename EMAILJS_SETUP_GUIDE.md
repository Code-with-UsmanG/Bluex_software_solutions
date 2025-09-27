# EmailJS Setup Guide for BlueX Contact Form

This guide will help you set up EmailJS to enable real email sending functionality for your contact form.

## Step 1: Create EmailJS Account

1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Click "Sign Up" and create a free account
3. Verify your email address

## Step 2: Set Up Email Service

1. In your EmailJS dashboard, go to **Email Services**
2. Click **Add New Service**
3. Choose your email provider:
   - **Gmail** (recommended for personal use)
   - **Outlook**
   - **Yahoo**
   - Or any other supported provider

4. Follow the setup instructions for your chosen provider
5. Note down your **Service ID** (e.g., `service_abc123`)

## Step 3: Create Email Template

1. Go to **Email Templates** in your dashboard
2. Click **Create New Template**
3. Use this template content:

```
Subject: New Contact Form Message - {{subject}}

Hello BlueX Team,

You have received a new message from your website contact form:

Name: {{sender_name}}
Email: {{sender_email}}
Subject: {{subject}}

Message:
{{message}}

---
Reply to: {{reply_to}}
This message was sent from your BlueX Software Solutions website.
```

4. Save the template and note down your **Template ID** (e.g., `template_xyz789`)

## Step 4: Get Public Key

1. Go to **Account** → **General**
2. Find your **Public Key** (e.g., `user_abcdef123456`)
3. Copy this key

## Step 5: Update Your HTML File

Replace the placeholder values in your `index.html` file:

```javascript
const EMAILJS_SERVICE_ID = 'YOUR_SERVICE_ID'; // Replace with your actual service ID
const EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID'; // Replace with your actual template ID
const EMAILJS_PUBLIC_KEY = 'YOUR_PUBLIC_KEY'; // Replace with your actual public key
```

For example:
```javascript
const EMAILJS_SERVICE_ID = 'service_abc123';
const EMAILJS_TEMPLATE_ID = 'template_xyz789';
const EMAILJS_PUBLIC_KEY = 'user_abcdef123456';
```

## Step 6: Test Your Setup

1. Open your website in a browser
2. Go to the Contact section
3. Fill out the form with test data
4. Submit the form
5. Check your email for the message

## Features Included

✅ **Real Email Sending**: Messages are sent directly to your email
✅ **Form Validation**: Client-side validation for all fields
✅ **Loading States**: Visual feedback during email sending
✅ **Success/Error Messages**: User-friendly status messages
✅ **Email Formatting**: Professional email template
✅ **Spam Protection**: Basic validation and error handling

## Free Tier Limits

EmailJS free tier includes:
- 200 emails per month
- 2 email services
- 2 email templates
- Basic support

## Troubleshooting

### Common Issues:

1. **"EmailJS is not defined" error**
   - Make sure the EmailJS CDN script is loaded before your JavaScript

2. **"Invalid service ID" error**
   - Double-check your service ID in the EmailJS dashboard

3. **"Template not found" error**
   - Verify your template ID and make sure the template is published

4. **Emails not received**
   - Check your spam folder
   - Verify your email service configuration
   - Check the EmailJS dashboard for error logs

### Testing Tips:

- Use a real email address for testing
- Check browser console for any JavaScript errors
- Test with different email providers
- Verify all form fields are filled correctly

## Security Notes

- Your public key is safe to use in client-side code
- EmailJS handles the actual email sending securely
- No sensitive data is stored on your website
- Consider adding reCAPTCHA for additional spam protection

## Need Help?

- EmailJS Documentation: https://www.emailjs.com/docs/
- EmailJS Support: support@emailjs.com
- Check the browser console for detailed error messages

---

Your contact form is now ready to send real emails! 🚀
