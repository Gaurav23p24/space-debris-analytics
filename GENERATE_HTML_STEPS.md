# 📊 Step-by-Step: Generate HTML Files in Google Colab

## Complete Walkthrough

Follow these steps to generate all your visualization HTML files.

---

## Step 1: Open Google Colab

1. Go to **https://colab.research.google.com/**
2. Sign in with your Google account

---

## Step 2: Upload Your Notebook

1. Click **"File" → "Upload notebook"**
2. Upload: `GauravPatel_801426641_VA_Project1_Space_Debris (1).ipynb`
3. Wait for it to upload and open

---

## Step 3: Upload Your Data File

**Option A: Upload from Files (Recommended)**

1. Click the **folder icon** on the left sidebar (📁 Files)
2. Click **"Upload to session storage"** button
3. Select your `satcat.csv` file
4. Wait for upload to complete

**Option B: Mount Google Drive**

If your file is in Google Drive:
```python
from google.colab import drive
drive.mount('/content/drive')
# Then point to: /content/drive/MyDrive/your_file.csv
```

---

## Step 4: Verify Data Upload

1. In the notebook, find the cell that uploads data:
```python
from google.colab import files
uploaded = files.upload()
df = pd.read_csv("satcat.csv")
```

2. If data already uploaded, skip the upload cell

---

## Step 5: Run All Cells

**Method 1: Run All at Once (Recommended)**
1. Click **Runtime → Run all** (or press `Ctrl+F9`)
2. Wait for all cells to execute (this takes 2-5 minutes)
3. Watch the output to see progress

**Method 2: Run Individual Cells**
1. Click each cell
2. Press **Shift + Enter** to run
3. Continue until all are done

---

## Step 6: Check for Output Messages

Look for these messages as cells run:

```
✅ Saved: /content/launches_decays_timeline.html
✅ Saved: /content/orbit_3d_visualization_fixed.html
✅ Saved: /content/public_private_stacked_bar.html
✅ Saved: /content/orbit_altitude_pyramid.html
✅ Saved: /content/perigee_apogee_eccentricity.html
```

**Note:** If you only see 5 HTML files, that's okay! Some visualizations might not have HTML export code yet.

---

## Step 7: Add HTML Export for Missing Visualizations

If you notice some visualizations don't have HTML export, you can add it manually.

### For Growth Timeline (V1)

Find the cell that creates the growth timeline chart. After `fig.show()`, add:

```python
# Save as HTML
fig.write_html("/content/growth_timeline.html", include_plotlyjs="cdn", full_html=True)
print("Saved: /content/growth_timeline.html")
```

### For Regime Dominance (V2)

Find the cell that creates the regime dominance chart. After `fig.show()`, add:

```python
# Save as HTML
fig.write_html("/content/regime_dominance.html", include_plotlyjs="cdn", full_html=True)
print("Saved: /content/regime_dominance.html")
```

---

## Step 8: Verify Files Created

1. Click the **folder icon** (📁 Files) on the left
2. Navigate to the **`content`** folder
3. You should see files like:
   - `growth_timeline.html`
   - `regime_dominance.html`
   - `launches_decays_timeline.html`
   - `orbit_3d_visualization_fixed.html`
   - `public_private_stacked_bar.html`
   - `orbit_altitude_pyramid.html`
   - `perigee_apogee_eccentricity.html`

---

## Step 9: Download All HTML Files

**Method 1: Download All at Once (Recommended)**

1. Right-click on the **`content`** folder
2. Click **"Download"**
3. Save the ZIP file to your computer
4. Extract the ZIP to get all HTML files

**Method 2: Download Individually**

1. Right-click each HTML file
2. Click **"Download"**
3. Save to a folder on your computer

---

## Step 10: Verify Downloads

1. Open the folder where you saved the files
2. You should have **7 HTML files**:
   - `growth_timeline.html` ✅
   - `regime_dominance.html` ✅
   - `launches_decays_timeline.html` ✅
   - `orbit_3d_visualization_fixed.html` ✅
   - `public_private_stacked_bar.html` ✅
   - `orbit_altitude_pyramid.html` ✅
   - `perigee_apogee_eccentricity.html` ✅

3. Double-click one to open it in a browser and verify it works

---

## ⚠️ Troubleshooting

### Issue: "ModuleNotFoundError: No module named 'plotly'"

**Solution:**
```python
!pip install plotly pandas numpy
```
Run this in a new cell, then restart runtime: **Runtime → Restart runtime**

### Issue: "File not found: satcat.csv"

**Solution:**
- Make sure you uploaded the file correctly (Step 3)
- Check the file name matches exactly
- Verify the file is in the current directory

### Issue: "Only 5 HTML files generated instead of 7"

**Solution:**
- This is normal if the notebook doesn't have export code for all visualizations
- Add the export code manually (see Step 7)
- Or just upload the 5 files you have - that's still great!

### Issue: "Colab session disconnected"

**Solution:**
- Your files might be lost! Re-run from Step 5
- Consider upgrading to Colab Pro for longer sessions
- Or download files immediately after generation

### Issue: "Files won't download"

**Solution:**
- Try downloading individually instead of as a folder
- Use the right-click menu
- Check your browser's download settings

---

## 📝 Quick Checklist

Before moving to the next step (uploading to GitHub):

- [ ] Notebook opened in Colab
- [ ] Data file (satcat.csv) uploaded
- [ ] All cells ran successfully
- [ ] At least 5 HTML files generated
- [ ] All HTML files downloaded to my computer
- [ ] Tested opening one HTML file in browser

---

## ⏭️ Next Steps

Once you have all HTML files:

1. **Go to:** https://github.com/Gaurav23p24/space-debris-analytics
2. **Upload files** to the `content/` folder
3. **Enable GitHub Pages**
4. **Submit your URL to Canvas!**

See **QUICK_START.md** for the full process!

---

## 🎯 Time Estimate

- **Step 1-4:** 2 minutes (uploading files)
- **Step 5-7:** 5-10 minutes (running notebook)
- **Step 8-10:** 2 minutes (downloading files)

**Total: ~10 minutes** ⏱️

---

## 🆘 Still Need Help?

If you're stuck:
1. Check the notebook output for error messages
2. Make sure your internet connection is stable
3. Try refreshing Colab and starting over
4. Verify the notebook file isn't corrupted
5. Check that you have enough Colab storage space

**Good luck! You've got this!** 🚀

