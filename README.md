<div align="center">

<h1>HEMAPRIYAN R K</h1>

Computer Science and Engineering (Data Science) · Vellore Institute of Technology

[LinkedIn](https://www.linkedin.com/in/hemapriyan-rk) · [Portfolio](https://hemapriyan.vercel.app) · [GitHub](https://github.com/hemapriyan-rk)

</div>

---

**Currently building**
- **VIMES**: tracks people around industrial machinery across two cameras and raises a risk level before they reach a hazardous zone.
- **ORCA EYE**: turns depth and object detection into a stop, turn or continue command for assistive walking guidance.
- **MOVA**: a ride and food-delivery platform for Vellore, with three native Android apps and one backend.

**Direction:** taking the same perception and security engineering into medical systems.

---

## Active projects

### Computer vision and safety systems

**[VIMES](https://github.com/hemapriyan-rk/vimes-industrial-intrusion-detection): Industrial intrusion detection and emergency safety**
Dual-camera edge system that detects people entering hazardous zones around machinery and raises a risk level before contact.
- YOLO11 detection and ByteTrack tracking on each camera, with cross-camera person Re-ID using MobileNetV2 embeddings and cosine matching.
- Ground-plane homography converts pixels to metres, which gives velocity, acceleration, time-to-collision and constant-velocity or constant-acceleration trajectory prediction.
- Polygon safe, warning and hazard zones feed a deterministic risk engine with reason codes.
- Fusion with an ESP32 node (motion, temperature, vibration) over a serial protocol.
- Incident video recording and a cloud console (FastAPI, Supabase) with session-based RBAC, rate limiting and health probes.
- About 21,000 lines of Python across 39 test modules.

**[ORCA EYE](https://github.com/hemapriyan-rk/orca-eye): Assistive-vision navigation baseline (research prototype)**
Measurable baseline pipeline that turns a camera stream into walking guidance commands.
- YOLO detection, MiDaS monocular depth and a hybrid free-space estimator feed a grid-based spatial map.
- Candidate paths are generated and ranked by a weighted score, and the output is one of seven commands, such as `STRAIGHT`, `LEFT` or `STOP`.
- Every stage writes to a JSONL or CSV log, a 12-condition failure detector snapshots bad frames, and a 15-scenario evaluation suite records baseline metrics.
- Explicitly not for real-world mobility use.

### Full-stack and mobile systems

**MOVA: Ride and food-delivery coordination platform (private repository)**
Vellore-based MVP that matches passenger rides with compatible food orders so one vehicle serves both, subject to consent from customer and captain.
- Three native Kotlin Android apps (Customer, Captain, Restaurant) built with Jetpack Compose, on shared network and UI modules.
- Layered TypeScript and Express API on PostgreSQL (Prisma, Supabase with PostGIS) with Redis geo-prefiltering of candidate captains.
- Corridor and micro-detour matching, a dual-consent handshake, explicit state machines for combo and solo jobs, a fare engine, and OTP handover for rides and food.
- Routing goes through a vendor-neutral provider interface with a caching proxy on the back-end. React web landing page, GitHub Actions CI, and 18 test files.
- Source is private. I can walk through it on request.

**[Crate Link](https://github.com/hemapriyan-rk/filelink): Expiring file sharing**
Upload a file, get a short-lived link and QR code.
- Files move directly between the browser and storage through short-lived signed URLs and never pass through the application server.
- Access tokens are stored as SHA-256 hashes, and download limits are enforced atomically in SQL so concurrent requests cannot exceed them.
- Documented handling of five expiry and cleanup race conditions, an admin TOTP override, and escalating bans for abuse.
- Next.js, TypeScript and Supabase, with Vitest unit and integration tests and a written threat model.

### Tooling

**[claude-rigor-skills](https://github.com/hemapriyan-rk/claude-rigor-skills)**
30 Claude Code skills that enforce engineering rigor: threat and trade-off analysis, security review, test design, prior-art search and patent claim stress-testing.

---

## Archived (no longer maintained)

- [A\* Heuristic Analysis](https://github.com/hemapriyan-rk/a-star-search-heuristic-optimization-and-performance-analysis): benchmark of five informed-search algorithms on the n-puzzle, comparing Manhattan Distance with Linear Conflict.
- [RKS Management System](https://github.com/hemapriyan-rk/shop-rks): billing and operations platform for a computer and print shop, built with React, Express, Prisma and PostgreSQL.

---

## Technical stack

| Area | Tools |
| --- | --- |
| Computer vision | YOLO (Ultralytics), ByteTrack, OpenCV, MiDaS depth, homography and kinematics |
| Machine learning | PyTorch, NumPy |
| Back-end | FastAPI, Node.js and Express, Prisma, PostgreSQL with PostGIS, Supabase, Redis |
| Front-end and mobile | Next.js, React, TypeScript, Tailwind CSS, Kotlin, Jetpack Compose |
| Embedded | ESP32 firmware, serial sensor protocol |
| Security | RBAC, rate limiting, hashed tokens, TOTP, signed URLs, threat modelling |
| Delivery | Docker, Vercel, Render, GitHub Actions, Vitest, pytest |

---

## Contact

[LinkedIn](https://www.linkedin.com/in/hemapriyan-rk) · [Portfolio](https://hemapriyan.vercel.app) · [GitHub](https://github.com/hemapriyan-rk)
