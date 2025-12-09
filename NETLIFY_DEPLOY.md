# Netlify Deployment Guide

## Method 1: Deploy via Netlify Dashboard (Easiest)

### Step 1: Build your project locally
```bash
npm run build
```

### Step 2: Deploy to Netlify
1. Go to [https://app.netlify.com](https://app.netlify.com)
2. Sign up/Login with GitHub, GitLab, or Email
3. Click "Add new site" → "Deploy manually"
4. Drag and drop the `build` folder to Netlify
5. Your site will be live in seconds!

## Method 2: Deploy via Git (Recommended)

### Step 1: Push to GitHub
```bash
git add .
git commit -m "Ready for deployment"
git push origin main
```

### Step 2: Connect to Netlify
1. Go to [https://app.netlify.com](https://app.netlify.com)
2. Click "Add new site" → "Import an existing project"
3. Choose GitHub and authorize Netlify
4. Select your repository: `SM_LUXE_STORE`
5. Configure build settings:
   - **Build command:** `npm run build`
   - **Publish directory:** `build`
6. Click "Deploy site"

### Step 3: Environment Variables (if needed)
If you have any API keys or environment variables:
1. Go to Site settings → Environment variables
2. Add your variables (e.g., Cloudinary keys)

## Method 3: Deploy via Netlify CLI

### Step 1: Install Netlify CLI
```bash
npm install -g netlify-cli
```

### Step 2: Login to Netlify
```bash
netlify login
```

### Step 3: Deploy
```bash
# Build first
npm run build

# Deploy
netlify deploy --prod
```

## Important Notes:

1. **Build folder:** Make sure `build` folder is in `.gitignore` (it should be)
2. **SPA Routing:** The `_redirects` file ensures React Router works correctly
3. **Environment Variables:** Add any API keys in Netlify dashboard
4. **Custom Domain:** You can add a custom domain in Site settings → Domain management

## Troubleshooting:

- **404 errors on routes:** Make sure `_redirects` file exists in `public` folder
- **Build fails:** Check Node version (should be 18+)
- **Missing dependencies:** Run `npm install` before building



