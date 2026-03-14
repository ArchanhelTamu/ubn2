# Ultimate Baby Nurses - Healthcare Recruitment Website

A professional, responsive healthcare staffing and recruitment platform connecting skilled healthcare professionals with global opportunities.

## 🌐 Quick Start

### Option 1: Direct File Opening
Simply open the `index.html` file in your web browser:
```
file:///c:/Users/Administrator/Documents/websites/UBN%20RECRUITMENT/static_site/index.html
```

### Option 2: Local HTTP Server (Recommended)
If you have Python installed, run:
```bash
cd c:\Users\Administrator\Documents\websites\UBN RECRUITMENT\static_site
python -m http.server 8000
```
Then open `http://localhost:8000` in your browser.

For Node.js users:
```bash
npx http-server .
```

## ✨ Features

### 8 Main Pages
- **Home** - Hero section with statistics, services overview, testimonials
- **About** - Company mission, values, team information
- **Candidates** - Registration form for healthcare professionals
- **Candidate Portal** - Login portal for existing candidates
- **Employers** - Job posting form for healthcare institutions
- **Medical Travel** - Medical travel & patient concierge services consultation
- **Resources** - Blog posts, guides, and professional development materials
- **Contact** - Contact form and company information
- **Terms of Service** - Legal terms governing website and services use
- **Privacy Policy** - Data protection and privacy information
- **Admin Dashboard** - Management system for all submissions

### 3 Main Forms
1. **Candidate Registration**
   - Full name, country, email, WhatsApp
   - Healthcare profession selection
   - Years of experience
   - Current employer
   - Skills and availability
   - Preferred locations
   - CV file upload
   - Terms acceptance

2. **Employer Job Posting**
   - Company information
   - Contact details
   - Healthcare role required
   - Staff count needed
   - Required skills
   - Visa sponsorship options

3. **Contact Form**
   - Sender information
   - User type selection
   - Message submission

4. **Medical Travel Inquiry** (NEW)
   - Patient full name
   - Country of origin
   - Destination hospital/city
   - Medical needs/treatment type
   - Preferred travel dates
   - Contact information
   - Additional requirements
   - Pre-launch service notice

### Admin Dashboard
- **Tab System** - Switch between Candidates, Employers, and Contact Inquiries
- **Statistics** - Real-time counts of submissions
- **Filtering** - Search by name/email, filter by profession, filter by status
- **Status Management** - Update status (Pending, Reviewed, Shortlisted)
- **CSV Export** - Download data for analysis

## 🎨 Design Features
- **Responsive Layout** - Works perfectly on desktop, tablet, and mobile
- **Professional Colors** - Medical-inspired blues and pastels
- **Modern Typography** - Playfair Display for headings, Source Sans 3 for body
- **Smooth Animations** - Fade-in, float, and pulse effects
- **Accessible Forms** - Clear labels, proper validation, helpful tooltips

## 💾 Data Storage
- **Local Storage** - Form submissions are saved locally in your browser
- **No Backend Required** - Works completely offline
- **Persistent Data** - Data persists even after closing the browser
- **CSV Export** - Export all data for backup or analysis

## � Email Notifications
- **All forms send email** to recruitment.ubn@outlook.com automatically
- **Instant notifications** when submissions received
- **Professional email formatting** with all submission details
- **Formspree integration** for reliable email delivery
- **Fallback system** - Data saved locally even if email fails
- **See EMAIL_SETUP_GUIDE.md** for complete setup instructions

## �📱 Mobile Responsive
- Hamburger menu for navigation on mobile devices
- Touch-friendly buttons and forms
- Optimized layout for all screen sizes
- Fast loading on mobile networks

## 🏥 Medical Travel & Patient Concierge Service

### What We Offer
Ultimate Baby Nurses provides **Medical Travel & Patient Concierge Services** - a comprehensive coordination service for patients seeking international medical treatment. 

### Services Coordinated
- **Licensed Caregiver Escorts** - Professional caregivers accompany patients throughout their journey
- **Hospital Coordination** - Pre-admission planning and appointment scheduling
- **Transport Arrangements** - Ground and air transport with reliable providers
- **Visa & Documentation** - Travel and medical visa guidance
- **Travel Planning** - Complete itineraries considering medical and rest schedules
- **24/7 Support** - Emergency assistance throughout the journey

### Service Status
⏳ **Pre-Launch Phase**: Currently offering consultation and planning services while completing business registration and licensing requirements. Full service coordination will be available upon licensing completion.

### How to Use
1. Navigate to the **Medical Travel** page
2. Fill out the inquiry form with:
   - Medical needs and treatment type
   - Preferred destination hospital
   - Travel dates
   - Contact information
3. Submit for a personalized consultation
4. Our team will contact you within 24 hours

### Data Management
- Medical travel inquiries are stored separately in LocalStorage
- Admin dashboard tracks all medical travel submissions
- All data is handled with confidentiality

## ⚖️ Legal & Compliance

### Terms of Service
- Comprehensive legal terms governing use of website and services
- Clearly outlines scope of services, liability limitations, and responsibilities
- Accessible via "Terms of Service" link in footer
- **Key sections:**
  - About Ultimate Baby Nurses
  - Scope of services (recruitment support, candidate screening, coordination)
  - No employment guarantee
  - Candidate and client responsibilities
  - Service fees and payment terms
  - Independent service provider status
  - Limitation of liability
  - Confidentiality agreements

### Privacy Policy
- **GDPR-compliant** privacy documentation for UK and international compliance
- Protects user data collection (CVs, names, emails, phone numbers)
- Establishes legitimacy with UK healthcare companies
- **Key sections:**
  - Information collection practices
  - Data usage and processing
  - Third-party sharing policies
  - Data security measures
  - User rights and data retention
  - Cookie usage
  - Contact for data access requests

### Why This Matters
- ✅ UK healthcare organizations require GDPR compliance
- ✅ Clear terms protect you from liability
- ✅ Privacy policy required when collecting personal/sensitive data
- ✅ Increases trust and professional credibility
- ✅ Legally defensible in case of disputes

## 🔧 Technical Stack
- **Frontend**: HTML5, CSS3, JavaScript
- **Framework**: Tailwind CSS 3.4.17 (via CDN)
- **Typography**: Google Fonts
- **Storage**: Browser LocalStorage
- **No Dependencies**: Runs completely standalone

## 📊 Admin Access
Access the Admin Dashboard:
1. Click "Admin" in the navigation menu
2. View all form submissions
3. Filter by status, profession, or search term
4. Update submission status
5. Export data as CSV

### Default Admin Access
- The admin dashboard is publicly accessible (no authentication currently)
- Future: Implement admin login and authentication

## 🚀 Deployment Options

### Option 1: Static Web Host
Upload the entire `static_site/` folder to:
- GitHub Pages
- Netlify
- Vercel
- AWS S3
- Any static hosting service

### Option 2: Traditional Web Server
- Apache
- Nginx
- IIS
- Any HTTP server

### Option 3: Node.js Server
```javascript
const express = require('express');
const app = express();
app.use(express.static('static_site'));
app.listen(3000, () => console.log('Server running on port 3000'));
```

## 📈 Future Enhancements
- [ ] Backend API integration
- [ ] Database for persistent storage
- [ ] User authentication and login
- [ ] Email notifications on form submission
- [ ] File upload for CVs and documents
- [ ] Payment processing for premium features
- [ ] Video interview integration
- [ ] Real-time notifications
- [ ] Multi-language support
- [ ] Advanced analytics

## 📞 Contact Information
- **Email**: recruitment.ubn@outlook.com
- **Phone**: +44 (203) 026-0312
- **WhatsApp**: +27 670-486-798

**Recruitment & Talent Acquisition Manager**: Thuli Mlalazi

## 📄 Features Checklist
✅ 8 fully functional pages
✅ 3 comprehensive forms
✅ Admin dashboard with filtering and export
✅ Responsive design
✅ Toast notifications
✅ Local data persistence
✅ Professional UI/UX
✅ Mobile-optimized
✅ Accessible forms
✅ SEO-friendly structure
✅ Fast loading
✅ No external dependencies (except CDN)

## 🎯 Browser Support
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📝 License
All rights reserved © 2024 Ultimate Baby Nurses

## ✉️ Support
For issues or feature requests, contact: support@ultimababenurses.com

---

**Website Status**: ✓ Ready for Production
**Last Updated**: 2024
**Version**: 1.0
