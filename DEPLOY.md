# Firebase Hosting Deployment Guide

## Prerequisites
- Node.js and npm installed
- Firebase CLI installed

## Quick Deployment Steps

### 1. Install Firebase CLI (if not already installed)
```bash
npm install -g firebase-tools
```

### 2. Login to Firebase
```bash
firebase login
```

### 3. Deploy to Firebase Hosting
```bash
firebase deploy --only hosting
```

## Your App URLs
- **Firebase Hosting**: https://casa-de-amor-content-os.web.app
- **Alternative URL**: https://casa-de-amor-content-os.firebaseapp.com

## Files Already Configured
- `firebase.json` - Firebase Hosting configuration
- `.firebaserc` - Firebase project configuration
- `index.html` - Main application file

## Notes
- The `firebase.json` is configured to serve all files from the root directory
- All routes are redirected to `index.html` for single-page application behavior
- After deployment, your app will be live at the URLs above


---

## Option 2: Automatic Deployment with GitHub Actions (Recommended)

This is the easiest way to deploy - every time you push to GitHub, it automatically deploys to Firebase!

### Setup GitHub Actions (One-time setup)

1. Clone your repository locally:
```bash
git clone https://github.com/casadeamor/casa-de-amor-content-os.git
cd casa-de-amor-content-os
```

2. Install Firebase CLI:
```bash
npm install -g firebase-tools
```

3. Initialize GitHub Actions integration:
```bash
firebase init hosting:github
```

4. Follow the prompts:
   - The CLI will create a service account with deploy permissions
   - It will add the service account key as a GitHub secret
   - It will create workflow files for automatic deployment

5. Commit and push the workflow files:
```bash
git add .github/
git commit -m "Add Firebase Hosting GitHub Action"
git push
```

### What happens after setup?

- **Every PR**: Gets its own preview URL for testing
- **Every merge to main**: Automatically deploys to production
- **No manual commands needed**: Just push your code!

### Your Live URLs
After deployment:
- **Production**: https://casa-de-amor-content-os.web.app
- **Alternative**: https://casa-de-amor-content-os.firebaseapp.com
