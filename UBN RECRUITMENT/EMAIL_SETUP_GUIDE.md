# Email Setup Guide for Ultimate Baby Nurses

## Overview
All forms on the website are now configured to send email notifications to **recruitment.ubn@outlook.com** when submitted.

## How It Works

### Forms That Send Emails
1. **Candidate Registration** → Sends candidate details to admin
2. **Employer Job Posting** → Sends job posting details to admin
3. **Contact Form** → Sends inquiry to admin
4. **Medical Travel Inquiry** → Sends medical travel request to admin

### Email Flow

```
User Submits Form
        ↓
Data Saved to LocalStorage (local backup)
        ↓
Email Sent to recruitment.ubn@outlook.com
        ↓
Admin Receives Notification Email
        ↓
Admin Reviews & Follows Up with User
```

---

## Setup Instructions

### Step 1: Create Formspree Account

Formspree is a free service that allows static websites to send emails without a backend.

**How to Set Up:**

1. Visit: https://formspree.io/
2. Sign up with your email (recruitment.ubn@outlook.com recommended)
3. Click "Create New Form"
4. Give it a name: "UBN Website Forms"
5. You'll get a **Form ID** (looks like: `xyzabjnl`)

### Step 2: Update Your Website Code

In `index.html`, find the Configuration section (around line 1645):

**Current Configuration:**
```javascript
const CONFIG = {
    storageKey: 'ubn_form_data',
    candidatePrefix: 'UBN-C',
    employerPrefix: 'UBN-E',
    inquiryPrefix: 'UBN-I',
    formspreeEndpoint: 'https://formspree.io/f/xyzabjnl', // UPDATE THIS
    adminEmail: 'recruitment.ubn@outlook.com'
};
```

**Replace `xyzabjnl` with your actual Formspree Form ID:**
```javascript
formspreeEndpoint: 'https://formspree.io/f/YOUR_FORM_ID_HERE'
```

### Step 3: Test the Setup

1. Open your website
2. Go to the Contact page
3. Fill out and submit a test form
4. Check your email (recruitment.ubn@outlook.com) for the notification
5. You should receive an email within seconds

---

## What Each Email Contains

### Candidate Registration Email
- Candidate ID
- Full name
- Country
- Email address
- WhatsApp number
- Healthcare profession
- Years of experience
- Current employer
- Skills
- Availability
- Preferred locations
- CV file name
- Submission date/time

### Employer Job Posting Email
- Employer ID
- Company name
- Contact person
- Email
- Country
- Role required
- Number of staff needed
- Required skills
- Visa sponsorship availability
- Submission date/time

### Contact Form Email
- Inquiry ID
- Full name
- Email
- User type
- Message
- Submission date/time

### Medical Travel Inquiry Email
- Inquiry ID
- Patient name
- Country of origin
- Destination hospital/city
- Medical needs/treatment type
- Preferred travel dates
- Email
- Phone
- Additional information
- Submission date/time

---

## Data Backup System

**Your website has a two-layer system:**

1. **Local Storage** (Browser)
   - Automatically saves all form submissions locally
   - Acts as backup if email fails
   - Data accessible via Admin Dashboard
   - Can export as CSV anytime

2. **Email Notifications**
   - Sends to recruitment.ubn@outlook.com
   - Allows immediate follow-up
   - Professional notification system
   - Can be forwarded/archived

**This means:**
✅ Form data is NEVER lost
✅ You get email notifications
✅ You can access data in Admin Dashboard
✅ You can export data as CSV

---

## Advanced Configuration (Optional)

### Alternative Email Services

If you prefer not to use Formspree, you can use:

1. **EmailJS** (https://www.emailjs.com/)
   - Free tier: 200 emails/month
   - Similar setup process

2. **Basin** (https://basin.io/)
   - Very simple
   - Completely free

3. **Netlify Forms** (if hosted on Netlify)
   - Built-in form handling
   - Free tier available

### To Switch Services:
Replace the `sendEmail()` function with your preferred service's code.

---

## Troubleshooting

### Problem: Not Receiving Emails

**Solution 1: Check Formspree Confirmation**
- Formspree may send you a confirmation email on first submission
- Click the link in confirmation email to activate
- Then subsequent emails will work

**Solution 2: Check Email Filter**
- Check Spam/Junk folder
- Add Formspree to contacts
- Check email filter rules

**Solution 3: Verify Form ID**
- Make sure you updated the Form ID in the code
- Form ID format: `https://formspree.io/f/XXXXX` (5 characters)
- If missing or wrong, emails won't send

**Solution 4: Check Browser Console**
- Open DevTools (F12)
- Go to Console tab
- Look for any error messages
- This helps diagnose the issue

### Problem: Forms Still Work But Emails Not Sending

**This is fine!** The website is still fully functional:
- ✅ Data is saved to LocalStorage
- ✅ Admin Dashboard shows all submissions
- ✅ You can export as CSV
- ✅ Fix email issue when you have time

### Solution: Double-Check Formspree Status

1. Visit https://formspree.io/
2. Log in to your account
3. Check form status
4. Verify form is active
5. Check recent submissions

---

## Best Practices

### Email Management

1. **Create Email Filters**
   - Create filter: From: Formspree
   - Route to "UBN Submissions" folder
   - Keeps inbox organized

2. **Set Up Auto-Responses**
   - If you have Outlook rules
   - Can auto-respond to confirmations
   - Add to contacts on receipt

3. **Weekly Backup**
   - Export CSV from Admin Dashboard
   - Save locally
   - Keep records of all submissions

### Security Notes

- **Never share your Formspree Form ID publicly** in git/public repos
- Form ID acts like a password
- If exposed, anyone could use your form

---

## Monthly Monitoring

### What to Check:
- [ ] Emails still arriving
- [ ] No spam emails in filter
- [ ] Admin Dashboard updating correctly
- [ ] CSV exports working
- [ ] No error messages in console

### Monthly Tasks:
- [ ] Export and backup CSV of all submissions
- [ ] Archive replied inquiries
- [ ] Review follow-up status on pending inquiries
- [ ] Test one form to ensure email working

---

## Scaling Up (When You Need More)

### If Getting Lots of Submissions:

**Option 1: Upgrade Formspree**
- Free → Premium (~$25/month)
- More submissions allowed
- Better organization

**Option 2: Move to Email Service**
- MailChimp, SendGrid, Brevo
- More robust
- Better for high volume

**Option 3: Get Your Own Backend**
- Node.js/Express server
- Database for submissions
- More control
- More expensive

---

## Contact

For email setup questions:
- Visit: https://formspree.io/
- Email: recruitment.ubn@outlook.com
- WhatsApp: +27 670-486-798

---

## Checklist: Email Setup Complete

- [ ] Created Formspree account
- [ ] Generated Form ID
- [ ] Updated index.html with Form ID
- [ ] Tested contact form
- [ ] Received test email
- [ ] Verified email contains all information
- [ ] Set up email filters (optional)
- [ ] Bookmarked admin dashboard
- [ ] Exported first CSV backup

**Status:** ✅ Ready to receive form submissions
