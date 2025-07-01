# GoRest API: CRUD Operations Automated Tests

![CI](https://github.com/saranyanumpy/GoRest-API-CRUD-Operations/actions/workflows/run-newman-tests.yml/badge.svg)

This repository contains automated API tests for the **GoRest API** using **Postman** and **Newman**.  
It covers various CRUD operations to validate API endpoints and is integrated with **GitHub Actions** for CI/CD.  
The tests run automatically on every push or pull request.

## 🚀 CI/CD Pipeline

✅ Runs on every `push` or `pull request` to `main`  
✅ Automatically executes Postman tests using Newman  
✅ Generates rich HTML reports using `newman-reporter-htmlextra`  
✅ Uploads reports as downloadable artifacts in GitHub Actions  

## 📊 Report Example

The report artifact is generated on each CI run.  
👉 Download it from the **Actions run page** under `Artifacts`.

## 🛠 How to run locally

```bash
npm install -g newman newman-reporter-htmlextra
newman run "postman/GoRest API- CRUD Operations.postman_collection.json" \
  -e "postman/GoRest-QA.postman_environment.json" \
  -d "data/GoRest.csv" \
  -r cli,htmlextra --reporter-htmlextra-export ./newman-report.html
