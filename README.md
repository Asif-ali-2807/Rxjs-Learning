# RxJS Learning Roadmap (2026 Edition)

## 0. Prerequisites (The Foundation)
Before starting RxJS, ensure you are proficient in:
- [ ] **ES6+ Syntax:** Arrow functions, Destructuring, Spread/Rest.
- [ ] **Asynchronous JS:** Promises, Async/Await, and the Event Loop.
- [ ] **Functional Programming:** `map`, `filter`, `reduce`, and Pure Functions.
- [ ] **Observer Pattern:** Understanding Producers vs. Consumers.

---

## 1. Phase One: The Fundamentals
*Focus: How data moves from A to B.*
- **Observable:** The stream of data.
- **Observer:** The object that "listens" (next, error, complete).
- **Subscription:** Starting and stopping the stream (`.unsubscribe()`).
- **Creation Operators:** `of`, `from`, `fromEvent`, `interval`.

---

## 2. Phase Two: The Pipe & Basic Operators
*Focus: Manipulating data without leaving the stream.*
- **Pipeable Operators:** Using `.pipe()`.
- **Transformation:** `map`, `scan`, `pluck`.
- **Filtering:** `filter`, `take`, `first`, `debounceTime`, `distinctUntilChanged`.
- **Utility:** `tap` (for debugging/side effects).

---

## 3. Phase Three: The "Flattening" Operators
*Focus: Handling nested Observables (The hardest part).*
- **Higher-Order Observables:** Understanding `Observable<Observable<T>>`.
- **The Big Four:**
    - `switchMap`: Cancel previous, start new (Search/Routing).
    - `mergeMap`: Run all concurrently (Parallel requests).
    - `concatMap`: Run in sequence (Queued actions).
    - `exhaustMap`: Ignore new until current finishes (Login buttons).

---

## 4. Phase Four: State Management & Combination
*Focus: Making multiple streams work together.*
- **Subjects:** `Subject`, `BehaviorSubject` (Initial value), `ReplaySubject`.
- **Combination:** `combineLatest`, `withLatestFrom`, `forkJoin`, `zip`.
- **Multicasting:** `shareReplay` (To avoid multiple HTTP calls).

---

## 5. Phase Five: Advanced Patterns
*Focus: Production-ready code.*
- **Error Handling:** `catchError`, `retry`, `retryWhen`.
- **Testing:** Marble Diagrams (`-a-b-c-|`).
- **Schedulers:** Managing execution context (Queue, Asap, Async).
- **Memory Management:** `takeUntil(destroy$)` pattern.
