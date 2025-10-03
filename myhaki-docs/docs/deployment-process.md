# Deployment Process



## <span style="font-weight: 600; color: #A87352;">Frontend Deployment (LSK Dashboard & Informational Site)</span>

- **Platform:** Vercel (Next.js/Tailwind)
- **Branch:** Auto-deployment from `main`
- **Environment Variables:** Managed securely via `.env` in Vercel dashboard
- **Build & Preview:** Each PR triggers preview builds; production deploys on merge to `main`
- **Brand Compliance:** Ensure final builds use MyHaki colors, fonts, and logo ([see Brand Guideline](images/brand-guideline.png))

---

## <span style="font-weight: 600; color: #A87352;">Mobile Deployment (Android App)</span>

- **Platform:** Google Play Console (Production), Firebase App Distribution (Testing)
- **Build:** Release builds via Gradle (`assembleRelease`), signed with team keystore
- **Environment Variables:** API URLs, keys stored in `local.properties` and encrypted secrets
- **CI:** GitHub Actions runs unit/UI tests on push; releases only after passing all tests
- **Brand Compliance:** All assets, colors, and typography must match MyHaki guidelines

---

## <span style="font-weight: 600; color: #A87352;">Backend Deployment (Django REST API)</span>

- **Platform:** Heroku (Staging & Production)
- **Branch:** Deploy from `main`
- **Environment Variables:** Managed securely in Heroku dashboard; never commit secrets
- **Scaling:** Automatic scaling via Heroku dynos based on demand
- **Rollback:** Previous stable releases can be redeployed via Heroku dashboard

---

## <span style="font-weight: 600; color: #A87352;">AI Agent Deployment (FastAPI)</span>

- **Platform:** Google Cloud Platform (Cloud Run, GKE, or Compute Engine)
- **Build:** Dockerized FastAPI microservice
- **Environment Variables:** Managed in Google Cloud Secret Manager
- **Scaling:** Automatic scaling via Google Cloud Run/GKE
- **Monitoring:** Use Google Cloud Monitoring for logs, alerts, and uptime

---

## <span style="font-weight: 600; color: #A87352;">CI/CD Pipeline</span>

- **Tool:** GitHub Actions
- **Pre-Deployment:** All codebases run tests, build, and lint checks before deploy
- **Automation:** Automatic deployment on merge to `main`
- **Status:** Build/test status visible in PRs and repository dashboard
- **Security:** Secrets scanned before deploy, API keys never exposed

---

## <span style="font-weight: 600; color: #A87352;">Deployment Flow Diagram</span>

![Deployment Architecture](images/deployment-diagram.png)
*Request this diagram from the DevOps team or generate via Lucidchart/Figma if missing*

---

## <span style="font-weight: 600; color: #A87352;">Release Checklist</span>

- [ ] All tests passing (unit, integration, UI)
- [ ] Linting with zero errors
- [ ] Secrets verified (no `.env` in repo)
- [ ] Brand assets up to date
- [ ] Team notified of release

---

## <span style="font-weight: 600; color: #A87352;">References</span>

- [Brand Guideline](images/brand-guideline.png)
- [Code Standards](code-standards.md)
- [QA Process](qa-process.md)
- [API Reference](api-reference.md)

---