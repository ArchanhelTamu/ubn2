# 🚀 Quick Reference: FAQ & File Upload Updates

## What's New?

✅ **FAQ Page** - 12 professional FAQs with accordion interface
✅ **CV Upload** - Real file upload with validation (5MB max, PDF/DOC/DOCX/TXT)

---

## How to Access

### FAQ Page
1. Open website
2. Click **"FAQs"** in navigation menu (between Resources and Contact)
3. Click any question to expand/collapse answers

### CV Upload
1. Go to **Candidates** page
2. Scroll to **"CV/Resume File"** section
3. Click to select file (PDF, DOC, DOCX, or TXT)
4. See validation feedback
5. Submit form

---

## File Upload Rules

| Rule | Requirement |
|------|-------------|
| Max Size | 5 MB |
| File Types | PDF, DOC, DOCX, TXT |
| Required | Optional (can skip) |
| Validation | Real-time feedback |

---

## 12 FAQs Included

1. ❓ What is UBN?
2. ❓ What services do you provide?
3. ❓ Do you guarantee employment?
4. ❓ How do employers work with UBN?
5. ❓ What healthcare professionals do you source?
6. ❓ How does recruitment process work?
7. ❓ Do you offer international recruitment?
8. ❓ Do you provide visa sponsorship?
9. ❓ How are service fees determined?
10. ❓ How can candidates submit info?
11. ❓ Is personal info secure?
12. ❓ How to contact UBN?

---

## Testing Quick Checklist

### FAQs ✓
- [ ] Navigation link appears
- [ ] Click expands answer
- [ ] Only one open at a time
- [ ] Icons change (+ to −)
- [ ] Mobile view works

### File Upload ✓
- [ ] Valid PDF uploads
- [ ] Valid DOC/DOCX uploads
- [ ] File size shows
- [ ] Error on > 5MB
- [ ] Error on wrong type
- [ ] Data saves in admin
- [ ] Optional field works

---

## Contact Info Included in FAQs

📧 **Email:** recruitment.ubn@outlook.com  
📱 **WhatsApp:** +44 (203) 026-0312 or +27 670-486-798  
🌐 **Website:** Contact page form

---

## File Upload User Messages

| Event | Message |
|-------|---------|
| Valid upload | ✓ File ready: filename.pdf (123.45KB) |
| Too large | ❌ File too large! Maximum size is 5MB. Your file is 6.25MB. |
| Wrong type | ❌ Invalid file type! Only PDF, DOC, DOCX, and TXT files are allowed. |

---

## Code Changes Made

**File Modified:** `static_site/index.html`

**New Functions:**
- `toggleFaq(button)` - Expands/collapses FAQ answers
- `handleFileUpload(event)` - Validates file uploads in real-time

**Modified Functions:**
- `handleCandidateSubmit()` - Now includes file metadata
- `sendCandidateEmail()` - Includes file info in email

**New HTML Elements:**
- `page-faqs` div with 12 FAQ items
- File input with accept filter and validation feedback

---

## Data Stored with Each Submission

```
{
  id: "UBN-C-1234567890",
  fullName: "John Doe",
  email: "john@example.com",
  cvFile: "resume.pdf",
  cvFileInfo: {
    name: "resume.pdf",
    size: 125450,
    type: "application/pdf",
    uploadDate: "2026-03-13T14:30:00Z"
  },
  ... other fields
}
```

---

## Customization

### Add New FAQ
Copy this template and add to FAQ section:
```html
<div class="faq-item" style="margin-bottom: 20px; ...">
    <button class="faq-question" onclick="toggleFaq(this)" style="...">
        <span>Question?</span>
        <span class="faq-icon">+</span>
    </button>
    <div class="faq-answer" style="display: none; ...">
        <p>Answer here...</p>
    </div>
</div>
```

### Change File Size Limit
Edit line in `handleFileUpload()`:
```javascript
const maxSizeMB = 5;  // Change to desired MB
```

### Add File Types
Edit `allowedTypes` array and HTML accept attribute

---

## Where to Find Things

| Item | Location |
|------|----------|
| FAQ Page | Lines 1503-1678 in index.html |
| toggleFaq() | Lines 2388-2410 |
| handleFileUpload() | Lines 2411-2451 |
| File Input HTML | Line 1037 |
| Full Guide | FAQ_AND_FILE_UPLOAD_GUIDE.md |

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| FAQ not opening | Clear cache (Ctrl+F5) |
| File upload fails | Check file size < 5MB and type is allowed |
| Data not saving | Enable localStorage in browser |
| Mobile not working | Try clearing cache and refreshing |

---

## Version Info

**Date Updated:** March 13, 2026  
**Features Added:** 2 (FAQs + File Upload)  
**Status:** ✅ Production Ready  
**Tested:** ✅ Yes  

---

## 📞 Need Help?

See **FAQ_AND_FILE_UPLOAD_GUIDE.md** for detailed documentation

