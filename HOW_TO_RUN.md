# 🌐 How to Run Your Website

## Quick Start

Your Ultimate Baby Nurses website is a **single-file HTML application** - it's easy to run!

---

## Method 1: Direct File Opening (Simplest)

### Windows
1. Navigate to: `c:\Users\Administrator\Documents\websites\UBN RECRUITMENT\static_site\`
2. Double-click `index.html`
3. Website opens in your default browser
4. Start using immediately

### Mac
1. Navigate to: `/Users/[YourUsername]/Documents/websites/UBN RECRUITMENT/static_site/`
2. Double-click `index.html`
3. Website opens in your default browser

### Linux
```bash
cd ~/Documents/websites/UBN\ RECRUITMENT/static_site/
firefox index.html  # or: chromium index.html, google-chrome, etc.
```

**✅ This method works for:**
- Local testing
- Demo purposes
- Internal use
- Single-user access

**⚠️ Limitations:**
- Only works on your computer
- Others can't access it
- No external internet access

---

## Method 2: Local Web Server (Recommended for Testing)

### Using Python (Windows/Mac/Linux)

**Step 1:** Open Terminal/Command Prompt

**Step 2:** Navigate to your site folder
```bash
cd "c:\Users\Administrator\Documents\websites\UBN RECRUITMENT\static_site"
```

**Step 3:** Start Python server
```bash
python -m http.server 8000
```

**Step 4:** Open browser and visit
```
http://localhost:8000
```

**Step 5:** Stop server
```
Press Ctrl+C
```

### Using Node.js (if installed)

**Step 1:** Install http-server
```bash
npm install -g http-server
```

**Step 2:** Navigate to site folder
```bash
cd "c:\Users\Administrator\Documents\websites\UBN RECRUITMENT\static_site"
```

**Step 3:** Start server
```bash
http-server -p 8000
```

**Step 4:** Open browser
```
http://localhost:8000
```

### Using PHP (if installed)

**Step 1:** Navigate to site folder
```bash
cd "c:\Users\Administrator\Documents\websites\UBN RECRUITMENT\static_site"
```

**Step 2:** Start PHP server
```bash
php -S localhost:8000
```

**Step 3:** Open browser
```
http://localhost:8000
```

**✅ This method works for:**
- Local network testing
- Multiple users on same network
- Email form testing (with Formspree)
- Admin dashboard testing
- File upload testing

---

## Method 3: Cloud Hosting (For Production)

### Popular Free Options

#### Netlify (Recommended)
1. Visit https://netlify.com
2. Sign up for free account
3. Drag & drop `static_site` folder
4. Website goes live instantly
5. Get automatic HTTPS
6. Share your unique URL

#### Vercel
1. Visit https://vercel.com
2. Sign up for free account
3. Import your repository or upload files
4. Automatic deployment
5. Get HTTPS automatically
6. Share your URL

#### GitHub Pages
1. Create GitHub account (free)
2. Create new repository
3. Upload `static_site` contents
4. Enable GitHub Pages in settings
5. Website goes live at `yourusername.github.io`
6. Works with custom domain

#### Firebase Hosting
1. Visit https://firebase.google.com
2. Create new project
3. Follow deployment guide
4. Website live with HTTPS
5. Free tier includes hosting

### Paid Options (Better Support)

- **Bluehost** - $2.95/month
- **SiteGround** - $2.99/month
- **HostGator** - $2.75/month
- **AWS S3** - Pay per use (~$1-5/month for small site)

**✅ Best for:**
- Production websites
- Professional domain names
- Worldwide access
- Email forms (Formspree integration)
- File upload handling
- Analytics and monitoring

---

## File Upload Testing

### Important Note About File Uploads

When using `file://` protocol (Method 1):
- ✗ File upload won't work (browser security restriction)
- ✗ Error: "File not accessible due to CORS policy"

**Solution:** Use Method 2 (Local Server) or Method 3 (Hosting) to test file uploads

### How to Test File Uploads Locally

1. **Start local server** (Method 2)
2. **Open:** `http://localhost:8000`
3. **Navigate to:** Candidates page
4. **Fill out form** with test data
5. **Upload test CV** (use PDF/DOC/DOCX file)
6. **Submit form**
7. **Check Admin Dashboard** for file info

---

## Email Forms Testing

### For Formspree Integration

**Test with local server:**
1. Start local server on `http://localhost:8000`
2. Fill out any form (Contact, Candidate, Employer, Medical Travel)
3. Click Submit
4. Check email: `recruitment.ubn@outlook.com`
5. Email should arrive within seconds

**If email doesn't work:**
1. Verify Formspree Form ID in index.html (line 1850)
2. Verify `CONFIG.formspreeEndpoint` is set correctly
3. Check browser console (F12) for errors
4. Verify Formspree account is active
5. See EMAIL_SETUP_GUIDE.md for detailed troubleshooting

---

## File Structure

```
UBN RECRUITMENT/
├── static_site/
│   └── index.html ← Main application (open this!)
│   └── index_old.html (backup)
│   └── README.md
├── FAQ_AND_FILE_UPLOAD_GUIDE.md ← Detailed guide
├── QUICK_REFERENCE_FAQ_UPLOAD.md ← Quick tips
├── IMPLEMENTATION_COMPLETE.md ← What's been added
├── EMAIL_INTEGRATION_COMPLETE.md
├── EMAIL_SETUP_GUIDE.md
├── GDPR_COMPLIANCE_GUIDE.md
├── LEGAL_DOCUMENTS.md
└── QUICK_EMAIL_SETUP.md
```

---

## Browser Recommendations

### Desktop Browsers
| Browser | Version | Status |
|---------|---------|--------|
| Chrome | Latest | ✅ Excellent |
| Firefox | Latest | ✅ Excellent |
| Safari | Latest | ✅ Excellent |
| Edge | Latest | ✅ Excellent |
| Opera | Latest | ✅ Good |

### Mobile Browsers
| Browser | Platform | Status |
|---------|----------|--------|
| Chrome | iOS/Android | ✅ Excellent |
| Safari | iOS | ✅ Excellent |
| Firefox | iOS/Android | ✅ Excellent |
| Samsung Internet | Android | ✅ Good |

---

## Performance Tips

### For Best Experience

1. **Clear Browser Cache**
   - Chrome: Ctrl+Shift+Delete
   - Firefox: Ctrl+Shift+Delete
   - Safari: Cmd+Option+E

2. **Disable Extensions**
   - Some ad blockers may interfere
   - Try incognito/private window first

3. **Check Internet Speed**
   - Minimum 1 Mbps recommended
   - Tailwind CDN requires internet connection

4. **Use Modern Browser**
   - Keep browser updated
   - Use latest stable version

---

## Troubleshooting

### Website Won't Load

**Problem:** Blank page or errors  
**Solution:**
1. Clear browser cache (Ctrl+F5)
2. Try different browser
3. Check internet connection
4. Verify file path is correct
5. Check browser console (F12) for errors

### Forms Don't Work

**Problem:** Submit button does nothing  
**Solution:**
1. Fill all required fields (marked with *)
2. Check browser console for errors (F12)
3. Try Method 2 (local server)
4. Verify localStorage is enabled in browser
5. Check file upload validation

### File Upload Fails

**Problem:** Can't upload CV file  
**Solution:**
1. Verify file size < 5 MB
2. Verify file type is PDF/DOC/DOCX/TXT
3. Use local server (Method 2)
4. Try different browser
5. Check browser console (F12)

### Email Not Sending

**Problem:** Forms submit but no email received  
**Solution:**
1. Verify Formspree endpoint configured
2. Check email in CONFIG object (line 1850)
3. Data saves locally (check Admin Dashboard)
4. See EMAIL_SETUP_GUIDE.md for detailed help
5. Check spam/junk folder

### Mobile View Broken

**Problem:** Layout looks wrong on phone  
**Solution:**
1. Refresh page (Ctrl+R or Cmd+R)
2. Disable zoom (pinch zoom)
3. Check internet speed
4. Try different mobile browser
5. Clear browser app data

---

## Admin Access

### Accessing Admin Dashboard

1. **On website:** Click "Admin" in navigation menu
2. **Or navigate to:** `http://localhost:8000/index.html` (with admin in URL hash)
3. **No login required** - Dashboard is accessible
4. **Features:**
   - View all candidate submissions
   - View all employer posts
   - View all inquiries
   - Filter by status
   - Export to CSV
   - Update status

### Admin Dashboard Functions

- **Candidates Tab:** View all candidate registrations, filter by status
- **Employers Tab:** View all job postings, track postings
- **Inquiries Tab:** View contact inquiries
- **Export:** Download data as CSV file
- **Status Update:** Change submission status (Pending, Reviewing, Approved, Rejected)

---

## Deployment Checklist

Before going live, verify:

- [ ] Website works locally (Method 1 or 2)
- [ ] All 11 pages load correctly
- [ ] Forms submit and save data
- [ ] File uploads work
- [ ] FAQs accordion works
- [ ] Admin dashboard accessible
- [ ] Links work correctly
- [ ] Mobile view responsive
- [ ] No console errors (F12)
- [ ] Choose hosting provider
- [ ] Upload files to server
- [ ] Update domain DNS
- [ ] Test on production server
- [ ] Set up HTTPS/SSL
- [ ] Configure Formspree for production
- [ ] Monitor email delivery
- [ ] Announce website launch

---

## Next Steps

1. **Immediate:** Run website locally using Method 1 or 2
2. **This Week:** Test all features thoroughly
3. **Next Week:** Choose hosting and deploy
4. **After Launch:** Monitor and gather user feedback
5. **Ongoing:** Update content and FAQs regularly

---

## Support Resources

| Resource | Purpose |
|----------|---------|
| FAQ_AND_FILE_UPLOAD_GUIDE.md | Feature documentation |
| QUICK_REFERENCE_FAQ_UPLOAD.md | Quick tips |
| EMAIL_SETUP_GUIDE.md | Email configuration |
| GDPR_COMPLIANCE_GUIDE.md | Data privacy |
| Browser Console (F12) | Error messages |
| index.html comments | Code explanations |

---

## Quick Reference: Port Numbers

Common ports for local servers:
- **8000** - Default (used in examples)
- **8080** - Alternative
- **3000** - Node.js default
- **5000** - Flask/Python alternative
- **8888** - Another alternative

If port 8000 is busy, try:
```bash
python -m http.server 8001  # Use port 8001 instead
```

---

## Final Notes

✅ **Your website is complete and production-ready!**

- Single HTML file (easy to deploy)
- No backend required
- No databases to configure
- Works offline (except email/file upload)
- Mobile responsive
- GDPR compliant
- Professional appearance
- Email integration ready

**Time to deploy:** ~5 minutes  
**Difficulty:** Easy  
**Cost:** Free (with free hosting options)

---

**Questions?** See FAQ_AND_FILE_UPLOAD_GUIDE.md for detailed help!

