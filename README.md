# QA Bug Hunt Pack: DemoBlaze Manual Testing Project

## Overview
Manual QA testing project for the DemoBlaze e-commerce demo website.

## Goal
The goal of this project was to practice and demonstrate manual QA skills by preparing test documentation, executing test cases, documenting bugs and summarizing test results.

## Website Under Test
https://www.demoblaze.com

## Tools Used
- Google Chrome
- Google Sheets / Excel
- Markdown
- GitHub
- Screenshots and screen recordings
- Manual testing

## What Was Tested
- Home page
- Product categories
- Product details
- Cart
- Checkout
- Sign up
- Log in / Log out
- Contact form
- Navigation

## Test Results
| Metric | Result |
|---|---:|
| Total Test Cases | 25 |
| Passed | 21 |
| Failed | 4 |
| Blocked | 0 |
| Pass Rate | 84% |

## Main Bugs Found
- Pagination buttons reset selected product category
- Payment fields accept invalid text values
- Order can be placed with an empty cart
- Contact form can be submitted with empty fields
- Multiple products use duplicate or very similar images
- Inconsistent product title capitalization

## Project Structure

qa-bug-hunt-pack/
 - README.md
 - docs/
   -  test-plan.md
   -  test-scenarios.md
   -  bug-reports.md
   -  test-summary-report.md
 -  tests/
   -  test-cases.xlsx
 - screenshots/

## What I Learned

Through this project, I practiced:
- Writing manual test cases
- Executing functional and negative tests
- Documenting actual vs expected results
- Reporting bugs with severity and priority
- Retesting issues before confirming bugs
- Separating confirmed bugs from temporary observations
- Creating a structured QA summary report

## Future Improvements

- Add a QA dashboard in Excel or Power BI
- Add more exploratory test cases
- Test the website on different browsers
- Add mobile/responsive testing
- Create automated UI tests in the future
