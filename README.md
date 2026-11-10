# Community Learning Center Management System

**Name:** Harvey yuan A. Flores
**Section:** BSIT 3.8
**Course:** Mobile Development – Midterm Laboratory Examination

## Description
A Dart console application that registers learning resources and participants
(students and instructors), processes borrow/return transactions, and displays
organized records.

## Implemented Features
- Menu-driven console interface that loops until the user exits
- Add learning resources (title, category, price, copies)
- Register students and instructors
- Borrow and return resources with rule checks (borrow limits, availability)
- View resources, participants, and all records
- Input validation and error handling (no crashes on bad input)
- OOP: abstract class `CenterRecord`; subclasses `LearningResource`, `Student`,
  `Instructor`; mixin `Timestamped`; encapsulation with private fields
- Collections: `List` for resources, `Map` for participants

## Sample Test Scenarios
1. **Normal flow:** Add resource "Dart Basics" (copies: 2) → register a student →
   borrow R001 for P001 → view participants. Expected: borrow recorded, count 1/3.
2. **Invalid input:** Enter "abc" for the number of copies, then "-5" for price,
   and "9" at the menu. Expected: clear error messages, program keeps running.
3. **Rule violation:** Borrow the same resource twice with the same participant,
   or borrow when copies are 0. Expected: error message, no crash.
4. **Polymorphism:** Choose option 7. Expected: resources, students and
   instructors each display their own format.

## How to Run
1. Install the Dart SDK (https://dart.dev/get-dart).
2. Open a terminal in the project folder.
3. Run: `dart run main.dart`
(Or paste `main.dart` into DartPad/another Dart console environment.)
