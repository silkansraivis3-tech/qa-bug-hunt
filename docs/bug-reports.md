# Bug Reports

This document contains bugs and usability issues found during manual testing of the DemoBlaze e-commerce demo website.

---

## BUG-001: Multiple products use duplicate or very similar images

**Severity:** Low  
**Priority:** Medium  
**Type:** UI / Content issue  

### Description
Several products use the same or very similar product images, even though they represent different product models. This may confuse users when comparing products, especially in the laptop and phone categories.

Examples observed:
- MacBook Air and MacBook Pro use the same or very similar image.
- Dell i7 6500U and Dell i7 7500U use the same or very similar image.
- Sony Vaio i5 and Sony Vaio i7 use the same or very similar image.
- Samsung Galaxy S6 and Samsung Galaxy S7 use the same or very similar image.

### Steps to Reproduce
1. Open https://www.demoblaze.com
2. Go to the product list or select the Laptops category.
3. Compare product images for MacBook, Dell and Sony Vaio products.
4. Go to the Phones category.
5. Compare product images for Samsung Galaxy S6 and Samsung Galaxy S7.

### Expected Result
Each product should have a unique and accurate image that matches the product model.

### Actual Result
Several different products use duplicate or very similar images, which makes it harder for the user to visually distinguish between products.

### Evidence
Screenshots:
- `screenshots\tc-002-bug-001-1.png`
- `screenshots\tc-002-bug-001-2.png`

### Related Test Cases
- TC-002: Product list is displayed
- TC-003: Phones category works
- TC-004: Laptops category works

## BUG-002: Pagination buttons reset selected product category

**Severity:** Medium  
**Priority:** Medium  
**Type:** Functional / Navigation issue  

### Description
Pagination buttons remain visible after selecting a product category. When the user clicks the Next or Previous button inside a selected category, the website redirects the user back to the main product list instead of keeping the selected category filter active.

This issue was observed in multiple categories:
- Phones category: Previous button remains visible and redirects the user back to the main product list.
- Laptops category: Next and Previous buttons remain visible and redirect the user back to the main product list.
- Monitors category: Next and Previous buttons remain visible and redirect the user back to the main product list.

### Steps to Reproduce
1. Open https://www.demoblaze.com
2. Click the Phones category.
3. Click the Previous pagination button.
4. Observe that the user is redirected back to the main product list.
5. Repeat the same test for Laptops and Monitors categories using the visible Next or Previous buttons.

### Expected Result
When a user selects a category, pagination should either:
- stay inside the selected category, or
- be hidden if the selected category does not have additional pages.

### Actual Result
Pagination buttons remain visible inside selected categories and redirect the user back to the main product list when clicked.

### Evidence
Video:
- `screenshots\tc-003-004-005-bug-002-003.mp4`

### Related Test Cases
- TC-003: Phones category works
- TC-004: Laptops category works
- TC-005: Monitors category works


## BUG-003: Inconsistent product title capitalization

**Severity:** Low  
**Priority:** Low  
**Type:** UI / Content consistency issue  

### Description
Some product names use inconsistent capitalization in the product list and product detail pages. For example, the product is displayed as “Samsung galaxy s6” instead of “Samsung Galaxy S6”.

This does not block the user from using the website, but it makes the product information look less professional and inconsistent.

### Steps to Reproduce
1. Open https://www.demoblaze.com
2. Go to the Phones category or view the product list on the home page.
3. Find the product “Samsung galaxy s6”.
4. Open the product detail page.
5. Check the product title capitalization.

### Expected Result
Product names should use consistent and correct capitalization, for example “Samsung Galaxy S6”.

### Actual Result
The product title is displayed as “Samsung galaxy s6”, with inconsistent capitalization.

### Evidence
Video:
- `screenshots\tc-003-004-005-bug-002-003.mp4`

### Related Test Cases
- TC-002: Product list is displayed
- TC-003: Phones category works
- TC-004: Laptops category works
- TC-006: Product details page opens



## BUG-004: Payment fields accept invalid text values

**Severity:** Medium  
**Priority:** Medium  
**Type:** Validation / Checkout issue  

### Description
The Place Order form accepts random text values in payment-related fields such as Credit card, Month and Year. The order can be completed even when these fields do not contain realistic numeric payment data.

This shows that the checkout form does not properly validate payment-related input formats.

### Steps to Reproduce
1. Open https://www.demoblaze.com
2. Add any product to the cart.
3. Go to the Cart page.
4. Click “Place Order”.
5. Fill in Name, Country and City.
6. Enter random text values in Credit card, Month and Year fields.
7. Click “Purchase”.
8. Observe the confirmation message.

### Expected Result
Payment-related fields should validate the expected format. Credit card should require a valid numeric card-like value, and Month and Year should require valid date-related numeric values.

### Actual Result
The form accepted random text values in Credit card, Month and Year fields and completed the purchase successfully.

### Evidence
Screenshot:
- `screenshots\tc-011-bug-004.png`

### Related Test Cases
- TC-010: Place order modal opens
- TC-011: Complete order with valid data


## BUG-005: Order can be placed with an empty cart

**Severity:** High  
**Priority:** High  
**Type:** Functional / Checkout logic issue  

### Description
The website allows the user to open the Place Order form and complete an order even when the cart is empty. The user still needs to fill in the required form fields, but the system does not check whether the cart contains any products before allowing the purchase.

This is a serious checkout logic issue because an order should not be possible without products in the cart.

### Steps to Reproduce
1. Open https://www.demoblaze.com
2. Go directly to the Cart page without adding any products.
3. Click “Place Order”.
4. Fill in the required form fields.
5. Click “Purchase”.
6. Observe that the website allows the order to be completed even though the cart is empty.

### Expected Result
The Place Order button should be disabled or hidden when the cart is empty. The system should not allow the user to complete an order without products.

### Actual Result
The user can complete an order after filling in the required form fields, even when the cart is empty.

### Evidence
Screenshots:
- `screenshots\tc-012-bug-005.png`

### Related Test Cases
- TC-010: Place order modal opens
- TC-011: Complete order with valid data

## BUG-006: Contact form can be submitted with empty fields

**Severity:** Medium  
**Priority:** Medium  
**Type:** Validation / Contact form issue  

### Description
The Contact form allows the user to send a message even when all fields are empty. After clicking “Send message”, the website displays a confirmation message saying “Thanks for the message!!” without validating the required fields.

This can result in empty or invalid contact messages being submitted.

### Steps to Reproduce
1. Open https://www.demoblaze.com
2. Click “Contact”.
3. Leave Contact Email, Contact Name and Message fields empty.
4. Click “Send message”.
5. Observe the confirmation message.

### Expected Result
The website should validate the Contact form fields and prevent submission when required fields are empty. The user should see a clear validation message.

### Actual Result
The website displays “Thanks for the message!!” even when all Contact form fields are empty.

### Evidence
Screenshot:
- `screenshots\tc-021-bug-006.png`

### Related Test Cases
- TC-020: Contact modal opens
- TC-021: Send contact message
- TC-022: Contact form with empty fields