# Cybersecurity-Awareness-Game
Week 1 Report:roject Inception & Architecture
# 📋 1. Executive Summary & Project Vision
Modern digital ecosystems face an escalating volume of cyber threats, ranging from sophisticated phishing campaigns and social engineering attacks to weak credential management. Unfortunately, traditional cybersecurity training is often dense, theoretical, and unengaging for students and everyday internet users.

To bridge this gap, Week 1 establishes the foundation of the Cybersecurity Awareness Game—an interactive, desktop-based educational application designed to gamify cybersecurity learning. Built using Java Swing and SQLite, the project combines structured multi-module quizzes, dual-language localization (English & Hinglish), hands-on mini-game simulations, and persistent user progress tracking into a clean, modular architecture.

# 🎯 2. Core Problem Statement & Solution Architecture
The Challenge: Creating a lightweight, offline-accessible learning tool that makes digital hygiene rules intuitive, engaging, and accessible to a regional audience without requiring complex web infrastructure.

Our Solution: An engineered desktop application implementing a strict Model-View-Controller (MVC) design pattern to cleanly decouple presentation elements, business logic, and database persistence.

Key Value Propositions:
Bilingual Accessibility: Seamless switching between Hinglish and English instruction modes, broadening the user reach.

Gamified Reinforcement: Integration of a dedicated practice arena (CyberGameArena) featuring real-time password strength evaluation, safe browsing simulators, and phishing URL detectors.

Robust Data Persistence: Embedded SQLite transactional storage (cybergame.db) that records user profiles, language preferences, and performance scores securely.

Fault-Tolerant Multimedia: Programmatic audio fanfare generation and particle-based celebrations (PartyPopperCelebrationDialog) isolated via multi-threading to ensure zero UI thread starvation.

# 🛠️ 3. Technical Stack & Engineering Specifications
The project utilizes a robust, industry-standard technology stack optimized for desktop environments:

Core Programming Language: Java (JDK 17+)

GUI & Rendering Framework: Java Swing, AWT, Custom Anti-Aliased Graphics (Graphics2D, Custom ShapeButton components)

Architectural Pattern: Model-View-Controller (SoC - Separation of Concerns)

Database Management System: SQLite via JDBC (sqlite-jdbc driver) for ACID-compliant local storage

Concurrency & Safety: Dedicated background worker threads for audio synthesis and timer loops, protecting the Event Dispatch Thread (EDT)

# 📂 4. Modular Codebase Scaffolding
To maintain high cohesion and low coupling, the project repository is structured into five distinct, decoupled component classes:

## Cybersecurity-Awareness-Game/
│
├── src/
│   │
│   ├── cybergame/
│   │   ├── CyberMain.java         # Application Entry Point & Native Look-and-Feel Bootstrap
│   │   ├── CyberModel.java        # State Repository, Multi-Language Dataset & Quiz Banks
│   │   ├── CyberView.java         # UI Theme Palettes & Reusable Rounded Custom Components
│   │   ├── CyberController.java   # Business Logic, Quiz Engine, CardLayout Routing & JDBC Bridge
│   │   └── CyberGameArena.java    # Interactive Mini-Games Sandbox & Threat Simulators
│
├── docs/                          # Engineering artifacts, SRS documents, and UML specifications
├── assets/                        # Audio wave generators and multimedia UI assets
├── .gitignore                     # Exclusion rules for local SQLite databases (.db) and bytecode (.class)
└── README.md                      # Comprehensive system documentation index
✔️ 5. Week 1 Milestones & Deliverables Checklist
[x] Concept Finalization & Feasibility: Defined project scope around 5 essential threat modules (Phishing, Passwords, Malware, Social Engineering, Safe Browsing).

[x] Architectural Blueprint: Established strict MVC boundaries across CyberMain, CyberModel, CyberView, CyberController, and CyberGameArena.

[x] Localization Architecture: Implemented a 3D jagged array structure (String[][][]) for rapid, index-bound bilingual content switching.

[x] Database Schema Initialization: Configured SQLite auto-creation logic for secure user session and score tracking tables.

[x] Repository Structuring: Initialized professional Git repository hierarchy and version control baseline.

# ⏭️ 6. Roadmap Preview: Week 2 Objectives
Software Requirements Specification (SRS): Formalizing functional actors, use-case boundaries, and non-functional performance criteria.

UML System Modeling: Constructing detailed Class Diagrams and Sequence Diagrams mapping the exact method invocation flow between controller logic and database transactions.
