# 🎶 Live Song Request Web App

A real-time web-based song request system built for DJs and event hosts. Guests can submit song requests via a mobile-friendly form, and DJs receive and manage those requests live on a dashboard.

---

## 🚀 Features

- 📱 **Mobile-friendly form** for guests to request songs  
- 📡 **Real-time dashboard** that updates instantly  
- 🔄 **Syncs across all devices** using Firebase  
- 🔊 **Track most requested songs** by artist/title  
- ✅ **Mark requests as fulfilled**  
- 📤 **Export all requests as CSV**  
- 🔍 **Search and filter** requests  
- 🎛️ **Sort by latest or most requested**  
- 🌐 **Hosted on GitHub Pages**  

---

## 📁 File Structure

```
/song-request
├── song-request-form.html      # Mobile-friendly submission form
├── song-request-form.css       # Styling for the form
├── dj-dashboard.html           # DJ view of live requests
├── dj-dashboard.css            # Styling for the dashboard
├── index.html (optional)       # Redirects to form or dashboard
└── README.md                   # You're reading it!
```

---

## 🔧 Setup & Hosting

This project is fully static and hosted via **GitHub Pages**.

### ✅ Firebase Setup

1. Create a project at [Firebase Console](https://console.firebase.google.com/)
2. Enable **Cloud Firestore** in test mode
3. Add a **Web App** and copy your Firebase config
4. Paste the config into both HTML files:
   - `song-request-form.html`
   - `dj-dashboard.html`

### 🔒 Firestore Rules (Dev-Only)

```js
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```

> ⚠️ These rules are for testing only. For production, you should implement authentication and restrict access.

---

## 📸 Screenshots

| Mobile Form                          | DJ Dashboard                        |
|-------------------------------------|-------------------------------------|
| ![Form](https://via.placeholder.com/200x400?text=Form) | ![Dashboard](https://via.placeholder.com/400x300?text=Dashboard) |

---

## 🧰 Tech Stack

- HTML, CSS, JavaScript
- Firebase Firestore (v8 SDK)
- GitHub Pages

---

## 🛣 Roadmap Ideas

- 🔐 Auth for DJ dashboard
- 🎨 Custom theming (dark/light mode)
- 📊 Analytics dashboard (top requested songs/artists)
- ✉️ Notifications or email alerts

---

## 📄 License

MIT License. Feel free to remix and build your own version.
