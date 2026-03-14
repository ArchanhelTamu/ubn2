# 🚀 Formspree Setup Instructions for UBN Website

## Quick Overview
Your UBN website has **4 forms** that need to send emails to `recruitment.ubn@outlook.com`:
1. ✅ Candidate Registration Form
2. ✅ Employer Job Posting Form
3. ✅ Contact Inquiry Form
4. ✅ Medical Travel Consultation Form

All forms are configured to use **Formspree** - a free service that bridges static websites with email delivery.

---

## 📋 Step-by-Step Setup (5 Minutes)

### Step 1: Create a Formspree Account
1. **Visit** https://formspree.io/
2. **Click** "Sign Up" button (top right)
3. **Enter your email:** `recruitment.ubn@outlook.com`
4. **Set a password** of your choice
5. **Click** "Sign Up"
6. **Verify your email** - Check your inbox for confirmation link

### Step 2: Create Your First Form
1. **Log in** to your new Formspree account
2. **Click** "Create" button (or "New Form")
3. **Name your form:** `UBN Website Forms`
4. **Email address:** Should default to `recruitment.ubn@outlook.com` ✓
5. **Click** "Create Form"

### Step 3: Get Your Form ID
1. After creating the form, you'll see a page showing your **Form ID**
2. It looks like: `xyzabc123def` (alphanumeric string)
3. **Copy this ID** - you'll need it in the next step

**Example what it looks like:**
```
Your form endpoint is:
https://formspree.io/f/YOUR_FORM_ID_HERE
```

### Step 4: Update Your Website
Now you need to add your Form ID to the website code:

1. **Open** `c:\Users\Administrator\Documents\websites\UBN RECRUITMENT\static_site\index.html`
2. **Find line 2032** (use Ctrl+G in most editors)
3. **Look for:**
   ```javascript
   formspreeEndpoint: 'https://formspree.io/f/xyzabjnl',
   ```
4. **Replace `xyzabjnl`** with YOUR Form ID from Step 3
5. **Example (if your ID is `abc123def`):**
   ```javascript
   formspreeEndpoint: 'https://formspree.io/f/abc123def',
   ```
6. **Save the file** (Ctrl+S)

---

## ✅ Testing Your Setup

### Test 1: Submit a Contact Form
1. **Open** `index.html` in your browser
2. **Click** "Contact" in the menu
3. **Fill out the contact form** with test data
4. **Submit the form**
5. **Check** `recruitment.ubn@outlook.com` inbox within 30 seconds
6. **You should see** an email with all form details

### Test 2: Submit a Candidate Registration
1. **Click** "Candidates" in the menu
2. **Fill the registration form** (all required fields)
3. **Optionally upload a CV** (any PDF/DOC file under 5MB)
4. **Submit**
5. **Check your inbox** - you should receive the full candidate details

### Test 3: Submit an Employer Form
1. **Click** "Employers" in the menu
2. **Fill the job posting form**
3. **Submit**
4. **Check your inbox** - confirmation email with job details

### Test 4: Submit Medical Travel Form
1. **Click** "Medical Travel" in the menu
2. **Fill the inquiry form**
3. **Submit**
4. **Check your inbox** - medical travel request details

---

## 🎯 What Happens When You Submit a Form

### Form Submission Flow:
```
User fills form on website
       ↓
Form validates locally
       ↓
Data saved to browser (LocalStorage)
       ↓
Email sent to Formspree API
       ↓
Formspree forwards to recruitment.ubn@outlook.com
       ↓
✉️ Email arrives in your inbox
```

### Email Format Example (Candidate Registration):
```
Subject: New Candidate Registration - John Smith

NEW CANDIDATE REGISTRATION

Candidate ID: UBN-C-1678123456789
Full Name: John Smith
Country: United Kingdom
Email: john@example.com
WhatsApp: +44 1234567890
Healthcare Profession: Registered Nurse
Years of Experience: 5-10 years
Current Employer: London Hospital
Key Skills: Patient care, medication management
Availability: Immediately
Preferred Locations: USA, UK, Canada

CV/RESUME FILE:
File Name: John_Smith_CV.pdf
File Size: 245.50KB
Upload Date: 2026-03-13T10:30:00Z

Submission Date: 2026-03-13T10:30:00Z

Please review this candidate and follow up accordingly.
```

---

## 🔧 Troubleshooting

### Problem 1: Email Not Arriving
**Solution:**
1. Check spam/junk folder in Outlook
2. Verify Form ID is correct (copy-paste exactly from Formspree)
3. Clear browser cache (Ctrl+Shift+Delete)
4. Try submitting from a different browser
5. Check Formspree dashboard to see if submission was recorded

### Problem 2: "Invalid Form ID" Error
**Solution:**
1. Go back to Formspree.io
2. Log in and check your form
3. Copy the Form ID again (make sure no spaces)
4. Update the website code again
5. Save and refresh browser

### Problem 3: File Upload Not Working
**Solution:**
1. Maximum file size is **5MB**
2. Allowed formats: **PDF, DOC, DOCX, TXT**
3. Check browser console (F12) for error messages
4. File info is stored in your email even if not uploaded

### Problem 4: Form Submits but No Email
**Solution:**
1. Data IS being saved locally (check Admin Dashboard)
2. Formspree might be temporarily offline
3. Try submitting again after a few minutes
4. Contact Formspree support: https://formspree.io/help

---

## 📊 Admin Dashboard Features

Even if emails don't arrive, your data is SAFE:

1. **Click "Admin"** in the menu
2. **Tab 1 - Candidates:** See all candidate registrations
3. **Tab 2 - Employers:** See all job postings
4. **Tab 3 - Inquiries:** See contact form submissions

**Features:**
- ✅ Filter by status (Pending, Reviewed, Contacted, Hired)
- ✅ Sort by date
- ✅ View all details
- ✅ Export as CSV (download spreadsheet)

---

## 📝 Useful Links

| Resource | URL |
|----------|-----|
| **Formspree Website** | https://formspree.io/ |
| **Your Website** | Open `static_site/index.html` in browser |
| **Your Email** | recruitment.ubn@outlook.com |
| **Formspree Help** | https://formspree.io/help |

---

## ✨ Summary Checklist

- [ ] Created Formspree account
- [ ] Verified email at Formspree
- [ ] Created a new form at Formspree
- [ ] Copied the Form ID
- [ ] Updated line 2032 in `index.html`
- [ ] Saved the `index.html` file
- [ ] Tested Candidate form ✓
- [ ] Tested Employer form ✓
- [ ] Tested Contact form ✓
- [ ] Tested Medical Travel form ✓
- [ ] All emails arriving in inbox ✓

---

## 🚀 You're Done!

Once you complete these steps, **all forms will send emails directly to your inbox**.

**Questions?** Check the FAQ page on your website or contact Formspree support.

**Happy recruiting!** 🎉
