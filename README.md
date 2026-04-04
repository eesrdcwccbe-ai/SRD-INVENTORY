# 🚀 SRD Inventory Portal - Production Deployment Guide

## Overview
Complete inventory management system for Southern Rivers Division, Central Water Commission, Coimbatore.

## Features
✅ Firebase Realtime Database Integration
✅ User Management (EE Level)
✅ T&P Assets Management
✅ MAS Articles Management
✅ Add/Edit/Delete Items (JE Level)
✅ Export to CSV
✅ Search & Filter
✅ Responsive Design (Mobile, Tablet, Desktop)
✅ Real-time Sync
✅ QR Code Generation

## Quick Start

### 1. Firebase Setup
1. Go to [Firebase Console](https://console.firebase.google.com)
2. Create a new project: "SRD-Inventory"
3. Enable Realtime Database
4. Get your config from Project Settings > General > Your apps > Web app

### 2. Configure Firebase
Edit `index.html` and replace Firebase config (lines 46-53):
```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  databaseURL: "https://YOUR_PROJECT.firebaseio.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

### 3. Deploy to Vercel

#### Option A: Using Vercel CLI
```bash
npm install -g vercel
vercel login
vercel --prod
```

#### Option B: Using Vercel Dashboard
1. Go to [vercel.com](https://vercel.com)
2. Click "Add New" > "Project"
3. Import this repository
4. Deploy!

## File Structure
```
srd-inventory-portal/
├── index.html          # Main application file
├── vercel.json         # Vercel configuration
├── package.json        # NPM configuration
└── README.md           # This file
```

## Default Credentials
- **JE (Junior Engineer)**: `je` / `je123` - Full Access
- **AD-II (Assistant Director)**: `ad` / `ad123` - View Only  
- **EE (Executive Engineer)**: `ee` / `ee123` - View + User Management

## User Management (EE Level)
EE can:
- Change user names
- Update usernames
- Change passwords
- Modify user roles

## Data Storage
- **Firebase**: Real-time cloud database (when configured)
- **localStorage**: Automatic fallback if Firebase unavailable

## Adding Lab Items
The portal starts with 3 sample items. To add all 136 lab items:
1. Login as JE
2. Use "Add New" tab
3. Or import via browser console (see documentation)

## Browser Compatibility
- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile browsers

## Support
For issues or questions, contact CWC Coimbatore IT Department.

## License
© 2024 Central Water Commission, Coimbatore
