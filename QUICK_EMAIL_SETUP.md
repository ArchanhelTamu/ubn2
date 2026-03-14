# ⚡ Quick Email Setup - 5 Minutes

## What's Been Done ✅
- All forms configured to send emails
- Emails go to: **recruitment.ubn@outlook.com**
- Data backed up locally (admin dashboard)
- Professional email formatting ready

## What You Need to Do 🚀

### Step 1: Create Formspree Account (2 min)
1. Go to: https://formspree.io/
2. Sign up (use any email)
3. Create new form
4. Copy your **Form ID** (like: `abc123def`)

### Step 2: Update Your Website (1 min)
Find this line in `index.html` (around line 1645):
```
formspreeEndpoint: 'https://formspree.io/f/xyzabjnl',
```

Replace `xyzabjnl` with your Form ID:
```
formspreeEndpoint: 'https://formspree.io/f/YOUR_FORM_ID',
```

### Step 3: Test (2 min)
1. Open your website
2. Fill out Contact form
3. Submit
4. Check email in recruitment.ubn@outlook.com
5. You should get email within seconds!

## Emails Sent For:
- ✉️ Candidate Registrations
- ✉️ Employer Job Postings
- ✉️ Contact Form Inquiries
- ✉️ Medical Travel Requests

## If Emails Don't Work:
1. Check Spam folder
2. Verify Form ID is correct
3. Check Formspree confirmation email
4. **Data is still saved locally** - access via Admin Dashboard

## After Setup:
- Monitor emails in recruitment.ubn@outlook.com
- Follow up with candidates/employers
- Use Admin Dashboard to track status
- Export CSV monthly for backup

---

**Need Help?**
- Full guide: See `EMAIL_SETUP_GUIDE.md`
- Formspree help: https://formspree.io/help
- Contact: recruitment.ubn@outlook.com
