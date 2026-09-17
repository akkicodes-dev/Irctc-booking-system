# Concept Notes — Train Ticket Booking System

> Har concept ke neeche apne words mein explanation likh.
> Mentor sirf heading aur bullets dega, content TERA hai.

---

## Session 1 — 2026-09-17

### Absolute Path vs Relative Path
- Absolute path: full path from root (e.g., `D:\folder\file.json`) — machine-specific, breaks on other systems
- Relative path: path relative to where program runs (e.g., `app/src/.../file.json`) — portable
- Lesson: never hardcode absolute paths in source code
- (Ab tu apne shabdon mein isko bhar — kya galti ki thi aur kyun)

### Gradle Build System Basics
- `settings.gradle` — project name, plugins, subproject includes
- `build.gradle` — dependencies, Java version, main class
- `gradle clean installDist` — recompile + create runnable distribution
- Gradle daemon caches old builds — `clean` forces fresh compile
- (Ab tu apne shabdon mein isko bhar)

### Method Return Values — Ignore Mat Kar
- `loginUser()` returns Boolean — agar result check nahi kiya toh login verify hi nahi hoga
- Pattern: `if (object.method()) { success } else { fail }`
- Seedha `if` mein method call kar sakte hain — alag variable optional hai
- (Ab tu apne shabdon mein isko bhar)

### File Path Case Sensitivity
- Windows pe `localDb` = `localDB` (case-insensitive filesystem)
- Linux/Mac pe `localDb` ≠ `localDB` (case-sensitive filesystem)
- Code hamesha exact case use karo — cross-platform compatibility ke liye
- (Ab tu apne shabdon mein isko bhar)
