# Postman API Automation Integration with Github Actions #

This repository is a POC for integrating Postman tests with GitHub Actions. The test execution is triggered
whenever changes are pushed to the main branch, and the workflow can also be executed manually using
workflow_dispatch. Cron jobs are configured to schedule workflow executions as required. Once the
execution is completed, the latest HTML test report is generated and published to GitHub Pages, which can
be accessed at https://sdet-manojgali.github.io/Phoenix-Inwarranty-Flow/. The latest HTML report is also
attached to an email notification sent to all team members.

## About Me ##
Hi, I'm Manoj. I have 4 years of experience in Automation Testing, with expertise in Playwright, Selenium, BDD, Rest Assured, Postman, and Java.
You can connect with me via: (https://www.linkedin.com/in/gali-manoj/)

## Testing Coverage ##
1) Happy Flow Testing
2) Negative Testing and Edge Case Testing
3) Token Testing
4) Data Driven Testing with CSV
5) Schema Validation
6) Secrets Management with Github Secrets

## Tech Stack ##
1) Postman
2) Node.js 22v & npm
3) Newman
4) newman-reporter-htmlextra
5) GitHub Actions
6) Gmail SMTP
7) CSV for Data Driven Testing
8) AWS EC2 Runner for Self-Hosted GitHub Runner

## GitHub Pages ##
You can directly view the latest html report of the postman test at the Github page Link: https://sdet-manojgali.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The Report will created in the newman folder
![Postman Report](https://github.com/SDET-ManojGali/Phoenix-Inwarranty-Flow/blob/static-content/newman-report.png)

## Project Structure ##
```
Phoenix-Inwarranty-Flow
├─ Inwarranty-flow Collection.postman_collection.json # Collection File
├─ QA.postman_environment.json # Environment File
└─ testData.csv # Test Data File

```

## How to run the project? ##
You can run the project on your local system for that:
1) Clone the project on Local System: https://github.com/SDET-ManojGali/Phoenix-Inwarranty-Flow.git
2) Install Node Js : https://nodejs.org/en/download
3) Install Newman using: ```npm install -g newman```
4) Install Newman Reporter htmlextra using: ```npm install -g newman-reporter-htmlextra```
5) Run the Collection in CLI using command:
    ```
    newman run 'Inwarranty-flow Collection.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testData.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
    ```
