# 🔄 Cross-Device Product Sync Setup

## Problem
Products added on one device are not showing on other devices because they're stored in localStorage (device-specific).

## Solution
Use JSONBin.io (Free) to sync products across all devices.

---

## ⚡ Quick Setup (5 Minutes)

### Step 1: Create JSONBin.io Account
1. Go to **https://jsonbin.io/**
2. Click **Sign Up** (Free account)
3. Create account with email or GitHub

### Step 2: Create a Bin
1. After login, click **"Create Bin"**
2. Name: `SM_LUXE_STORE_PRODUCTS`
3. Add initial data: `[]` (empty array)
4. Click **"Create"**
5. **Copy the Bin ID** (you'll see it in URL or bin details)

**Example Bin ID:** `507f1f77bcf86cd799439011`

### Step 3: Get API Key
1. Go to **Account Settings** or **API Keys**
2. Copy your **Master Key** (X-Master-Key)

**Example:** `$2b$10$abc123def456...`

### Step 4: Update Code
1. Open file: `src/cloudStorage.js`
2. Find these lines (around line 4-5):
   ```javascript
   const JSONBIN_API_KEY = 'YOUR_JSONBIN_API_KEY';
   const JSONBIN_BIN_ID = 'YOUR_BIN_ID';
   ```
3. Replace with your actual values:
   ```javascript
   const JSONBIN_API_KEY = '$2b$10$abc123...'; // Your Master Key
   const JSONBIN_BIN_ID = '507f1f77bcf86cd799439011'; // Your Bin ID
   ```

### Step 5: Save & Deploy
1. Save the file
2. Run `npm run build`
3. Deploy to Netlify
4. Test: Add product on one device, check on another!

---

## ✅ How It Works

- **Auto-sync:** Products sync every 30 seconds
- **Cloud Storage:** Products stored in JSONBin.io (cloud)
- **Local Cache:** Also saved in localStorage for offline access
- **Merge Logic:** Cloud products take priority, local products added if not in cloud

---

## 🧪 Testing

1. **Device 1:** Add a product as admin
2. **Wait 30 seconds** (or refresh page)
3. **Device 2:** Open website - product should appear!

---

## 🔧 Troubleshooting

### Products still not syncing?
1. ✅ Check API key and Bin ID in `src/cloudStorage.js`
2. ✅ Verify Bin ID is correct in JSONBin.io
3. ✅ Check browser console for errors (F12)
4. ✅ Make sure Bin is set to "Private" with your API key

### Still using localStorage only?
- Check browser console (F12) for error messages
- Verify JSONBin.io credentials are correct
- App will work with localStorage if cloud storage fails

---

## 📝 File to Edit

**File:** `src/cloudStorage.js`

**Lines to update:**
```javascript
const JSONBIN_API_KEY = 'YOUR_ACTUAL_API_KEY_HERE';
const JSONBIN_BIN_ID = 'YOUR_ACTUAL_BIN_ID_HERE';
```

---

## 🆓 Free Tier Limits (JSONBin.io)

- **Free:** 10,000 requests/month
- **Storage:** Unlimited JSON size
- **Perfect for:** Small to medium stores

---

## 🚀 After Setup

1. Save `cloudStorage.js` file
2. Run `npm run build`
3. Deploy to Netlify
4. Test on multiple devices
5. Products will sync automatically! 🎉

---

**Need help? Check browser console (F12) for error messages!**



