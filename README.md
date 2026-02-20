# CI/CD Demo

A minimal single-file static website built to demonstrate a GitHub Actions CI/CD pipeline — from code push to automated Docker build and deploy.

---

## Screenshot

```
┌─────────────────────────────────────┐
│         ● Pipeline Active           │
│                                     │
│          CI/CD Demo                 │
│                                     │
│  📝 Push → ⚙️ Build → ✅ Test → 🚀  │
│                                     │
│      [ Trigger Pipeline Alert ]     │
└─────────────────────────────────────┘
```

---

## Run Locally

No build tools needed. Just open the file:

```bash
open index.html
# or double-click index.html in your file manager
```

---

## Run with Docker

**Build the image:**
```bash
docker build -t cicd-demo .
```

**Run the container:**
```bash
docker run -p 8080:80 cicd-demo
```

**Open in browser:**
```
http://localhost:8080
```

---

## Project Structure

```
.
├── index.html   # The entire app (HTML + CSS + JS)
├── Dockerfile   # nginx:alpine serving index.html
├── .gitignore
└── README.md
```

---

## CI/CD Pipeline (GitHub Actions)

This project is designed to be wired into a GitHub Actions workflow that:
1. Triggers on every push to `main`
2. Builds the Docker image
3. Runs any validation/tests
4. Pushes the image to a container registry
5. Deploys to your hosting environment

---

## Tech Stack

- Pure HTML5 + CSS3 + Vanilla JS (zero dependencies)
- nginx:alpine for serving
- Docker for containerization
- GitHub Actions for CI/CD
