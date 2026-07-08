# 🛡️ NSPPD Protocol VIP Journey Tracker 2026

**Old Trafford Stadium, Manchester | 25–26 September 2026**

A full-featured VIP guest journey management web application for the NSPPD UK Conference 2026 Protocol Department. Track 200+ VIP guests across all journey stages, from international airports to Old Trafford and back.

---

## ✨ Features

### Admin Interface
- **Dashboard** — live overview of all guest journeys, active tasks, and pending assignments
- **VIP Guest Register** — full guest profiles with flight details, hotel assignments, accessibility needs
- **Task Management** — create, assign, and monitor journey tasks for each guest stage
- **Vehicle Fleet** — manage hired coaches/minibuses, driver contacts, availability
- **Staff Management** — view protocol volunteer assignments and performance
- **Live Map** — Google Maps integration with active journey routes
- **Real-time notifications** — instant alerts when tasks are accepted or completed

### Protocol Staff Interface
- **My Tasks** — view assigned tasks, accept them, and confirm stage completions
- **Journey Tracker** — step-by-step current stage with navigation links
- **Guest Profile** — full VIP guest details, flight status checker, vehicle info
- **Driver Call** — one-tap driver contact

### Shared Features
- **Team Chat** — multi-channel messenger (General, Airport, Venue, Transport, VIP)
- **Flight Status Checker** — live flight status simulation for each guest
- **Google Maps Integration** — turn-by-turn directions for every journey leg
- **Journey Progress Bar** — visual 6-stage progress tracker per guest
- **Notification Centre** — task assignment and completion alerts
- **Persistent Storage** — all data saved locally via localStorage

> **⚠ Operational constraint — read before event day:** localStorage is **device-local**. Data entered on one phone/laptop does **not** sync to other devices. Until the Firebase/Supabase upgrade (see Production Upgrade Path), run the platform from a **single command-desk device** or treat each device as an independent log.

---

## 🗺️ The 6-Stage VIP Journey Cycle

Each guest journey must complete all 6 stages in sequence and **return to origin** before being fully closed:

1. ✈️ **Airport Arrival** — Meet guest at arrivals hall, identity verification, luggage
2. 🏨 **Hotel Escort** — Transport to hotel, check-in facilitation, schedule handover
3. 🏟️ **Hotel → Stadium** — Event day transfer to Old Trafford via VIP route
4. ⭐ **In-Event Service** — Personal detail during the conference
5. 🌙 **Stadium → Hotel** — Phased departure, return transfer
6. 🛫 **Hotel → Airport** — Departure transfer, personal farewell

**Tasks cannot be marked complete until the full cycle is confirmed.** Protocol staff confirm each sub-step, which unlocks the next stage assignment.

---

## 🚀 GitHub Pages Deployment

### Option 1: Direct Upload
1. Fork or create a new repository on GitHub
2. Upload `index.html` to the repository root
3. Go to **Settings → Pages**
4. Under **Source**, select `main` branch and `/ (root)`
5. Click **Save** — your app will be live at `https://yourusername.github.io/repo-name`

### Option 2: GitHub CLI
```bash
git init
git add index.html README.md
git commit -m "Initial commit: NSPPD VIP Tracker 2026"
git branch -M main
git remote add origin https://github.com/yourusername/nsppd-tracker.git
git push -u origin main
```
Then enable GitHub Pages in repository settings.

### Option 3: Netlify Drop
Drag and drop the `index.html` file onto [netlify.com/drop](https://netlify.com/drop) for instant deployment.

---

## 📱 Mobile Compatibility

The app is fully responsive and optimised for:
- iPhone (Safari iOS 14+)
- Android (Chrome 90+)
- Tablet (iPad, Android tablet)
- Desktop (Chrome, Firefox, Edge, Safari)

Protocol staff on event day can use their phones to accept tasks, confirm steps, call drivers, and open Google Maps navigation.

---

## 🔐 Demo Login Credentials

| Name (short ID accepted) | PIN | Role |
|------|-----|------|
| Joseph Mokwugwo | 0000 | Admin |
| Sarah Adebayo | 1111 | Admin |
| V-012 Thomas A. | 0012 | Protocol Staff |
| V-027 Grace M. | 0027 | Protocol Staff |
| V-034 David K. | 0034 | Protocol Staff |
| V-045 Rachel O. | 0045 | Protocol Staff |
| V-056 Ahmed S. | 0056 | Protocol Staff |

**Protocol staff PIN policy:** PIN = last 4 digits of the registered phone number (auto-generated when Admin onboards a member). Staff may sign in with just their volunteer ID (e.g. `V-012`) — full name not required.

**Guest tracking codes** (read-only guest portal, no PIN): `ADY001` · `MEN002` · `OSE003` · `WIL004` · `OKO005`

---

## 🏟️ Venue Configuration

- **Venue**: Old Trafford Stadium, Sir Matt Busby Way, Manchester M16 0RA
- **VIP Entrance**: S Gate (Sir Bobby Charlton Stand) via E2 Car Park
- **VIP Green Room**: Executive Suites, Sir Bobby Charlton Stand
- **VIP Car Park**: E2 (Sir Matt Busby Way) — GMP pre-registration required

---

## 🌍 International Airport Coverage

| Origin | Country | Primary Route |
|--------|---------|--------------|
| Lagos (LOS) | 🇳🇬 Nigeria | LHR via Air Peace / BA |
| Abuja (ABV) | 🇳🇬 Nigeria | LHR via Air Peace / BA |
| Accra (ACC) | 🇬🇭 Ghana | LHR via BA / KLM |
| Johannesburg (JNB) | 🇿🇦 South Africa | LHR via BA / Virgin |
| Toronto (YYZ) | 🇨🇦 Canada | LHR via Air Canada / BA |
| New York (JFK) | 🇺🇸 USA | LHR via BA / Delta |

**UK Connection**: Heathrow → Manchester via Avanti West Coast (2hr 8min) or direct flight LHR→MAN (1hr)

---

## 🔧 Technical Stack

- **Framework**: Vanilla JavaScript (zero dependencies, zero CDN calls, no build step) — deliberately chosen after in-browser Babel/React transpilation failed in restricted environments
- **Routing**: Client-side state management
- **Storage**: localStorage (client-side persistence)
- **Maps**: Google Maps Embed API + directions links
- **Styling**: Custom CSS with CSS variables (dark theme)
- **Icons**: Unicode emoji (no external icon library required)
- **Deployment**: Single HTML file — zero configuration

---

## 📋 Production Upgrade Path

For a production deployment with real-time multi-device sync:
- Replace localStorage with **Firebase Realtime Database** or **Supabase**
- Add **push notifications** via Firebase Cloud Messaging
- Integrate **AviationStack API** for real flight tracking
- Add **Google Maps Platform** for live vehicle tracking
- Implement **JWT authentication** replacing PIN system
- Deploy on **Vercel** or **Railway** with a Node.js backend

---

## 📞 Protocol Department Contact

- **Protocol Director**: Joseph Mokwugwo
- **Operations**: 0161 868 8000 (Old Trafford Events)
- **GMP Transport**: Greater Manchester Police Transport Division
- **Event Dates**: 25–26 September 2026

---

*NSPPD UK Conference 2026 — Protocol & Security Department — Operational Excellence Framework v4.0*
