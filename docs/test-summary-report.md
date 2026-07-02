# Test Summary Report

## Project Overview

This report summarizes the manual testing results for the DemoBlaze e-commerce demo website.

The testing focused on the main user flows, including product browsing, categories, product details, cart functionality, checkout, sign up, log in, contact form and navigation.

## Test Execution Summary

| Metric | Result |
|---|---:|
| Total Test Cases | 25 |
| Passed | 21 |
| Failed | 4 |
| Blocked | 0 |
| Pass Rate | 84% |

## Tested Areas

The following areas were tested:

- Home page
- Product list
- Product categories
- Product detail pages
- Add to cart
- Cart page
- Checkout / Place Order
- Sign up
- Log in / Log out
- Contact form
- About us modal
- Navigation
- Cart total calculation

## Failed Test Cases

| Test Case ID | Area | Issue |
|---|---|---|
| TC-003 | Phones category | Pagination button redirects user back to main product list |
| TC-004 | Laptops category | Pagination buttons redirect user back to main product list |
| TC-005 | Monitors category | Pagination buttons redirect user back to main product list |
| TC-022 | Contact form | Contact form can be submitted with empty fields |

## Confirmed Bugs

| Bug ID | Title | Severity | Priority |
|---|---|---|---|
| BUG-001 | Multiple products use duplicate or very similar images | Low | Medium |
| BUG-002 | Pagination buttons reset selected product category | Medium | Medium |
| BUG-003 | Inconsistent product title capitalization | Low | Low |
| BUG-004 | Payment fields accept invalid text values | Medium | Medium |
| BUG-005 | Order can be placed with an empty cart | High | High |
| BUG-006 | Contact form can be submitted with empty fields | Medium | Medium |

## Observations

During testing, some temporary delays were observed in cart update, sign up and login feedback. However, these issues were not consistently reproduced during retesting, so they were documented as observations instead of confirmed bugs.

Additional observations:
- Product cards sometimes loaded with a short visible delay.
- The cart page layout looks visually unpolished.
- The Place Order modal may require scrolling at 100% browser zoom.
- Some product images and product names could be improved for better consistency.

## Overall Result

The main website functionality works in most tested areas, including product browsing, adding products to cart, checkout with filled fields, sign up, login, logout and navigation.

However, several issues were found in category pagination, form validation, checkout logic and content consistency. The most important issue is that the website allows an order to be placed with an empty cart.

## Conclusion

The DemoBlaze website is usable for basic e-commerce flows, but it has several validation, navigation and content quality issues that should be fixed to improve the user experience and reliability of the application.