# Bug Tracker — Train Ticket Booking System

| # | File | Line(s) | Severity | Description | Status |
|---|------|---------|----------|-------------|--------|
| 1 | `UserBookingService.java` | 25 | 🔴 Critical | `USER_FILE_PATH` = `"app/src/main/java/ticket/booking/localDb/users.json"` — case mismatch (`localDb` vs `localDB`), will fail on case-sensitive OS (Linux/Mac) | Open |
| 2 | `TrainService.java` | 19 | 🔴 Critical | `TRAIN_DB_PATH = "../localDB/trains.json"` — relative path, depends on working directory. Will break if app is run from different location | Open |
| 3 | `UserBookingService.java` | 72-95 | 🔴 Critical | `cancelBooking()` — double `removeIf` call on same list. First removes ticket, second tries again on already-modified list. Also takes `ticketId` param but immediately overwrites it with Scanner input | Open |
| 4 | `App.java` | 39 | 🟡 Medium | `trainSelectedForBooking` is created inside while loop but used across switch cases (case 4 sets it, case 5 uses it). Variable scope is wrong — if user goes to case 5 without case 4, they get empty Train | Open |
| 5 | `App.java` | 79 | 🟡 Medium | `trains.get(scanner.nextInt())` — no bounds check. User types 0 but list is 1-indexed in display. Off-by-one error | Open |
| 6 | `App.java` | 71-77 | 🟡 Medium | `index` variable initialized to 1 but never incremented in the for loop. All trains show as "1 Train id: ..." | Open |
| 7 | `App.java` | 38 | 🟡 Medium | `scanner.nextInt()` — no `InputMismatchException` handling. User types "abc" → crash | Open |
| 8 | `App.java` | 52 | 🟢 Low | Login prompt says "Enter the password to signup" — copy-paste typo, should be "to login" | Open |
| 9 | `App.java` | 54 | 🟡 Medium | Login creates new `User` with `UUID.randomUUID()` — but existing user already has a userId. Login should find existing user, not create new one | Open |
| 10 | `User.java` | 7-10 | 🟢 Low | Lombok `@Getter`, `@Setter`, `@Data`, `@Builder` imported but not used — all getters/setters written manually | Open |
| 11 | `Train.java` | 17 | 🟡 Medium | `@Builder` annotation present but no `@AllArgsConstructor` — Lombok builder won't work properly without it at compile time (needs annotation processing) | Open |
| 12 | `trains.json` | 1-42 | 🟡 Medium | Both trains have same `train_id: "bacs"` and `train_no: 12345` — duplicate data, no unique identity | Open |
| 13 | `UserBookingService.java` | 100 | 🟡 Medium | `new TrainService()` created on every `getTrains()` call — reads entire JSON file each time. No caching, no reuse | Open |
| 14 | `App.java` | 103-104 | 🟢 Low | Case 6 (Cancel Booking) not implemented in switch — falls through to default silently | Open |
