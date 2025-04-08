# Module-20-Homework-GitHub-Actions-CICD-Setup

## Project Overview

This project demonstrates a full CI/CD pipeline using GitHub Actions for a full-stack application.

- Test pipeline: Runs Cypress component tests when a Pull Request is made to the `develop` branch.
- Deploy pipeline: Deploys the application to Render when code is merged to the `main` branch.

The goal is to ensure code quality and automated deployment for clean and reliable production workflows.

---

## User Story

**As** a software engineer looking to integrate a CI/CD pipeline in a codebase  
**I want** a full-stack application that runs test cases when a Pull Request is made to the develop branch and automatically deploys to Render when the code is merged to main  
**So that** I can ensure that all code integrations are clean and pass the proper requirements and that the application is constantly updated when major releases are made to the main branch

---

## Acceptance Criteria Checklist

- [x] Pull Requests to `develop` run Cypress component tests
- [x] GitHub Actions show test results clearly in the "Actions" tab
- [x] Merging `develop` into `main` triggers deployment to Render
- [x] Render deploy hook is securely stored in GitHub Secrets

---

## GitHub Actions Workflows

### Cypress Component Tests (`.github/workflows/test.yml`)

Runs Cypress tests on every Pull Request to the `develop` branch.

Check the `test.yml` file in this repository.

### Deploy to Render (`.github/workflows/deploy.yml`)

Triggers deployment on every push to the `main` branch.

Check the `deploy.yml` file in this repository.

**Note:**  
Render deploy hook URL is stored as a secret in GitHub:
- Go to **Settings > Secrets > Actions > New repository secret**
- Name: `RENDER_DEPLOY_HOOK_URL`
- Value: *(Your Render deploy hook URL)*

---

## How to View GitHub Actions Logs

1. Go to your GitHub repository.
2. Click the **Actions** tab.
3. Select the workflow run:
   - Cypress Component Tests (PR to `develop`)
   - Deploy to Render (Push to `main`)
4. Click any step to expand logs and view outputs.
5. Screenshot the workflow for proof or copy the URL of the workflow run for submission!

## Credits

N/A

## License

Please refer to the LICENSE in the repository.