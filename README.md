# 💻 Test Automation Framework | API 

[![Playwright](https://img.shields.io/badge/Playwright-34495E?style=for-the-badge&logo=playwright&logoColor=white)](https://playwright.dev/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://js.org/index.html) 

[![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://code.visualstudio.com/)
[![Playwright HTML Reporter](https://img.shields.io/badge/Playwright%20HTML%20Reporter-<COLOR>?style=for-the-badge&logo=playwright&logoColor=white)](https://www.npmjs.com/package/playwright-html-reporter)
[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)](https://github.com/features/actions) 

## 📑 Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Running Tests](#running-tests)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Continuous Integration](#continuous-integration)
- [Reporting](#reporting)

## 📖 Introduction
This repository contains a Test Automation Framework built using Playwright and Javascript for automated testing of REST APIs.

## 🛠️ Prerequisites

- [![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/) (v18.16.1 or higher recommended)
- [![npm](https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white)](https://www.npmjs.com/) (v9.5.1 or higher recommended)

## ▶️ Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/sayan-tan/playwright-api-automation.git
   ```

2. Navigate to the project directory:

   ```bash
   cd playwright-api-automation-framework
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

## 🚀 Running Tests

  ```bash
  npm run playwright:tests
  ```

## 📁 Project Structure

The tests follow a modular and maintainable structure:

```
|-- .github
|     |-- workflows
|          |-- 01_api_tests.yml
|          |-- 02_api_tests_select_env.yml
|-- test-data
|     |-- login
|          |-- login-successful.json
|          |-- login-unsuccessful.json
|     |-- register
|          |-- register-successful.json
|          |-- register-unsuccessful.json
|     |-- users
|          |-- user_create.json
|          |-- user_update_patch.json
|          |-- user_update_put.json
|-- tests-reqres
|     |-- login.spec.js
|     |-- register.spec.js
|     |-- users.spec.js
|-- utils
|     |-- EndpointUtils.js
|     |-- RequestBodyUtils.js
|     |-- RequestUtils.js
|     |-- ResponseUtils.js
|     |-- VerificationUtils.js
|-- .gitignore
|-- package.json
|-- playwright.config.js
```

- `playwright-report`: Contains the HTML report for tests (Logs are attached).
- `test-data`: Contains external files (example: user create/update data) that can be used to mock data during tests.
- `tests-reqres`: Contains the actual test files. You can organize your tests into subdirectories as needed. 
- `utils`: Contains the Utilities that provide methods for asserting different conditions on web elements, handling requests, and responses.

## ⚙️ Configuration

- Modify `playwright.config.js` for playwright configuration settings such as
  - `baseURL`
  - `testDir`
  - `reporter`

## 🔄 Continuous Integration

This project is configured for CI using GitHub Actions. Check the configurations in `.github/workflows/*.yml`.

- `01_api_tests.yml`: This workflow executes tests in a pre-defined environment PROD.
- `02_api_tests_select_env.yml`: This workflow will first ask the User to select the environment (DEV / Pre-PROD / PROD) for test execution.

## 📊 Reporting

The Playwright HTML report (Logs are attached) is stored in the `playwright-report` directory.
