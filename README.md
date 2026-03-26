# Mapathon
project
# Shatorko BD

Shatorko BD is a hybrid last-mile early warning system for vulnerable communities in Bangladesh.  
It is designed for areas with weak mobile networks, limited smartphone access, and low-literacy populations.

The system delivers official disaster alerts through:
- LoRaWAN-based relay nodes
- sirens and warning lights
- local Bangla / dialect voice alerts
- trusted institutions such as mosques, schools, hospitals, shelters, and Union Parishads
- dynamic shelter mapping for evacuation support

---

## Problem

In many parts of Bangladesh, official disaster warnings are issued on time but do not reach local communities in a form they can quickly understand and act upon.

Common challenges include:
- poor or unreliable mobile network coverage
- geographically isolated communities
- limited access to smartphones or internet services
- difficult or non-localized warning language
- delays in communication between authorities and communities
- poor coordination during evacuation

---

## Solution

Shatorko BD closes the last-mile gap by combining:

1. **LoRaWAN communication**
   - long-range, low-power communication for weak-network areas

2. **Edge-AI local voice alerts**
   - converts warning text into simple Bangla or local-dialect audio

3. **Community relay nodes**
   - uses existing trusted institutions as last-mile broadcast points

4. **Dynamic shelter mapping**
   - identifies the nearest safe shelter and route

5. **Acknowledgment tracking**
   - helps authorities know which nodes and communities received the alert

---

## System Architecture

The system has 6 major layers:

### 1. Central Command Layer
- Disaster Authority Dashboard
- Alert Management Server
- Database
- Map / GIS Engine

### 2. Message Intelligence Layer
- Bangla Alert Simplifier
- Dialect TTS / Audio Engine
- Alert Template Builder
- Policy / Routing Rules Engine

### 3. Communication Layer
- Internet / App Push
- LoRaWAN Server
- SMS Fallback
- LoRa Gateway

### 4. Community Relay Layer
- Mosque Node
- Temple Node
- Hospital Node
- School / Shelter Node
- Union Parishad Node
- Orange Pi / Edge-AI Unit

### 5. Human Dissemination Layer
- Institution Staff
- Local Volunteers
- Community Members

### 6. Feedback & Evacuation Support Layer
- Volunteer / Responder App
- Dynamic Shelter Mapping
- Acknowledgment & Coverage Tracking

---

## Key Features

- works without depending only on smartphones or internet
- sends warnings through LoRaWAN relay nodes
- triggers siren, warning light, and loudspeaker audio
- supports local Bangla / dialect voice alerts
- uses trusted local institutions for dissemination
- helps responders guide people to the nearest safe shelter
- supports acknowledgment and coverage tracking

---

## Tech Stack

### Backend
- Python
- FastAPI / Flask
- PostgreSQL / SQLite
- NetworkX
- REST API

### Relay Node
- Orange Pi / Raspberry Pi
- LoRa module (SX1276 / SX1278)
- Python daemon
- GPIO relay control
- speaker + amplifier

### Dashboard
- React or simple web frontend

### Mapping
- OpenStreetMap / GeoJSON
- Dijkstra / A* route planning

---

## Repository Structure

```text
backend/         Central server and APIs
node/            Relay node software
dashboard/       Operator dashboard
responder-app/   Volunteer / responder interface
data/            Shelters, nodes, routes, sample alerts
audio/           Bangla and dialect audio assets
docs/            Architecture and deployment docs
scripts/         Utilities and demo scripts

## Our System Architecture

<img width="6037" height="3040" alt="image" src="https://github.com/user-attachments/assets/c2aef416-f7ac-413c-9d38-eb8736b5cbc6" />
