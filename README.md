# Digital QR Menu Card

A clean, modern, mobile-first QR menu card powered directly by **Google Sheets** (or a local CSV).

---

## 📁 Files Included
- **`index.html`**: The complete single-page digital menu application.
- **`menu.csv`**: Sample menu spreadsheet format.

---

## ⚡ How to Connect Your Google Sheet

1. Open **[Google Sheets](https://sheets.new)**.
2. Go to **File** > **Import** > **Upload** and upload `menu.csv` (or manually create columns: `Category`, `Name`, `Description`, `Price`, `Badge`).
3. Fill in your dishes and prices.
4. Click **File** > **Share** > **Publish to web**.
5. In the popup:
   - Select your tab (e.g. `Sheet1` or `Menu`).
   - Change "Web page" to **Comma-separated values (.csv)**.
   - Click **Publish**.
6. Copy the generated link (it looks like: `https://docs.google.com/spreadsheets/d/e/2PACX-.../pub?output=csv`).
7. Open `index.html` in any text editor and paste the link into line 80:
   ```javascript
   const GOOGLE_SHEET_CSV_URL = "PASTE_YOUR_GOOGLE_SHEETS_CSV_URL_HERE";
   ```
8. Update your restaurant branding, Instagram, and Google Review links on lines 83-91:
   ```javascript
   const RESTAURANT_NAME = "Your Cafe / Restaurant";
   const RESTAURANT_TAGLINE = "Artisanal Kitchen & Bar";
   const CURRENCY_SYMBOL = "₹";
   
   // Links (leave as "" if you want to hide them)
   const INSTAGRAM_URL = "https://instagram.com/yourhandle";
   const INSTAGRAM_HANDLE = "@yourhandle";
   const GOOGLE_REVIEW_URL = "https://g.page/r/your-google-review-link/review";
   ```

Now, whenever you add, remove, or edit dishes/prices in your Google Sheet, the menu website will update automatically!

---

## 🚀 How to Host It Online for Free (Takes 2 Minutes)

You can host this website completely free with global speed and free SSL (HTTPS):

### Option 1: Vercel (Recommended)
1. Go to [vercel.com](https://vercel.com) and sign in.
2. Drag and drop the `D:\WORK\CODES\MENU` folder directly onto the Vercel dashboard.
3. You will get an instant live link like `https://your-cafe-menu.vercel.app`.

### Option 2: Netlify Drop
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag and drop the `D:\WORK\CODES\MENU` folder.
3. Your site is live immediately with a free HTTPS URL.

---

## 📱 Generating Your QR Codes

1. Copy your live website URL (e.g. `https://your-cafe-menu.vercel.app`).
2. If you want **Table-specific QR codes**, simply add `?table=1`, `?table=2`, etc. to the end of the URL:
   - `https://your-cafe-menu.vercel.app/?table=1`
   - `https://your-cafe-menu.vercel.app/?table=2`
3. Generate high-resolution print QR codes using free tools like [qr-code-generator.com](https://www.qr-code-generator.com/) or [Canva](https://www.canva.com/).
4. Print your acrylic table tents or table stickers!
