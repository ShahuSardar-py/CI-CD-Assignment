# ID Card Webpage

A simple Node.js application that serves an ID card webpage.

## Installation

1. Install dependencies:
   ```
   npm install
   ```

2. Start the server:
   ```
   npm start
   ```

3. Open your browser and go to `http://localhost:3000`

## Description

This webpage displays an ID card for Shahu Sardar, Software Engineer Trainee at Equation Works.

## CI/CD

A GitHub Actions workflow is included to build a Docker image and push it to an AWS ECR repository when commits are pushed to the `main` branch.

Secrets required:
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_REGION`
- `AWS_ACCOUNT_ID` (used when constructing the image URI)
- `ECR_REPOSITORY` (the name of the ECR repository, e.g. `my-repo`)

The workflow file is located at `.github/workflows/deploy-to-ecr.yml`. Adjust the docker build or tagging logic as needed.