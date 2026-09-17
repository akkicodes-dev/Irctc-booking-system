# Progress Tracker — Train Ticket Booking System

## Current Status
- **Current Phase:** Phase 0 — Setup & Codebase Understanding
- **Last Session:** 2026-09-17
- **Next Step:** Fix remaining bugs (scanner.next() issue, cancel booking, TrainService path)

---

## Phase 0 — Setup & Codebase Understanding
- [x] Project structure review
- [x] Read all source files
- [x] Create docs/ artifacts (ARCHITECTURE, PROGRESS, NOTES, BUGS, INTERVIEW)
- [x] Build the project with Gradle — fixed compatibility issues (plugin, toolchain, stdin)
- [x] Run the app — tested signup, login, fetch bookings
- [x] Fix login flow — added loginUser() call with result check
- [x] Fix file path case bug (localDb → localDB)
- [x] Fix absolute path → relative path
- [ ] Fix remaining bugs: scanner.next() word splitting, cancel booking (case 6), TrainService path
- [ ] Understand each layer: entities, service, util, persistence
- [ ] Understand Jackson serialization/deserialization
- [ ] Understand BCrypt password hashing
- [ ] Git commit session 1 changes

## Phase 1 — Entities Deep Dive
- [ ] Why POJOs? What problem do they solve?
- [ ] Jackson annotations — @JsonNaming, @JsonIgnoreProperties
- [ ] Lombok — why imported but not used properly?
- [ ] Constructor design — why both no-arg and all-arg?
- [ ] Mutable vs immutable entity design

## Phase 2 — Service Layer
- [ ] UserBookingService responsibilities (SRP violation?)
- [ ] TrainService — file I/O on every call
- [ ] Error handling patterns
- [ ] The cancelBooking bug
- [ ] Stateless vs stateful service design

## Phase 3 — Persistence & Data
- [ ] JSON as database — trade-offs
- [ ] File path issues (relative paths, OS differences)
- [ ] Concurrent access problems
- [ ] Data integrity — what if write fails midway?

## Phase 4 — Testing
- [ ] Why test? What to test first?
- [ ] Unit tests for service layer
- [ ] Edge cases and boundary testing

## Phase 5 — Refactoring
- [ ] Apply SOLID principles
- [ ] Proper error handling strategy
- [ ] Input validation
- [ ] Separation of concerns in App.java

## Phase 6 — Advanced Topics (Queue)
- [ ] Migrate to a real database
- [ ] Add REST API layer
- [ ] Authentication & session management
- [ ] Concurrency & thread safety
