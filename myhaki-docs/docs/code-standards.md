# Code Standards


## <h2>Frontend (Next.js, TypeScript, Tailwind, PWA)</h2>

- **Components:** Always use functional components for consistency and performance.
- **Naming:**
  - camelCase for variables and functions
  - PascalCase for component names
  - SCREAMING_SNAKE_CASE for constants
- **Files:** One component per file. Group by feature/module for maintainability.
- **Testing:** Use Jest and React Testing Library for unit tests; add tests for each new component or logic.
- **Styling:** Tailwind CSS only. Avoid inline styles unless absolutely necessary.
- **Accessibility:** All UI should meet WCAG AA standards. Use semantic HTML and aria attributes.

---

## <h2>Mobile (Android, Jetpack Compose, Kotlin)<h2>

- **Architecture:** MVVM, repository pattern, Koin for DI.
- **Naming:**
  - camelCase for variables and methods
  - PascalCase for classes, composables, ViewModels
  - SCREAMING_SNAKE_CASE for constants
- **File Structure:** Group by feature, separate data/model/viewmodel/ui.
- **Testing:** Use JUnit, MockK for unit tests; Compose Test for UI.
- **Dependency Injection:** Always inject dependencies via Koin modules.
- **Secure Storage:** Use EncryptedSharedPreferences for sensitive data.
- **Accessibility:** Use Compose’s accessibility APIs for labels, hints, focus.

---

## <h2>Backend (Django, DRF, Python)<h2>

- **Naming:**
  - snake_case for variables, functions, files
  - PascalCase for classes and models
- **Structure:** Place serializers/views in separate files unless tightly coupled.
- **Testing:** Use Django’s built-in test runner (`python manage.py test`), aim for >90% coverage.
- **API:** Follow REST conventions, use OpenAPI schema.
- **Security:** Validate all input, use Django’s CSRF and authentication mechanisms.

---

## <span style="font-weight: 600; color: #A87352;">General Standards</span>

- **Linting:**
  - Prettier + ESLint for frontend
  - ktlint for Android/Kotlin
  - flake8 and black for backend
- **Pull Requests:**
  - Write clear summaries for every PR
  - Link related issues (use `Fixes #issue_num`)
  - At least one reviewer before merging
  - Pass all CI checks (tests, lint)
- **Documentation:**
  - Use JSDoc (frontend), KDoc (Android), Python docstrings (backend)
  - Update README and feature docs for major changes
- **Branding & Design:**
  - Follow MyHaki brand guidelines for colors, typography, logos
    - See [Brand Guideline Reference](images/brand-guideline.png)
  - Keep UI consistent with Figma designs

---

## <span style="font-weight: 600; color: #A87352;">Accessibility & Values</span>

- **Accessibility:** All UIs must be usable by keyboard, screen reader, and on low-bandwidth devices.
- **Values:** Code and UI should always reflect MyHaki’s core values: Justice, Integrity, Accessibility.

---

## <span style="font-weight: 600; color: #A87352;">Best Practices</span>

- Keep functions and components small, focused and reusable.
- Prefer composition over inheritance.
- Avoid commented-out code in committed files.
- Refactor and remove unused code regularly.
- Always run lint and all tests before pushing or merging.
- Use environment variables for secrets (never commit credentials).

---

## <span style="font-weight: 600; color: #A87352;">References</span>

- [Brand Guideline](images/brand-guideline.png)
- [API Reference](api-reference.md)
- [Developer Docs](developer-docs.md)
- [QA Process](qa-process.md)

---