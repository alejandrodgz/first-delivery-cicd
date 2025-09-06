# first-delivery-cicd

This project demonstrates a simple CI/CD pipeline using GitHub Actions.

## Overview

The goal is to set up automated workflows for building, testing, and deploying code using GitHub Actions. As part of this project, you will create your first workflow YAML file to automate these tasks.

## Getting Started

1. **Create a GitHub Actions Workflow:**
   - In your repository, navigate to `.github/workflows/`.
   - Create a new YAML file (e.g., `ci.yml`).

2. **Sample Workflow YAML:**
   ```yaml
   name: CI

   on: [push, pull_request]

   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - name: Set up Node.js
           uses: actions/setup-node@v3
           with:
             node-version: '16'
         - name: Install dependencies
           run: npm install
         - name: Run tests
           run: npm test
   ```

3. **Commit and Push:**
   - Commit your workflow file and push to GitHub.
   - GitHub Actions will automatically run the workflow on each push or pull request.

## Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Workflow syntax for GitHub Actions](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions)

---
This is the first delivery of CICD using GitHub Actions.
