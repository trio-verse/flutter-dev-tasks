# 📱 Junior Flutter Task: Meal Browser App

## 📝 Description
Build a simple 2-screen Flutter application that fetches food categories from a public API, allows users to browse meals within each category, and enables them to save their favorite meals locally.

---

## 🛠️ Technical Requirements

### 1. UI & Framework Core
*   Implement exactly two screens:
    *   **Categories Screen:** Displays a list/grid of food categories fetched from the API.
    *   **Meal Details Screen:** Displays the details of the selected meal (image, ingredients, and instructions).
*   Ensure the layout is fully responsive and error-free across different screen sizes (**Correct Design**), with no UI clipping or overflows.

### 2. API & Data Handling
*   Integrate with any free public food API (Recommended: [TheMealDB API](https://www.themealdb.com/api.php)).
*   Parse the incoming JSON payloads into strongly-typed Dart Models using a `factory constructor` (e.g., `fromJson`).
*   Strictly adhere to Dart's Null Safety practices to handle potential null fields from the API and prevent application crashes (**Crash-free**).

### 3. Local Databases & Caching
*   Use `SharedPreferences` to locally store the IDs of the meals that the user adds to their favorites.
*   The favorited meals must persist and remain saved even after the application is closed and reopened.

### 4. Clean Code & Architecture
*   Separate your business logic from the UI widgets using either a clean `setState` approach or a basic `BLoC` implementation.
*   Structure your project folders logically (e.g., separating data models from UI screens).
*   Configure and respect the rules defined in `analysis_options.yaml` (Linter) to ensure clean code formatting.

---

## 🎯 Technical Success Criteria
*   **Crash-free:** The application must handle exceptions gracefully (e.g., No Internet, empty API responses) without crashing.
*   **Correct Design:** The user interface must be clean, responsive, aligned, and entirely free of the black-and-yellow `RenderFlex overflowed` stripes.

---

## 🚀 Submission Protocol

1. Create a new **Private or Public Repository** on your personal GitHub account and push your code there.
2. Ensure your repository includes a simple `README.md` explaining how to run the app.
3. Return to our main Tasks repository and open a **New Issue**.
4. Use the following title format for your Issue: `submission/flutter-junior: YourName`.
5. Inside the Issue body, provide the **link to your personal repository** along with any relevant screenshots or a short video recording of the working app.
6. Wait for the Tech Lead's review; feedback and discussion will take place directly within the comments of your Issue.