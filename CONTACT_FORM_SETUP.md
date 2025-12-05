# Contact Form Setup Instructions

The contact form is now fully functional with email notifications. Follow these steps to complete the setup:

## Option 1: Formspree (Recommended - Free & Easy)

1. **Sign up for Formspree**
   - Go to https://formspree.io
   - Create a free account (allows 50 submissions/month)

2. **Create a new form**
   - Click "New Form" in your dashboard
   - Name it "Attic AFH Contact Form"
   - Copy your form endpoint (looks like: `https://formspree.io/f/xpzgkqyz`)

3. **Update the form action**
   - Open `contact-us.html`
   - Find the line: `action="https://formspree.io/f/YOUR_FORM_ID"`
   - Replace `YOUR_FORM_ID` with your actual Formspree form ID
   - Example: `action="https://formspree.io/f/xpzgkqyz"`

4. **Configure email notifications**
   - In Formspree dashboard, go to your form settings
   - Add your email address to receive notifications
   - Customize the email template if desired

5. **Test the form**
   - Submit a test message
   - Check your email for the notification

## Option 2: EmailJS (Alternative)

If you prefer EmailJS:

1. Sign up at https://www.emailjs.com
2. Create an email service (Gmail, Outlook, etc.)
3. Create an email template
4. Get your Public Key and Service ID
5. Replace the form submission code in `contact-us.html` with EmailJS integration

## Option 3: Custom Backend

If you have your own backend:

1. Update the form `action` attribute to point to your API endpoint
2. Ensure your endpoint accepts POST requests with the form data
3. Handle email sending on your server

## Form Features

✅ **Client-side validation**
- Required field validation
- Email format validation
- Real-time error messages
- Visual feedback on input fields

✅ **User experience**
- Loading spinner during submission
- Success message display
- Error message display
- Form reset after successful submission
- Honeypot spam protection

✅ **Data collected**
- First Name (required)
- Last Name (required)
- Email Address (required)
- Phone Number (optional)
- Interest Type (Pricing/Tour/General Question)
- Message (required, min 10 characters)

## Testing

After setup, test the form:
1. Fill out all required fields
2. Submit the form
3. Check your email for the notification
4. Verify the form shows success message
5. Test error handling by submitting invalid data

## Troubleshooting

- **Form not submitting**: Check that you've replaced `YOUR_FORM_ID` with your actual Formspree ID
- **No email received**: Check Formspree dashboard for submission logs
- **Validation errors**: Ensure all required fields are filled correctly
- **Network errors**: Check browser console for detailed error messages

## Security Notes

- The form includes a honeypot field (`_gotcha`) to prevent spam
- All form data is validated client-side before submission
- Formspree handles server-side validation and spam filtering
- Never expose API keys or sensitive credentials in client-side code

