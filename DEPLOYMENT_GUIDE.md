# GitHub Deployment Checklist

## BEFORE You Start

You have two smart choices:

### ✅ OPTION 1: Create NEW Repo (Recommended)
- **Best for:** Keeping LT Permit Generator as its own clean, focused tool
- **URL:** https://github.com/DanLigairi1978/lt-permit-generator
- **Live site:** https://DanLigairi1978.github.io/lt-permit-generator/
- **Benefit:** Easy to maintain, share, and adapt for other regions

### ❌ OPTION 2: Use Existing MeridianVXP01 Repo (Not Recommended)
- **Only if:** This becomes the main Meridian Solutions public tool
- **Problem:** Mixes LT tool with other Meridian projects
- **Better approach:** Keep separate, then link from main Meridian site later

---

## QUICK START COMMANDS

### Setup (One-time, ~2 minutes)

**On GitHub Web:**
1. Go to github.com
2. Click **"New Repository"**
3. Name: `lt-permit-generator`
4. Description: "LT Base Letter & Permit Generator | Nabalebale Elite Suite"
5. Choose **Public**
6. Initialize with **README.md**
7. Click **"Create Repository"**

**On Your Computer:**
```bash
# Clone the repo
git clone https://github.com/DanLigairi1978/lt-permit-generator.git
cd lt-permit-generator

# Remove default README (we'll replace it)
rm README.md

# Download the files I created
# Option A: Copy from Claude output
cp /path/to/index.html .
cp /path/to/README.md .
cp /path/to/.gitignore .

# Option B: Or download direct from outputs folder you received
```

### Add Your Images (~1 minute)

```bash
# Create images folder
mkdir images

# Copy your PNG files (rename them as you add)
cp /path/to/Nabalebale_letterhead.png images/letterhead.png
cp /path/to/Don_sign.png images/don-signature.png
cp /path/to/TM_sign.png images/tm-signature.png
```

**Your folder structure should look like:**
```
lt-permit-generator/
├── index.html
├── README.md
├── .gitignore
└── images/
    ├── letterhead.png
    ├── don-signature.png
    └── tm-signature.png
```

### Commit & Push (~1 minute)

```bash
# Add all files to staging
git add .

# Commit with a message
git commit -m "Initial commit: LT Permit Generator with images and documentation"

# Push to GitHub
git push origin main
```

### Enable GitHub Pages (~1 minute)

1. Go to your repo: https://github.com/DanLigairi1978/lt-permit-generator
2. Click **Settings** (top right)
3. Click **Pages** (left sidebar, under "Code and automation")
4. Under "Source", select:
   - Branch: **main**
   - Folder: **/ (root)**
5. Click **Save**
6. Wait 30 seconds for deployment
7. Your site is live at: **https://DanLigairi1978.github.io/lt-permit-generator/**

---

## DETAILED CHECKLIST

### Pre-Deployment
- [ ] You have `index.html` (the LT Permit Generator app)
- [ ] You have `Nabalebale_letterhead.png`, `Don_sign.png`, `TM_sign.png`
- [ ] You have `README.md` (I created this)
- [ ] You have `.gitignore` (I created this)
- [ ] Git is installed on your machine (`git --version`)
- [ ] You have a GitHub account

### Local Setup
- [ ] Created `lt-permit-generator` folder locally
- [ ] Run: `git clone https://github.com/DanLigairi1978/lt-permit-generator.git`
- [ ] Copy `index.html` into the folder
- [ ] Copy `README.md` into the folder
- [ ] Copy `.gitignore` into the folder
- [ ] Created `/images` subfolder
- [ ] Renamed and copied your PNGs:
  - [ ] `Nabalebale_letterhead.png` → `images/letterhead.png`
  - [ ] `Don_sign.png` → `images/don-signature.png`
  - [ ] `TM_sign.png` → `images/tm-signature.png`

### Test Locally
- [ ] Open Terminal/Command Prompt in the folder
- [ ] Run: `python3 -m http.server 8000`
- [ ] Open: http://localhost:8000
- [ ] Verify:
  - [ ] Images display correctly (letterhead, signatures)
  - [ ] "Load Example Data" button works
  - [ ] Letters populate with data
  - [ ] Form fields auto-fill
  - [ ] Print preview looks good

### Push to GitHub
- [ ] Run: `git add .`
- [ ] Run: `git commit -m "Initial commit: LT Permit Generator with images and docs"`
- [ ] Run: `git push origin main`
- [ ] Check https://github.com/DanLigairi1978/lt-permit-generator — files are there ✓

### Enable Pages
- [ ] Go to repo Settings → Pages
- [ ] Set Source to: **main** branch, **/ (root)** folder
- [ ] Click Save
- [ ] Wait 30-60 seconds for GitHub to deploy
- [ ] Visit: https://DanLigairi1978.github.io/lt-permit-generator/
- [ ] Verify app loads and images display ✓

### Post-Launch
- [ ] Test on mobile: Open URL on phone, ensure responsive ✓
- [ ] Test print-to-PDF: Generate sample documents ✓
- [ ] Share URL with stakeholders (chiefs, LTA staff, etc.)
- [ ] Add to your portfolio/LinkedIn as a tool you created

---

## QUESTIONS & ANSWERS

**Q: Can I rename it to something shorter?**  
A: Yes! Instead of `lt-permit-generator`, use:
- `lt-app`
- `permit-gen`
- `nabalebale-app`

Just make sure it's lowercase with hyphens (GitHub Pages preference).

**Q: Do I HAVE to include the image files?**  
A: **No, but recommended.** Two options:

1. **INCLUDE FILES** (What I've set up):
   - Pro: Easy to update signatures later
   - Pro: Smaller HTML file (50 KB vs. 400 KB)
   - Con: Need `/images` folder in repo
   - Size: ~150 KB total (letterhead + 2 signatures)

2. **EMBED IN HTML** (Alternative):
   - Pro: Single file, no dependencies
   - Con: Larger HTML file (~400 KB)
   - Con: Harder to update signatures
   - How: Convert PNGs to Base64, paste into HTML

**Recommendation:** Keep the `/images/` approach I've set up. It's cleaner and more professional.

**Q: Can I delete the old MeridianVXP01 repo content?**  
A: No, don't do that. Keep them separate. You can:
- Link from MeridianVXP01 to lt-permit-generator repo
- Use lt-permit-generator as a standalone tool
- Deploy both independently

**Q: How do I update signatures later?**  
A: Just replace the PNG files:
1. Save new signature as `don-signature.png` or `tm-signature.png`
2. Drop into `/images/` folder (overwrite old file)
3. Commit & push: `git add . && git commit -m "Update signatures" && git push`
4. GitHub Pages auto-updates in ~30 seconds

**Q: Will my village leaders' signatures be visible to the public?**  
A: Yes, if you include image files. The repo is public, so anyone can see them. If privacy is a concern:
- Embed signatures as Base64 in HTML (single file, private)
- Or use `.gitignore` to exclude `/images/` and regenerate locally

**Q: Can I make the repo private?**  
A: Yes, but then GitHub Pages won't work (private repos need paid Plans for Pages). Better to keep public—it's your service to the community!

---

## TROUBLESHOOTING

### "git: command not found"
Install Git: https://git-scm.com/download

### "fatal: not a git repository"
Make sure you're in the repo folder:
```bash
cd /path/to/lt-permit-generator
git status  # Should show branch and files
```

### Images not showing after pushing
1. Check that `/images/` folder is committed:
   ```bash
   git ls-files | grep images
   # Should show: images/letterhead.png, etc.
   ```
2. If not, run:
   ```bash
   git add images/
   git commit -m "Add image files"
   git push origin main
   ```

### Pages deployment stuck or erroring
1. Check repo Settings → Pages for any error messages
2. Ensure `/images/` folder is committed (see above)
3. Wait 1-2 minutes and refresh
4. If still stuck, disable then re-enable Pages

### Site loads but images are broken (404 errors)
- Check browser console (F12 → Console)
- Verify image filenames in `/images/` match exactly
- Check `index.html` image `src` attributes
- If needed, update `src="images/letterhead.png"` to match your actual filenames

---

## FINAL CHECKLIST BEFORE SHARING

Before you share the URL with village leaders, chiefs, and the LTA:

- [ ] Test on a computer (Chrome, Firefox, Safari)
- [ ] Test on a phone (Android Chrome, iOS Safari)
- [ ] Load example data and generate a test PDF
- [ ] Print a test page—verify formatting is correct
- [ ] Verify letterhead appears at the top of letters
- [ ] Verify signatures appear at bottom of letters
- [ ] Check that all form fields are there and working
- [ ] Test income threshold warning (enter amount > $30,000)
- [ ] Confirm print-to-PDF creates all 8 pages
- [ ] Share URL: https://DanLigairi1978.github.io/lt-permit-generator/

---

## NEED HELP?

If anything breaks:
1. Check this checklist for the exact error
2. Run: `git status` to see what files have changed
3. Run: `git log --oneline` to see commit history
4. Worst case: Delete everything, re-clone, and start over (you won't lose GitHub data)

---

**Good luck, buddy! 🎯**

Once live, this tool will save Nabalebale applicants hours of paperwork. Your village will love it.
