# Interview Questions — From This Project

> Ye sawaal is project ke design decisions se bante hain.
> Har sawaal ke neeche apna answer likh — interview mein aise hi puchenge.

---

## Design & Architecture

### Q1: File-based persistence vs Database — kab kya use karoge?
- **Context:** Is project mein JSON files (users.json, trains.json) use ho rahi hain as database
- **Expected Answer:** (tu likh)
- **Follow-up:** Concurrent users hain toh kya hoga?

### Q2: Service layer mein har call pe new TrainService() banaana — kya problem hai?
- **Context:** `UserBookingService.getTrains()` mein har baar `new TrainService()` banta hai jo file read karta hai
- **Expected Answer:** (tu likh)
- **Follow-up:** Singleton pattern yahan sahi hoga? Kya trade-offs hain?

### Q3: Password plaintext store karna vs hashing — explain the threat model
- **Context:** Is project mein BCrypt use ho raha hai, lekin `User` object mein `password` field bhi hai plain
- **Expected Answer:** (tu likh)

---

## Debugging & Bug Fixing

### Q4: `cancelBooking()` mein double removeIf — kya hoga?
- **Context:** Lines 84 aur 87 mein same list pe do baar removeIf call ho raha hai
- **Expected Answer:** (tu likh)

### Q5: Scanner.nextInt() ke baad kya crash ho sakta hai?
- **Context:** User non-integer input de toh InputMismatchException
- **Expected Answer:** (tu likh)

---

## System Design (Scaling Up)

### Q6: Agar ye system 10,000 concurrent users handle kare, toh kya changes karoge?
- **Expected Answer:** (tu likh)

### Q7: Seat booking mein race condition kaise handle karoge?
- **Context:** Do users same seat book karein simultaneously
- **Expected Answer:** (tu likh)
