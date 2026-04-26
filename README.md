# 🏗️ Vaultrix-CI: Reusable CI/CD Infrastructure

The central nervous system for all automation within the Vaultrix ecosystem. This repository contains shared GitHub Actions and Reusable Workflows to ensure consistent security and build standards across all microservices.

## 🧩 Shared Resources

- **.github/actions/notify**: A universal composite action for Slack and SMTP (Gmail) notifications with rich attachment support.
- **.github/workflows/parent-ci.yaml**: The primary reusable pipeline performing:
  - SonarQube Quality Gate analysis.
  - Snyk SCA vulnerability scanning.
  - Optimized multi-stage Docker builds.
  - Trivy Container security scanning.
  - Production-ready image pushing to GHCR.

## 🔌 Integration
Microservices integrate with this repo by calling the reusable workflow in their CI configs:
```yaml
uses: Vaultrix-in/Vaultrix-CI/.github/workflows/parent-ci.yaml@main
```


## 🛡️ Security & Quality
This repository is part of the Vaultrix Secure Software Development Lifecycle (SDLC):
- **SonarQube**: Static analysis & Quality Gate.
- **Snyk**: Open-source vulnerability scanning.
- **Trivy**: Container image security scanning.

## 🤝 Support
For internal support, please reach out to the DevOps team or open an issue in the **Vaultrix-Helm** repository.

---
© 2026 Vaultrix Platform. All rights reserved.
