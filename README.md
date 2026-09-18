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
| Hosting | Any static host (Netlify, GitHub Pages, Vercel, or run fully offline as a local file) |

---

## 📁 File Structure
