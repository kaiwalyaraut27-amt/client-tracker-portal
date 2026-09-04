# ⚡ Client Project Portal

A modern, responsive **Client Project Portal** for electrical and civil engineering projects.

The portal provides clients with a centralized dashboard to track project progress, milestones, budgets, site photos, project documents, alerts, and communication with the assigned project manager.

---

## ✨ Features

### 🔐 Client Authentication

The application includes a simple client authentication interface with:

* Login
* Client registration
* Project assignment during registration
* Session persistence
* Logout
* Demo client accounts

The login screen is designed specifically for secure client-facing project access.

### 📊 Project Dashboard

The main dashboard provides an overview of the client's assigned project, including:

* Active project count
* Average project progress
* Open client requests
* Site photo count
* Project budget
* Amount spent
* Schedule status
* Completed milestones
* Project deadline

### 🏗️ Project Progress Tracking

Clients can view detailed information about their assigned project, including:

* Project name
* Project type
* Location
* Completion percentage
* Budget
* Spending
* Project manager
* Risk level
* Next activity

Each project also includes a milestone timeline showing completed, active, and upcoming activities.

### 📅 Milestone Timeline

Projects contain a structured timeline for tracking major activities such as:

* Site survey and foundation
* Structural framework
* Roofing and exterior work
* Internal electrical wiring
* Flooring and finishing
* Final inspection and handover
* Testing and commissioning

Milestones are visually categorized as:

* ✅ Done
* 🔄 In Progress
* ⏳ Upcoming

---

## 📸 Site Photos

The portal provides a dedicated area for viewing recent site photos.

Photos are associated with individual projects and can represent activities such as:

* Foundation work
* Roofing
* Panel rooms
* Cable trays
* Transformer bays
* Cable trenches
* Earth pits

The current version uses generated SVG-based visual placeholders for site imagery.

---

## 📄 Project Documents

Clients can view project-related documents such as:

```text
Electrical safety inspection report.pdf
Civil milestone completion certificate.pdf
BOQ and material approval sheet.pdf
Monthly progress summary.pdf
```

The dashboard provides document download actions within the project workspace.

---

## 📝 Client Requests

Clients can submit project-related requests directly from the portal.

Available request types include:

* Site visit update
* Material clarification
* Design change
* Payment document

Each request can contain a custom message and is associated with the selected project.

Requests are stored locally in the browser and displayed in the Client Requests section.

---

## 💬 Project Manager Communication

The portal provides a contact interface for communicating with the assigned project manager.

Clients can send:

* Subject
* Message
* Project-related queries

## The dashboard also displays the assigned project manager and support information.

## 🔔 Alerts & Activity

The dashboard includes:

* Recent activity feed
* Project alerts
* Progress updates
* Document updates
* Site photo updates
* Client request status

Activity is filtered according to the project assigned to the logged-in client.

---

## 👥 Demo Accounts

The application includes three demo client accounts:

| Client        | Email                   | Password    | Project                      |
| ------------- | ----------------------- | ----------- | ---------------------------- |
| Rajesh Kumar  | `warehouse@muktai.com`  | `client123` | Nagpur Warehouse Complex     |
| Priya Shah    | `pune@muktai.com`       | `client123` | Pune Office Complex Rewiring |
| Amit Deshmukh | `substation@muktai.com` | `client123` | Amravati 33kV Substation     |

These accounts are defined directly in the frontend for demonstration purposes.

> **Security warning:** These are demo credentials only. Do not use this authentication approach for a production application.

---

## 🏢 Included Demo Projects

The project data currently contains three example projects:

### 1. Nagpur Warehouse Complex

**Type:** Civil + Electrical
**Location:** Nagpur, Maharashtra
**Progress:** 78%
**Status:** Active

### 2. Pune Office Complex Rewiring

**Type:** Electrical
**Location:** Pune, Maharashtra
**Progress:** 55%
**Status:** Active

### 3. Amravati 33kV Substation

**Type:** Electrical + Civil
**Location:** Amravati, Maharashtra
**Progress:** 32%
**Status:** On Hold

These project records include budgets, spending, managers, risks, milestones, photos, and deadlines.

---

## 🛠️ Technology Stack

This project is built using lightweight frontend technologies:

* **HTML5**
* **CSS3**
* **Vanilla JavaScript**
* **LocalStorage**
* **SVG**
* **Tabler Icons**
* **Google Fonts — Inter**

No frontend framework or build system is required.

---

## 📁 Project Structure

The current project is a standalone HTML application:

```text
client-project-portal/
│
├── client-portal.html
└── README.md
```

All HTML, CSS, JavaScript, project data, authentication logic, and UI components are contained in the HTML file.

---

## 🚀 Getting Started

### 1. Clone the repository


### 2. Open the project

Open:

```text
client-portal.html
```

in a modern web browser.

That's it — no installation or build process is required.

---

## 🔄 Application Flow

```text
             ┌─────────────────┐
             │   Login / Sign  │
             │       Up        │
             └────────┬────────┘
                      │
                      ▼
             ┌─────────────────┐
             │ Client Session  │
             └────────┬────────┘
                      │
                      ▼
             ┌─────────────────┐
             │    Dashboard    │
             └────────┬────────┘
                      │
        ┌─────────────┼─────────────┐
        ▼             ▼             ▼
   ┌─────────┐   ┌──────────┐  ┌──────────┐
   │ Projects│   │  Photos  │  │ Reports  │
   └────┬────┘   └──────────┘  └──────────┘
        │
        ▼
 ┌──────────────────┐
 │ Project Details  │
 ├──────────────────┤
 │ Progress         │
 │ Budget           │
 │ Milestones       │
 │ Documents        │
 │ Requests         │
 └──────────────────┘
```

---

## 💾 Data Storage

The current prototype uses the browser's **LocalStorage** for client accounts, sessions, and client requests.

Examples include:

```javascript
localStorage.getItem('muktaiPortalUsers')
localStorage.getItem('muktaiPortalSession')
localStorage.getItem('muktaiClientRequests')
```

This makes the project easy to run as a standalone prototype without requiring a database or backend.

---

## 📱 Responsive Design

The interface is designed to work across:

* Desktop
* Laptop
* Tablet
* Mobile devices

Responsive breakpoints adjust the dashboard layout, navigation, cards, statistics, authentication screen, and project details for smaller screens.

---

## 🎨 UI & Design

The interface uses a modern enterprise dashboard design featuring:

* Clean card-based layouts
* Responsive navigation
* Progress indicators
* Status badges
* Project timelines
* Modal dialogs
* Toast notifications
* Responsive grids
* Professional blue/green visual language
* Inter typography
* Tabler iconography

The authentication page also includes a dedicated visual landing panel describing the client portal's capabilities.

---

## 🔒 Security Notice

This repository contains a **frontend prototype**, not a production-grade authentication system.

The current implementation:

* Stores users in LocalStorage
* Stores passwords in LocalStorage
* Uses demo credentials in frontend JavaScript
* Does not use server-side authentication
* Does not have role-based authorization
* Does not use a secure database

Therefore, it should **not be used to store real client credentials, confidential documents, financial information, or sensitive project data** without implementing a proper backend authentication and authorization system.

---

## 🚧 Current Limitations

The following features are currently represented as frontend/demo functionality:

* Authentication
* Project database
* Document downloads
* Project reports
* Messaging
* Site photo management
* Alerts
* Project manager communication

For example, the current report action displays a download-preparation notification rather than generating a real report file.

---

## 🌱 Future Improvements

Potential production improvements include:

* [ ] Backend API
* [ ] Secure authentication
* [ ] Password hashing
* [ ] JWT/session-based authorization
* [ ] Role-based access control
* [ ] PostgreSQL/MySQL database
* [ ] Real project management backend
* [ ] Cloud file storage
* [ ] Real site photo uploads
* [ ] Real PDF report generation
* [ ] Document preview
* [ ] Real-time notifications
* [ ] Email notifications
* [ ] WhatsApp/SMS notifications
* [ ] Project manager/admin dashboard
* [ ] Payment tracking
* [ ] BOQ integration
* [ ] Invoice management
* [ ] Progress report generation
* [ ] Audit logs
* [ ] Multi-company support
* [ ] API-based project data

---

## 🔗 Integration Possibilities

This Client Project Portal can be extended into a complete construction/project management platform by integrating it with:

```text
                    Client Portal
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
     Project API      BOQ System     Documents
          │              │              │
          └──────────────┼──────────────┘
                         ▼
                   Backend Server
                         │
                         ▼
                     Database
```

It can also be connected to an existing BOQ/estimation application to allow clients to view approved BOQs, budgets, and project cost updates.

---

## 🎯 Intended Use

This project is suitable as a prototype or starting point for:

* Electrical contractors
* Civil contractors
* Construction companies
* Engineering firms
* Project management teams
* Site management platforms
* Client communication portals
* Construction progress tracking systems

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

Contributions, suggestions, and improvements are welcome.
