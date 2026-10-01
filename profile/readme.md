# FlyRust

**A boutique development organization focused on building the next generation of automation, real-time systems, and community infrastructure.**

We specialize in Discord bot ecosystems, flight simulation tooling, and modern infrastructure built on Rust and TypeScript. Our projects power communities ranging from 10 to 50k+ users, with an emphasis on performance, reliability, and elegant architecture.

---

## Mission

FlyRust exists to bridge the gap between passionate communities and the tools they need to thrive. Whether you're managing a roleplay server, or a community of 6 million, we're committed to delivering infrastructure that scales, integrates seamlessly, and stays out of the way.

We believe in:
- **Performance first**: Real-time systems demand efficiency. We measure everything.
- **Open infrastructure**: Where possible, we ship code back to the community.
- **User-centric design**: Tools should amplify community, not complicate it.
- **Transparency**: We document deeply and share learnings.

---

## Featured Projects

### **erlc.fm** — *Closed Source*
A next-generation web radio platform purpose-built for the ER:LC Roblox roleplay community.

**Tech Stack**: Next.js 14, TypeScript, MongoDB, Groq/LLaMA AI integration, Discord OAuth

**Core Features**:
- **AI AutoDJ**: LLaMA-powered music curation via Groq API with seamless track selection
- **YouTube Radio Backend**: Persistent playback infrastructure with streaming optimization
- **Discord OAuth Administration**: Granular role-based access control for station admins
- **Modern Frontend**: Responsive design with live player, schedule, and DJ analytics
- **Production Deployment**: Render-hosted with automated CI/CD pipelines

**Status**: Launched & actively maintained. Available at https://fm.erlc.dev

**Why erlc.fm exists**: The ER:LC community deserved a radio station built for roleplay immersion, not a band-aid streaming solution. erlc.fm delivers transparent backend transparency, real-time stats, and admin tooling that actually understands roleplay workflows.

---

### **Naxify** — *Production*
A Spotify-like dashboard ecosystem that centralizes Discord bot data and music streaming in one unified interface.

**Tech Stack**: Next.js, TypeScript, Discord API integration, Spotify Web API, MongoDB

**Core Features**:
- **Unified Dashboard**: Browse music, streaming stats, and bot activity in one place
- **Discord Bot Linkage**: Connect multiple Discord bots for coordinated music control and analytics
- **Spotify Integration**: Native Spotify API connectivity for seamless track discovery and playback
- **User Profiles**: Track listening history, playlists, and personalized recommendations
- **Real-Time Sync**: Live updates across dashboard and Discord bot commands

**Status**: Production. Live at https://y-o-o.cc.cd

**Why Naxify exists**: Discord bots scattered across different dashboards suck. Naxify consolidates music management and bot orchestration into something that actually feels coherent.

### **The Ayy Team Utilities** — *Closed Source*
Core infrastructure powering theayyteam Discord server (70k+ members, and a community of 6+ million).

**Tech Stack**: Discord.js v14, TypeScript, MongoDB

**Core Responsibilities**:
- Moderation automation and role management
- Event scheduling and announcement distribution
- User analytics and member engagement tracking
- Integration middleware for ecosystem coordination

**Operational Scope**: 24/7 uptime, sub-100ms latency on critical operations, real-time event processing for 70k+ member base.

---

### **OpenWheel** — *Open Source*
Transform a Logitech G29 racing wheel into a motorized autothrust throttle quadrant for X-Plane 12 on Linux.

**Tech Stack**: Rust (tokio async, tokio-tungstenite), evdev Linux input, serde/JSON configuration

**Headline Features**:
- **Hardware Repurposing**: Direct `/dev/input` integration for raw Logitech G29 wheel access
- **WebSocket Bridge**: Native communication with X-Plane 12 DataRef engine for real-time control
- **Motorized Feedback**: FFB motor control for realistic autothrust resistance and detent positioning
- **Configuration System**: JSON-based profiles for per-aircraft throttle behavior and curves
- **Cross-Platform Vision**: Linux-first development with Windows compatibility roadmap
- **Low-Latency Async**: tokio-based event loop for sub-50ms input-to-sim latency

**Status**: Production-ready. Available on GitHub for self-hosting and contribution.

**Why OpenWheel exists**: Flight sims need hardware that matches aircraft behavior. A G29 wheel can feel like an actual autothrust lever with the right translation layer. We're building that layer.

---

### **FlyRust Copilot** — *In Development*
The most emotionally intelligent flight simulation companion ever built for X-Plane 12.

**Tech Stack**: Rust (tokio async, WebSocket), Axum web framework, rodio audio playback, SQLite telemetry, Discord rich presence

**Vision**:
Real-time flight analytics daemon that watches every control input, every altitude, every descent rate, and responds with the voice of a grizzled veteran captain who actually *cares* if you're about to die.

**Core Components**:

1. **Flight State Machine**: Tracks progression from cold-and-dark through engine start, taxiing, flight, and landing
2. **DataRef Subscription Engine**: Native WebSocket integration with X-Plane 12.1.1+ (localhost:8086/api/v3) for real-time telemetry
3. **Aggressive Copilot AI**: Voice warnings powered by fish.audio pre-generated cues with full emotional arc:
   - *Exasperated*: "kid, FLAPS. you tryna kill us?"
   - *Critical fear*: "TOGA FULL POWER NOW!"
   - *Gentle concern*: "watch that rate"
   - *Relief*: "alright, nice recovery"
4. **Intelligent Monitoring**:
   - Flaps configuration (warns on improper settings)
   - Landing gear state (reminders on approach)
   - Landing lights synchronization
   - Autopilot mode validation
   - Stall warning detection and recovery prompts
   - G-force limits and performance envelope
   - Descent rate optimization
5. **Web Dashboard**: Localhost Axum-powered dashboard that auto-opens on launch
   - Live flight state visualization
   - Real-time control input tracking
   - Copilot mood indicator
   - Telemetry graphs and trend analysis
   - Warning log with severity levels
6. **Telemetry & Flight Logging**:
   - SQLite event recording (every state transition, warning, recovery)
   - Obsidian vault markdown export for flight review and analysis
   - Flight performance metrics and progression tracking
7. **Integration Layer**:
   - Discord rich presence (displays current flight status to friends)
   - CLI TUI dashboard alternative
   - Modular plugin architecture for future expansions

**Personality**: Inspired by air crash investigation transcripts—raw emotion, dark humor, genuine concern. The copilot isn't cheerful. It's experienced. It's been through your worst landing attempts. It knows you're better than that.

**Why FlyRust Copilot exists**: X-Plane pilots deserve more than generic warnings. They deserve a companion who understands the *feeling* of flight, the risk, the recovery. A captain who has opinions.

**Release Target**: Q4 2026

**Distribution**: Rust binary + npm CLI wrapper for streamlined installation and updates.

---

## Technology Foundations

### Languages
- **Rust**: Systems-level performance, async networking, embedded tooling (tokio, axum, serde)
- **TypeScript**: Application-layer logic, Discord bots, web services, full type safety
- **Python**: Specialized utilities and one-off infrastructure tasks

### Infrastructure
- **Render**: Production hosting for web services with automatic deployments
- **MongoDB**: Document persistence for user data, settings, analytics
- **Discord API**: OAuth, interactions, guild management, rich presence
- **X-Plane 12 WebSocket API**: Native telemetry streaming at 20+ Hz refresh rates
- **Groq API**: LLaMA inference for real-time AI curation
- **fish.audio**: Pre-generated voice synthesis for copilot audio cues

### Standards
- Full TypeScript everywhere (Discord.js, Next.js, Express/Axum)
- Async-first architecture for latency-sensitive operations
- Persistent storage with change event propagation
- Comprehensive logging and observability
- Automated CI/CD pipelines (GitHub Actions)

---

## Community & Ecosystem

We maintain active integrations with:

- **theayyteam Discord** (58k+ members): Core infrastructure provider
- **ER:LC Roblox Community**: Custom tooling for roleplay immersion
- **X-Plane 12 Flight Simulation**: Hardware interfaces and analytics
- **VATSIM/IVAO**: Future flight tracking and multiplayer coordination

Our philosophy: Ship tools that integrate, not tools that dominate.

---

## Development

### Active Maintainers
- [@enviksy](https://github.com/enviksy) — Architecture, design, core systems

### Contribution Policy
We maintain a selective contribution model:
- **Closed-source projects** (erlc.fm, Ayy Team Utilities): Invitation-based collaboration
- **Open-source projects** (Pogy++): Community contributions welcome via pull request
- **Upcoming projects**: Development-phase; contribution inquiries via GitHub discussions

### Code Standards
- Minimum 80% test coverage for new features
- Mandatory code review before merge
- Semantic commit messages
- Comprehensive README + inline documentation for complex logic
- Accessibility-first UI design where applicable

---

## Roadmap

### Q4 2026
- **FlyRust Copilot**: Beta Release
- **erlc.eu.org**: Community run domain service for ER:LC developers, similar to https://freedns.afraid.org

### 2027 Goals
- Expanded copilot personality system
- Community flight share platform
- Extended X-Plane aircraft type support

---

## Contact & Support

**Issues & Bug Reports**: Open a GitHub issue in the relevant repository

**Feature Requests**: GitHub discussions or email partnership inquiry

**Partnerships & Inquiries**: Reach out to the maintainers directly

---

## License

FlyRust maintains a dual licensing model:
- **Closed-source projects**: Proprietary (contact for licensing inquiries)
- **Open-source projects** (Openwheel): The UNLICENCE

---

## Acknowledgments

FlyRust wouldn't exist without:
- The Discord.js and Rust communities
- The X-Plane 12 flight simulation ecosystem
- The ER:LC roleplay community
- The folks at Groq for LLaMA inference at scale
- Every person who pushed back on mediocre tooling

---

*Last updated: July 2026*
