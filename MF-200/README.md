# 📱 MF-200 Flutter Task: Offline-First Todo & Notes App

## 📝 Description
Build an advanced, production-grade Todo and Notes application that operates primarily offline using a local database, and automatically synchronizes data with a remote server/mock API whenever an active internet connection is available.

---

## 🛠️ Technical Requirements

### 1. UI & Performance Optimization
*   Implement a highly reactive and intuitive user interface to manage tasks and notes.
*   Ensure the task list updates instantly upon addition, modification, or deletion of any item.
*   Optimize widget rebuilds efficiently; avoid rebuilding the entire Widget Tree unnecessarily by utilizing specific keys (`ValueKey` / `ObjectKey`) and constant widgets where applicable.

### 2. API & Network Layer
*   Integrate the application with a Mock API (e.g., [JSONPlaceholder](https://jsonplaceholder.typicode.com/) or a custom [Supabase](https://supabase.com/) instance).
*   Construct a centralized network layer using `Dio` (or `http`) equipped with `Interceptors`.
*   Implement a robust error handling system capable of detecting and gracefully differentiating between various failure states (e.g., No Internet Connection, Server Error, and Validation Errors), displaying descriptive alerts to the user.

### 3. Local Database & Offline-First Architecture
*   Design a reliable relational or document-based local storage system using `Hive` or `SQLite` (`Sqflite`).
*   Enforce a strict **Offline-First Approach**:
    *   Upon application launch, the UI must immediately fetch and display cached data from the Local DB.
    *   In the background, trigger an asynchronous network request to fetch updated data from the remote API, silently update the Local DB, and smoothly reflect changes on the UI without causing friction or freezing.

### 4. Architecture, Clean Code & Testing
*   Structure the repository following architectural patterns such as **Clean Architecture** (Data, Domain, Presentation layers) or a **Feature-First Modularization**.
*   Adhere to **SOLID** principles, specifically leveraging Dependency Inversion for service injection using packages like `GetIt` or state injection via `Providers` / `BLoC`.
*   Write comprehensive **Unit Tests** for your business logic components (e.g., testing `BLoC` states or `ChangeNotifiers`). Use mocking frameworks (`mockito` or `mocktail`) to decouple and isolate the API dependencies during tests.

---

## 🎯 Technical Success Criteria
*   **Solid & Clean Code:** The architecture must cleanly separate the data tracking logic from presentation widgets, establishing a scalable and maintainable codebase.
*   **Robust Error Handling:** The application must remain resilient under stress, maintaining seamless user interaction and complete data integrity when transitioning between offline and online states.

---

## 🚀 Submission Protocol

1. Create a new **Private or Public Repository** on your personal GitHub account and push your code there.
2. Ensure your repository includes a detailed `README.md` explaining the architecture choices, state management used, and instructions on how to run the app and tests.
3. Return to our main Tasks repository and open a **New Issue**.
4. Use the following title format for your Issue: `submission/MF-200: YourName`.
5. Inside the Issue body, provide the **link to your personal repository** along with any relevant screenshots or a short video recording demonstrating the offline capability.
6. Wait for the Tech Lead's review; feedback and code discussions will take place directly within the comments of your Issue.