# Cloud Storage Setup - Cross-Device Product Sync

## Problem
Products added by admin are only visible on the device where they were added because they're stored in localStorage (device-specific storage).

## Solution
Simple cloud storage using JSONBin.io (free JSON storage service) - No Firebase needed!

---

## Step 1: Create JSONBin.io Account (Free)

1. Go to [JSONBin.io](https://jsonbin.io/)
2. Click **Sign Up** (free account)
3. Create account with email or GitHub

---

## Step 2: Create a Bin

1. After login, click **Create Bin**
2. Name it: `SM_LUXE_STORE_PRODUCTS`
3. Add initial data: `[]` (empty array)
4. Click **Create**
5. Copy the **Bin ID** (you'll see it in the URL or bin details)

---

## Step 3: Get API Key

1. Go to **Account Settings** or **API Keys**
2. Copy your **Master Key** (X-Master-Key)

---

## Step 4: Update Code

1. Open `src/cloudStorage.js`
2. Replace these values:

```javascript
const JSONBIN_API_KEY = '$2a$10$gy0xCoZSfBiIyW31ThHmdu5AUoUpdOIQ9ZZRhIMHE.u0aZF8bjJUW';
const JSONBIN_BIN_ID = '6923012cae596e708f6ba074';
```

**Example:**
```javascript
const JSONBIN_API_KEY = '$2b$10$abc123...';
const JSONBIN_BIN_ID = '507f1f77bcf86cd799439011';
```

---

## Step 5: Test

1. Run `npm start`
2. Add a product as admin
3. Check JSONBin.io dashboard - you should see your product data
4. Open website on another device - product should appear!

---

## How It Works

- **Auto-sync:** Products sync every 30 seconds
- **Cloud Storage:** Products stored in JSONBin.io (cloud)
- **Local Cache:** Also saved in localStorage for offline access
- **Merge Logic:** Cloud products take priority, local products added if not in cloud

---

## Alternative: Use Your Own Backend API

If you have a backend API, update `src/cloudStorage.js`:

1. Uncomment the API_URL option
2. Replace with your API endpoint:

```javascript
const API_URL = 'https://your-api.com/api/products';

// Then update getProductsFromCloud and saveProductsToCloud functions
```

---

## Troubleshooting

### Products not syncing?
1. Check API key and Bin ID in `src/cloudStorage.js`
2. Verify Bin ID is correct in JSONBin.io
3. Check browser console for errors
4. Make sure Bin is set to "Private" with your API key

### Still using localStorage only?
- Check if API key and Bin ID are set correctly
- Check browser console for errors
- App will work with localStorage if cloud storage fails

---

## Free Tier Limits (JSONBin.io)

- **Free:** 10,000 requests/month
- **Storage:** Unlimited JSON size
- **Perfect for:** Small to medium stores

---

## Need More?

- JSONBin.io Docs: https://jsonbin.io/api-reference
- Upgrade to paid plan for more requests if needed



