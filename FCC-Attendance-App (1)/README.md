# Forces Coaching Center — Attendance Management System

A complete, browser-based Attendance Management System built for **Forces Coaching Center**, covering student attendance, teacher lateness tracking, fee status, daily absentee follow-up, and institute-wide analytics — all in a single installable web app (PWA), with no backend server or database required.

---

## ✨ Features

### 📊 Dashboard
- Today's Snapshot: live attendance %, present/absent/leave counts, best & lowest performing class **for the selected day**
- Monthly Overview: institute-wide attendance %, totals, students below 75%, best/lowest class, top 10 & bottom 10 students
- Charts: attendance by class (bar), present/absent/leave split (doughnut), daily attendance trend (line)

### 🏫 Class Management (15 classes: Playgroup → 2nd Year)
- Student roster per class: roll no, name, father's name, contact, parent contact, admission no, gender
- Monthly attendance register with a **P / A / L / H dropdown** per student per day
- Sundays are **auto-detected and locked as holidays**
- Auto-calculated per student: Present, Absent, Leave, Holiday, Working Days, Attendance %, Status
- Monthly Summary Panel: average attendance, present/absent/leave %, highest/lowest %, count below 75% / above 90%
- Print-ready attendance register (browser print)

### 📞 Daily Absent Report
- Auto-pulls every student marked **Absent** on a selected date, across all classes
- Admin can log Call Status, Call Time, Reason, Remarks, and Follow-up required — for parent follow-up calls

### 🧾 Student Attendance Report
- Filter by Class, Student, and Month
- Shows working days, present/absent/leave/holiday counts, attendance %, and performance status

### 👩‍🏫 Teacher Attendance & Lateness Tracking
- Teacher roster management (name, subject/class, contact)
- Configurable rules: **Late Threshold (minutes)** and **"N lates = 1 absence"** ratio
- Mark P/A/L + arrival time; late arrivals are auto-flagged
- Monthly summary: Present, Absent, Leave, Total Late, Lateness-converted absences, Effective Attendance %

### 💰 Fee Tracking
- Mark each student Paid/Unpaid per month
- Live Paid vs Unpaid counts shown right on the attendance-marking screen

### 🔍 Global Search
- Instantly find any student by name, roll number, admission number, or contact number, across all classes

### 📱 Mobile App (Progressive Web App)
- Installable on any phone's home screen — works like a native app, including offline
- Custom app icons and branding using the institute's real logo
- Fully responsive layout with a mobile navigation drawer

### 🎨 Branding
- Institute name, academic session, and logo are all customizable from the Settings page

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | CSS3 (custom design system, CSS variables, responsive/mobile-first, print stylesheet) |
| Logic | Vanilla JavaScript (ES6+, async/await) |
| Charts | [Chart.js](https://www.chartjs.org/) (via CDN) |
| Data Storage | Browser `localStorage` + Persistent Storage API (offline-first, no backend needed) |
| Mobile App | Progressive Web App — Web App Manifest + Service Worker |
| Icons/Branding | Generated from the institute's logo (Python/Pillow) |
| Hosting | Any static host (Netlify, GitHub Pages, Vercel, or run fully offline as a local file) |

---

## 📁 File Structure

```
FCC-Attendance-App/
├── attendance-system.html   # The entire application (UI + logic)
├── manifest.json            # PWA manifest (app name, icons, theme)
├── sw.js                    # Service worker (offline caching)
├── icon-192.png             # App icon (192×192)
├── icon-512.png             # App icon (512×512)
└── logo-sidebar.png         # Logo shown in the sidebar
```

All 6 files must stay together in the same folder — the app references the icons and manifest using relative paths.

---

## 🚀 Getting Started

### Option A — Run it locally (fastest, no setup)
1. Download all 6 files into one folder.
2. Double-click `attendance-system.html` to open it in your browser.
3. Start adding classes, students, and marking attendance — data saves automatically in that browser.

> Note: When opened this way (`file://`), the app works fully, but the "Install as mobile app" feature requires Option B below, since installability needs the app to be served over `http(s)`.

### Option B — Host it to get the installable mobile app
1. Go to [Netlify Drop](https://app.netlify.com/drop).
2. Drag and drop the **folder** containing all 6 files (not a `.zip`).
3. Netlify gives you a live link.
4. Open that link on your phone in Chrome/Safari → menu → **"Add to Home Screen"**.
5. The app now runs like a native app, with an icon, full-screen mode, and offline support.

---

## 💾 Data & Backups

- All attendance, student, teacher, and fee data is stored **locally in the browser** you use — nothing is sent to any server.
- Data persists across refreshes and browser restarts, and the browser is asked to protect it from automatic clean-up.
- Data is **only** removed if the browser's site data/history is manually cleared.
- **Go to Settings → Export Backup** regularly to download a JSON backup of everything. Use **Restore from Backup** to bring it back (or move it to another computer/browser).

---

## 🌐 Browser Compatibility

Works on all modern browsers: Chrome, Edge, Safari, Firefox (desktop and mobile).

---

## 🔧 Customization

- **Institute name, session, classes, teachers**: Settings page
- **Logo**: replace `logo-sidebar.png`, `icon-192.png`, and `icon-512.png` with your own (same filenames)
- **Colors/theme**: edit the CSS variables at the top of `attendance-system.html` (`--navy`, `--sky`, `--green`, `--yellow`, `--red`)
- **Late-arrival rules**: Teacher Attendance → Manage Teachers tab

---

## 📌 Notes

- This is a single-institute, single-device-at-a-time tool by design (no login system, no shared cloud database) — ideal for a front-desk computer or a teacher's/admin's own phone.
- If multi-device, multi-user syncing (e.g. every teacher's phone seeing the same live data) is needed in the future, that would require adding a small backend database — happy to help scope that out separately.

---

*Built for Forces Coaching Center.*
