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
