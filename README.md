# Medico 🩺

**Medico finds the closest hospital that treats what you need, books your visit, and keeps your prescriptions, procedures, and bills in one place.**

## Why Medico exists

For many Nigerians, getting healthcare means long queues, lost records, and not knowing which hospital can actually treat them. Poor data handling and mismanagement cost patients time, money, and sometimes their lives.

Medico was built to strengthen that overwhelmed system with technology.

*I am rewriting that story, one line at a time.*

## Features

**For patients**
- 🔎 **Treatment search:** search for a treatment and get routed to the closest hospital that offers it, using your live location
- 🎫 **Digital tickets:** book a visit and receive a ticket the hospital can scan on arrival
- 🔐 **Medical History:** patients can view their entire medical history at the click of a button
- 📊 **Personal dashboard:** active tickets, hospitals visited, and total amount spent
- ⭐ **Bills:** bills can be tracked on Medico and later paid for

**For hospitals**
- 📷 **Ticket scanner:** verify patient tickets at the front desk
- 🗂️ **Electronic medical records:** store, track, and query patient data (with patient consent)
- 📈 **Visibility:** reach patients searching for the treatments you offer

## Tech stack

| Layer | Technology |
|---|---|
| Frontend | React, TypeScript, Vite |
| Backend | Node.js, TypeScript |
| Database | MongoDB (Mongoose) |
| Hosting | Render |


## Architecture

Medico is made of three parts:

```
medicallyClient  (patient app)   ─┐
                                   ├──►  Medico API  ──►  MongoDB
hospitalClient   (hospital app)  ─┘
```

- **Patient app:** treatment search, location-based routing, tickets, payments
- **Hospital app:** ticket scanning, patient records, hospital dashboard
- **API:** authentication, hospital search, ticketing, and record access rules

<!-- TODO: one sentence describing how "closest hospital" is calculated, e.g. "Hospitals are ranked by distance from the patient's coordinates using ___." -->

## Live demo

> ⏳ Medico runs on Render's free tier, so the server may take **up to a minute to wake up** on first visit. Open the API link first to wake it.

| App | Link |
|---|---|
| API (open first) | https://medico-52jv.onrender.com/home |
| Patient dashboard | https://medico-patient.onrender.com/login |
| Hospital dashboard | https://medico-hospitals.onrender.com/ |

**Demo account**
- Username: `alaminmedico`
- Password: `12345`

The demo account contains sample data only, no real patient information.

## Screenshots

<img width="1912" height="902" alt="Medico patient dashboard: treatment search" src="https://github.com/user-attachments/assets/e7e016a9-a095-4b66-aad7-a467451c8a2b" />

<img width="1913" height="903" alt="Medico routing a patient to the nearest hospital" src="https://github.com/user-attachments/assets/c9ebb0dc-bb22-46c1-96a9-4ac1c4fd052c" />

<!-- TODO: check the captions above match what each screenshot actually shows -->

## Run locally

```bash
# Clone the repo
git clone <repo-url>
cd medico

# Backend
cd server
npm install
npm run dev

# Patient app (in a new terminal)
cd medicallyClient
npm install
npm run dev

# Hospital app (in a new terminal)
cd hospitalClient
npm install
npm run dev
```

**Environment variables**

Backend `.env`:
```
Requires a MongoDB connection string and a JWT secret in a .env file.

Frontend `.env.development` (in each client):

VITE_API_URL=/api
```

## Roadmap

- [ ] Mobile-first redesign of the patient app
- [ ] Hospital onboarding and pilot programme
- [ ] Payments for tickets
- [ ] Nigeria Data Protection Act compliance

## Author

Built by **MUHAMMAD ALAMIN BELLO**, a full-stack software engineer using technology to improve industries, starting with healthcare in Nigeria.

<!-- TODO: add LinkedIn / X / email -->
