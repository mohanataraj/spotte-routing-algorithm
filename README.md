# Spotte Routing Algorithm

**Temporal Journey Representation for Next-Generation Navigation**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21439010.svg)](https://doi.org/10.5281/zenodo.21439010)

> Research into traveler-specific temporal journey representations for predictive navigation and route decision support.

---

## Overview

Modern navigation systems already employ sophisticated traffic prediction models to estimate travel times and optimize routes. However, travelers are typically presented with estimated arrival times (ETA), current traffic overlays, and route recommendations rather than a representation of the conditions they are expected to encounter throughout their journey.

This repository explores a **Traveler-Specific Temporal Journey Representation (TJR)**—a navigation architecture that synchronizes predicted transportation network states with the predicted progression of an individual traveler through a transportation network.

Rather than replacing existing routing algorithms or traffic prediction models, this work investigates how predicted transportation states can be synchronized, represented, and communicated to improve route evaluation before navigation begins.

---

## Research DOI

This repository accompanies the following archived technical disclosure.

**Zenodo DOI**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21439010.svg)](https://doi.org/10.5281/zenodo.21439010)

---

## Vision

> *"An image speaks a thousand words. This one simply asks you to listen to the future while we build it."*

<img width="1536" height="1024" alt="driving_future" src="https://github.com/user-attachments/assets/6f2983f3-ebf6-46ff-81a9-9beefe80bd43" />

---

# Existing Navigation

```text
Origin + Destination
        │
        ▼
Future Traffic Prediction
        │
        ▼
Route Optimization
        │
        ▼
ETA
        │
        ▼
Navigate
```

---

# Traveler-Specific Temporal Journey Representation (Proposed)

```text
Origin + Destination
        │
        ▼
Future Traffic Prediction
        │
        ▼
Predict Arrival at Every Route Segment
        │
        ▼
Synchronize Forecast with Traveler Progression
        │
        ▼
Construct Traveler-Specific
Temporal Journey Representation
        │
        ▼
Present Candidate Journeys
        │
        ▼
User Selects Route
```

---

# Research Motivation

Drivers do not travel through the present.

They travel through the future.

Traditional navigation systems primarily communicate:

- Current traffic conditions
- Estimated arrival time
- Route recommendations

This research investigates whether navigation systems can instead communicate:

- Expected traffic at user arrival
- Predicted roadway conditions
- Forecasted incidents
- Confidence metrics
- Route stability
- A traveler-specific representation of the journey before navigation begins

The objective is not to improve traffic prediction itself, but to improve how those predictions are synchronized and presented for route evaluation.

---

# Comparison

| Existing Navigation | Traveler-Specific Temporal Journey Representation |
|---------------------|--------------------------------------------------|
| Current traffic overlays | Future transportation state synchronized with traveler arrival |
| ETA-centric | Journey-centric |
| Route recommendation | Journey representation |
| Network state | Traveler-specific state |
| Current conditions | Predicted conditions at arrival |
| Reactive updates | Predictive evaluation |
| Space | Space + Time |

---

# System Architecture

```text
                    Data Acquisition Layer
──────────────────────────────────────────────────────────────────

 Navigation Provider Traffic APIs
 (Google Maps • HERE • TomTom • etc.)

                 │
                 ▼

 Crowdsourced Dashcam Network

                 │
                 ▼

 Roadside Traffic Cameras

                 │
                 ▼

 Satellite & Aerial Imagery

                 │
                 ▼

 Weather
 Roadworks
 Construction
 Special Events
 Historical Traffic Data
 Vehicle Telemetry
 Connected Vehicles (V2X)
 Government Transportation Data

──────────────────────────────────────────────────────────────────
                     Sensor Fusion Layer
──────────────────────────────────────────────────────────────────

Normalize Data

↓

Computer Vision

↓

Traffic State Estimation

↓

Spatio-Temporal Road Graph

↓

Transportation State Forecasting

──────────────────────────────────────────────────────────────────
        Traveler Synchronization Engine
──────────────────────────────────────────────────────────────────

Generate Candidate Routes

↓

Predict Traveler Arrival
at Every Route Segment

↓

Synchronize Arrival Times
with Transportation Forecast

↓

Recursive ETA Propagation

↓

Update Downstream Predictions

↓

Estimate Confidence

↓

Compute Route Stability

↓

Construct Traveler-Specific
Temporal Journey Representation

──────────────────────────────────────────────────────────────────
                  Decision Support Layer
──────────────────────────────────────────────────────────────────

Future Journey Timeline

↓

Predictive Route Snapshots

↓

Journey Confidence

↓

Congestion Arrival Forecast

↓

Expected Delays

↓

Traveler Decision Support

↓

Navigation
```

---

# Research Scope

Potential heterogeneous data sources include:

- Navigation traffic providers
- Fleet telemetry
- Crowdsourced dashcams
- Roadside traffic cameras
- Satellite imagery
- Aerial imagery
- Vehicle telemetry
- Weather services
- Roadworks
- Construction activity
- Scheduled events
- Connected vehicle messages
- Government transportation feeds

The synchronization architecture is independent of the specific traffic forecasting model and may operate with statistical, physics-based, graph-based, or machine-learning forecasting techniques.

---

# Research Status

This repository represents ongoing research into temporal navigation architectures and traveler-specific journey representations.

The concepts described here are intended to stimulate research into decision-support systems for intelligent transportation and should not be interpreted as a replacement for existing navigation or traffic prediction systems.

---

# Intellectual Property Notice

This repository describes original research and technical concepts developed by the author.

This work has been archived as a citable scientific publication under the following DOI:

**https://doi.org/10.5281/zenodo.21439010**

The concepts, systems, methods, algorithms, architectures, traveler-specific temporal journey representations, synchronization methods, and implementations described herein may be the subject of one or more pending or future patent applications.

Nothing contained in this repository shall be construed as granting any license, express or implied, to practice any invention disclosed herein.

The author expressly reserves all intellectual property rights, including patent rights, copyrights, trade secrets, continuations, divisionals, continuations-in-part, derivative works, and future improvements to the fullest extent permitted by applicable law.
