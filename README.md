# SMART INDIA HACKATHON WORKSHOP

**Date:** 26/10/2026

**Register Number:** 212224040306

**Name:** Shamrin B

## Problem Title

**SIH 1710: Enhancing Navigation for Railway Station Facilities and Locations**

## Problem Creator's Organization

Ministry of Railways

## 1. Idea

**RailNav AI – Smart Railway Station Navigation System**

RailNav AI is a smart, accessible, and user-friendly navigation system designed to help passengers find platforms, ticket counters, restrooms, food courts, waiting halls, lifts, escalators, and exits inside railway stations. It uses interactive station maps, indoor navigation, voice assistance, and real-time facility updates to guide passengers to their destinations quickly and safely.

## 2. Proposed Solution / Architecture Diagram

### Proposed Solution

The proposed system consists of a mobile application and touchscreen kiosks installed inside railway stations. Passengers can select their destination, view the shortest accessible route, and follow step-by-step directions.

**Key features:**

- **Interactive maps:** Displays station layouts and important facilities in 2D or 3D.
- **Indoor navigation:** Guides passengers through corridors, platforms, stairs, lifts, and entrances.
- **Voice guidance:** Provides audio instructions for visually impaired passengers.
- **Accessibility mode:** Suggests wheelchair-friendly routes using lifts and ramps.
- **Live updates:** Shows temporary closures, platform changes, and unavailable facilities when updated data is available.
- **Multilingual support:** Provides directions in English, Tamil, Hindi, and other supported languages.
- **Digital kiosks:** Allows passengers without smartphones to search for facilities.
- **Emergency assistance:** Displays emergency exits and help desks.

### Architecture Diagram

```text
       PASSENGER
           |
           v
  +----------------------+
  | Mobile App / Kiosk   |
  | Voice & Touch Input  |
  +----------------------+
           |
           v
  +----------------------+
  | User Request Module  |
  | Destination Search   |
  +----------------------+
           |
           v
  +----------------------+
  | Navigation Engine    |
  | Route Calculation    |
  | Accessibility Rules  |
  +----------------------+
           |
           v
  +----------------------+
  | Station Map & Data   |
  | Facilities / Routes  |
  | Live Station Updates |
  +----------------------+
           |
           v
  +----------------------+
  | Directions Output    |
  | Map / Voice / Text   |
  +----------------------+
           |
           v
        PASSENGER
```

**Working:** The passenger selects a destination. The system identifies the current location, checks the station map and available route information, calculates a suitable path, and displays step-by-step directions. If accessible navigation is selected, it prioritizes suitable routes such as ramps and lifts.

## 3. Use Cases

1. **Finding a platform:** A passenger searches for Platform 5 and receives directions from the station entrance.
2. **Locating facilities:** A passenger finds the nearest restroom, ticket counter, drinking-water point, or food court.
3. **Assisting visually impaired passengers:** Voice instructions guide passengers along the mapped route.
4. **Wheelchair navigation:** A passenger receives a route that avoids stairs and uses accessible lifts or ramps.
5. **Finding a waiting hall:** A passenger gets directions to the waiting area while waiting for a train.
6. **Locating emergency exits:** Passengers can identify mapped emergency exits and help desks.
7. **Using digital kiosks:** Passengers without smartphones can search for locations through a touchscreen kiosk.
8. **Handling station changes:** When railway staff update platform or facility information, the system refreshes the relevant directions.

## 4. Technology Stack

| Component | Proposed Technology |
|---|---|
| Mobile application | React Native |
| Web application and kiosk interface | React.js |
| Backend API | Python FastAPI |
| Route calculation | Python with NetworkX |
| Interactive maps | MapLibre GL JS or a custom indoor map renderer |
| Database | PostgreSQL with PostGIS |
| Real-time updates | WebSockets or server-sent events |
| Voice assistance | Text-to-speech and speech recognition APIs |
| Authentication | Secure role-based authentication |
| Hosting | Cloud hosting or railway-approved infrastructure |
| Version control | Git and GitHub |

## 5. Dependencies

The project requires the following resources and dependencies:

1. **Station map data:** Accurate layouts of platforms, entrances, exits, corridors, stairs, lifts, ramps, and facilities.
2. **Location information:** QR codes, Bluetooth beacons, or other approved indoor-positioning methods to estimate passenger location.
3. **Railway data integration:** Access to authorized APIs or systems for platform changes and facility status updates.
4. **Backend services:** A server to process requests and provide route information.
5. **Database:** Storage for station layouts, facility details, accessible paths, and update records.
6. **Internet connectivity:** Required for downloading maps and receiving live updates; offline maps should be available where possible.
7. **Accessibility support:** Screen-reader compatibility, voice instructions, clear text, and wheelchair-friendly route information.
8. **Hardware:** Smartphones, touchscreen kiosks, and optional indoor-positioning devices.
9. **Security and privacy:** Secure communication, restricted staff access, and minimal collection of passenger location data.
10. **Testing resources:** Sample station maps and testing with passengers, including users with disabilities.

**Expected Outcome:** RailNav AI aims to reduce passenger confusion, save time, improve accessibility, and make railway stations easier to navigate. Real-time accuracy will depend on reliable station maps, authorized railway data, and regularly updated facility information.
