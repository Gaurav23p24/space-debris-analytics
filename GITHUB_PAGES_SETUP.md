# GitHub Pages Setup Guide

## Quick Start: Get Your Visualizations Live! 🚀

Follow these steps to publish your interactive visualizations to GitHub Pages.

---

## Step 1: Generate HTML Files

### Option A: Using Google Colab (Recommended)

1. **Open the notebook:**
   - Go to [Google Colab](https://colab.research.google.com/)
   - Upload `GauravPatel_801426641_VA_Project1_Space_Debris (1).ipynb`
   - Upload your `satcat.csv` data file

2. **Run all cells:**
   - Click "Runtime" → "Run all" (or `Ctrl+F9`)
   - Wait for all visualizations to generate

3. **Download HTML files:**
   - Files will be saved in `/content/` folder
   - Files to download:
     - `growth_timeline.html`
     - `regime_dominance.html`
     - `launches_decays_timeline.html`
     - `orbit_3d_visualization_fixed.html`
     - `public_private_stacked_bar.html`
     - `orbit_altitude_pyramid.html`
     - `perigee_apogee_eccentricity.html`

### Option B: Using Jupyter Locally

```bash
# If you haven't already
pip install pandas plotly numpy jupyter

# Run the notebook
jupyter notebook "GauravPatel_801426641_VA_Project1_Space_Debris (1).ipynb"

# Modify paths from /content/ to ./content/ or just use ./
```

---

## Step 2: Upload HTML Files to GitHub

### Using Git (Command Line)

```bash
# Create content directory
mkdir content

# Move your HTML files to the content directory
# (copy them from Colab's /content/ folder)

# Add, commit, and push
git add content/*.html
git commit -m "Add interactive visualization HTML files"
git push origin main
```

### Using GitHub Web Interface

1. Go to your repository: https://github.com/Gaurav23p24/space-debris-analytics
2. Click **"Add file"** → **"Create new file"** or **"Upload files"**
3. Type `content/` in the file path box
4. Upload all 7 HTML files
5. Commit changes

---

## Step 3: Enable GitHub Pages

### Method 1: Automatic (Recommended)

1. Go to your repository on GitHub
2. Click **"Settings"** tab
3. Scroll down to **"Pages"** in the left sidebar
4. Under **"Source"**, select:
   - **Branch:** `main`
   - **Folder:** `/ (root)`
5. Click **"Save"**
6. Wait 1-2 minutes for deployment
7. Your site will be live at: **`https://gaurav23p24.github.io/space-debris-analytics/`**

### Method 2: Using gh-pages branch

```bash
# Create and checkout gh-pages branch
git checkout -b gh-pages

# Copy index.html to root
git checkout main -- index.html

# Push
git push -u origin gh-pages
```

---

## Step 4: Verify Your Site

1. Visit: `https://gaurav23p24.github.io/space-debris-analytics/`
2. You should see:
   - Beautiful landing page
   - 7 visualization cards
   - Click any card to load the interactive visualization
3. Test all 7 visualizations:
   - Growth Timeline
   - Orbit Regime Dominance
   - Launches vs Decays
   - 3D Orbital Distribution ⭐
   - Public vs Private
   - Altitude Pyramid
   - Eccentricity Map

---

## Step 5: Share Your Submission

### For Canvas Submission

**Option 1: Website URL**
```
URL: https://gaurav23p24.github.io/space-debris-analytics/
```

**Option 2: Hybrid (Recommended)**
- Provide the GitHub Pages URL
- Attach the design report as backup
- Mention that notebook is available in repo

---

## Troubleshooting

### Issue: HTML files not loading

**Solution:** Check file paths
- Files should be in `content/` folder
- Check browser console for 404 errors
- Verify filenames match exactly (case-sensitive!)

### Issue: GitHub Pages shows 404

**Solution:** 
- Wait 5-10 minutes after deployment
- Check "Actions" tab for deployment status
- Verify index.html is in root directory

### Issue: Visualizations look broken

**Solution:**
- Check browser console for errors
- Ensure Plotly CDN is loading
- Try a different browser (Chrome recommended)

### Issue: Need to update content

**Solution:**
```bash
# Make changes, then:
git add .
git commit -m "Update visualizations"
git push origin main

# GitHub Pages auto-deploys!
```

---

## File Structure

Your repository should look like this:

```
space-debris-analytics/
├── index.html                              # Main landing page
├── README_Project3.md                      # Documentation
├── Project3_DesignReport_GauravPatel.md    # Design rationale
├── GauravPatel_801426641_VA_Project1_Space_Debris (1).ipynb
├── content/                                # HTML visualizations
│   ├── growth_timeline.html
│   ├── regime_dominance.html
│   ├── launches_decays_timeline.html
│   ├── orbit_3d_visualization_fixed.html
│   ├── public_private_stacked_bar.html
│   ├── orbit_altitude_pyramid.html
│   └── perigee_apogee_eccentricity.html
├── LICENSE
└── .gitignore
```

---

## Bonus: Custom Domain (Optional)

Want a custom URL? Example: `space-debris.yourname.com`

1. Buy a domain (Namecheap, GoDaddy, etc.)
2. Add CNAME file to repository
3. Configure DNS settings
4. See [GitHub Pages custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

---

## Need Help?

- 📖 GitHub Pages Docs: https://pages.github.com/
- 🐛 Report issues on your GitHub repo
- 💬 Stack Overflow: `[github-pages]` tag
- 📧 Email your instructor

---

## Checklist

Before submitting:

- [ ] All 7 HTML files generated and uploaded
- [ ] GitHub Pages enabled and working
- [ ] All visualizations load and are interactive
- [ ] Design report attached to Canvas
- [ ] URL submitted in Canvas text box
- [ ] Tested on mobile device
- [ ] Tested in different browsers

---

**🚀 Your visualizations are now live and ready to share with the world!**

