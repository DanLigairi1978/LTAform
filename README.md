# LT Base Letter & Permit Generator

**Nabalebale Village Elite Suite** — A complete, offline-ready HTML5 application for generating Land Transport (LT) taxi permit applications in Fiji.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue)](https://DanLigairi1978.github.io/lt-permit-generator/) 
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## Overview

This tool consolidates the complete taxi permit application workflow for rural applicants in Fiji, generating a professional **8-page PDF package** containing:

1. **Three Support Letters** (with elevated diction & cultural integration)
   - Turaga ni Mataqali (Chief) — Land authorization
   - Turaga ni Koro (Village Headman) — Provincial endorsement
   - Turaga ni Koro — LTA character certification

2. **Complete LTA Form Replica** (5 pages)
   - Sections A–D with all official fields
   - Auto-population from applicant data
   - Real-time income threshold validation ($30,000 cap)

3. **Interactive Checklists**
   - 16-item Application Packet Requirements
   - 8-item Base Setup & Infrastructure Standards

---

## Features

✅ **Zero Dependencies** — Single HTML5 file, works offline  
✅ **Mobile-First** — Responsive design for Android/iOS  
✅ **GitHub Pages Ready** — Deploy instantly  
✅ **Print-to-PDF** — Generates professional 8-page continuous documents  
✅ **Professional Diction** — Uses culturally appropriate, elevated language  
✅ **Auto-Population** — Enter data once, populate all documents  
✅ **LTA-Compliant** — Exact replica of official New Taxi Permit Application Form  
✅ **Income Validation** — Real-time alerts for the $30,000 household income threshold  

---

## Quick Start

### 1. **Use Online** (Easiest)
Open the live demo: https://DanLigairi1978.github.io/lt-permit-generator/

### 2. **Use Locally** (Offline)
```bash
git clone https://github.com/DanLigairi1978/lt-permit-generator.git
cd lt-permit-generator
python3 -m http.server 8000
# Open http://localhost:8000 in your browser
```

Or simply double-click `index.html` to open in your default browser.

### 3. **Use on Mobile**
- Save the repository to your phone
- Open `index.html` with your mobile browser
- All features work offline; tap "Print" to export as PDF

---

## How to Use

### Step 1: Enter Applicant Data
1. Click the **"Applicant Data"** tab
2. Fill in:
   - Applicant's full name & surname
   - Vehicle make & model
   - Proposed base location
   - Mataqali (land owner) name
   - Village chief details & contact
   - Village headman name
   - Village meeting date
3. Click **"Load Example Data"** to see how it works

### Step 2: Review Checklists
1. Click the **"Checklists"** tab
2. Check off items as you gather documents:
   - Application Packet (police clearance, medical, birth cert, etc.)
   - Base Setup Standards (12m² office, toilet facilities, parking, etc.)
3. Print checklists for your records

### Step 3: Generate Support Letters
1. Click the **"Support Letters"** tab
2. Click **"Update Letters with Data"** to populate from Step 1
3. Review the three letters
4. Click **"Print All Letters (PDF)"** to save as PDF

### Step 4: Complete LTA Form
1. Click the **"LTA Form"** tab
2. Click **"Auto-fill Form from Applicant Data"** to pre-populate basic fields
3. Complete remaining fields manually (financial details, vehicle specs, etc.)
4. Watch for **income threshold warnings** (must be ≤ $30,000)
5. Click **"Print Complete Application (PDF)"** to generate final form

### Step 5: Submit
- Combine all PDFs (3 letters + LTA form + supporting docs)
- Lodge with Land Transport Authority, Suva

---

## File Structure

```
lt-permit-generator/
├── index.html              # Main application (50 KB)
├── images/
│   ├── letterhead.png      # Nabalebale Village letterhead
│   ├── don-signature.png   # Turaga ni Koro (Antonio) signature
│   └── tm-signature.png    # Turaga ni Mataqali (Chief) signature
├── README.md               # This file
├── LICENSE                 # MIT License
└── DEPLOYMENT.md           # GitHub Pages setup guide
```

---

## Customization

### Update Village/Chief Names
Edit `index.html` and search for:
- `Nabalebale Village` → Replace with your village
- Letterhead address → Update to your location
- Chief/headman names → Replace with your leaders

### Update Signatures
1. Replace image files in `/images/`:
   - `letterhead.png` — Your village letterhead (PNG, any size)
   - `don-signature.png` — Village headman's digital signature
   - `tm-signature.png` — Mataqali chief's digital signature
2. Keep filenames the same; `index.html` will automatically reference them

### Change LTA Requirements
Checklists are hardcoded based on official LTA documentation. To update:
1. Search for `<div class="checklist">` in `index.html`
2. Add/remove `<div class="checklist-item">` blocks as needed
3. Update descriptions to match current LTA requirements

---

## Technical Details

**Built with:**
- HTML5 (semantic structure)
- CSS3 (responsive grid layout, print styles)
- Vanilla JavaScript (zero frameworks, no dependencies)

**Browser Support:**
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile Safari (iOS 14+)
- Chrome Android 90+

**Performance:**
- Load time: <1 second
- File size: 50 KB (HTML only; +3×PNG images ~150 KB)
- Works 100% offline after initial load

**Accessibility:**
- WCAG 2.1 Level AA compliant
- Semantic HTML labels and form groups
- High contrast (dark text on light background)
- Keyboard navigable

---

## Troubleshooting

### Images not showing
- Ensure `/images/` folder exists in the same directory as `index.html`
- Check that filenames match:
  - `letterhead.png`
  - `don-signature.png`
  - `tm-signature.png`
- If hosting on GitHub Pages, ensure images are committed and pushed

### PDF print quality
- Use **Print Preview** (Ctrl+P / Cmd+P) before printing
- Set margins to **Minimal** or **None**
- Disable "Print headers and footers"
- Save as PDF (recommended) rather than printing to paper

### Form fields not populating
- Ensure you've filled the **"Applicant Data"** tab completely
- Click **"Update Letters with Data"** or **"Auto-fill Form"** buttons
- Check browser console (F12 → Console) for errors

### Income threshold alert not triggering
- Make sure income field in **Section B** is filled
- Income must be entered as a number (no $ or commas)
- Alert appears when income exceeds $30,000

---

## Contributing

Found a bug? Have a suggestion?
1. Open an issue on GitHub
2. Provide screenshots if possible
3. Describe the steps to reproduce

**Note:** This tool follows official LTA New Taxi Permit Application requirements as of 2025. Check with the LTA if requirements change.

---

## License

MIT License — See [LICENSE](LICENSE) file for details.

You are free to:
- Use this tool for personal or commercial purposes
- Modify and customize for your needs
- Redistribute with attribution
- Adapt for other provinces or regions

---

## Support

**Questions?** 
- Check the **"Applicant Data"** tab for field descriptions
- Review the **"Checklists"** tab for LTA requirements
- Print the PDF previews to verify formatting

**Want to adapt this for another region?**
- Fork the repo
- Update village names, chief details, and letterhead
- Customize checklists for your local LTA requirements
- Submit a pull request to add your region

---

## Acknowledgments

Built for **Meridian Solutions PTE Ltd** to support grassroots tourism operators and community development in Fiji.

Developed with guidance from official LTA documentation and consultation with Nabalebale Village leadership.

---

**Version:** 1.0  
**Last Updated:** April 2026  
**Fiji Land Transport Authority Compliance:** Verified ✓

---

### Quick Links

- 🌐 **Live Demo:** https://DanLigairi1978.github.io/lt-permit-generator/
- 📖 **GitHub Repo:** https://github.com/DanLigairi1978/lt-permit-generator
- 📋 **LTA Official:** https://www.lta.org.fj
- 🏢 **Meridian Solutions:** Nabalebale Village, Cakaudrove, Fiji
