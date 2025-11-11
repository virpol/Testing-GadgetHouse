# Bug Report  DV-001 (Header, Search field, Catalog menu)

**Trello:** `https://trello.com/c/a0dg5ZCE`
**Page:** Header (visible on all pages)  
**Environment:** Desktop (tested at 1440px unless stated otherwise)  
**Test basis:** Figma design - Header and Navigation section  
**Test objective:** Verify visual compliance and functional behavior of header components: logo, navigation icons, search field, and catalog dropdown menu.

---

##  1. Search Field - Hover & States

**Description:**  
The magnifying glass icon in the search bar does not react to hover.  
Additionally, the field is missing proper UI states (hover, active, disabled, error).

**Steps to reproduce:**
1. Open the main page.
2. Hover over the search icon or interact with the input field.

**Expected result:**  
- Icon color changes according to hover state in Figma.  
- Input field displays proper states (hover/active/disabled/error).  

**Actual result:**  
- No hover effect on icon (unchanged on hover).  
- Missing field states.  

**Status:** Verified / Closed 
**Severity:** Minor  
**Attachments:** `[search_field.mp4](https://trello.com/1/cards/65fc3201e2d687252b272e37/attachments/67768f04261fad7db286dbbf/download/search_field.mp4)`

---

##  2. Search Functionality - Input & Confirmation

**Description:**  
The search input does not trigger navigation to the results page when pressing Enter or clicking the search icon.

**Steps:**
1. Type a product name (e.g., “iPhone”) in the search field.
2. Press Enter or click the magnifying glass icon.

**Expected:**  
User is redirected to the Search Results page for the entered query.

**Actual:**  
No navigation occurs; input cannot be confirmed.  
(Tab key also fails to confirm search.)

**Status:** Fixed (to be rechecked)  
**Severity:** Major  
**Attachments:** `[search_field.mp4](https://trello.com/1/cards/65fc3201e2d687252b272e37/attachments/67768f04261fad7db286dbbf/download/search_field.mp4)`

---

##  3. Search Results Behavior

**Description:**  
Incorrect navigation and inconsistency when searching for available and out-of-stock products.

**Steps:**
1. Search for an in-stock product (e.g., *Samsung Galaxy A24 6/128GB Black*).  
2. Search for an out-of-stock product (e.g., *Redmi Note 12*).

**Expected:**  
- In-stock → Product card or search results displayed.  
- Out-of-stock → “Products out of stock” page displayed.

**Actual:**  
- Redirected to “Products not found” page in both cases after pressing Enter or clicking the icon.  
- Temporary correct page appears briefly, then disappears.

**Status:** Verified / Closed
**Severity:** Major  

---

##  4. Overlay Behavior During Search

**Description:**  
When typing in the search field, a dark overlay appears (expected), but it remains after navigating away from the search results.

**Steps:**
1. Type any text into the search field.
2. Wait until results or “no results” message appears.
3. Navigate to another page.

**Expected:**  
The dark overlay disappears once the results are displayed or navigation occurs.

**Actual:**  
The overlay remains active after leaving the search state.  
A visible gap appears between header and overlay at screen width ≤1070px.

**Status:** Verified / Closed 
**Severity:** Medium  
**Attachments:** `https://www.screenpresso.com/cloud/BaNyiofbFdRh/`

---

## 5. Header Alignment (Search field & Banner)

**Description:**  
Search field and icons are not aligned according to Figma.

**Expected alignment:**  
- Left edge of search field = left edge of main banner.  
- Right edge of cart icon = right edge of main banner.

**Actual:**  
Misalignment visible on desktop.  
Right edge of header “cuts off” when text is entered.

**Status:** Verified / Closed 
**Severity:** Medium  

---

##  6. Cart Icon Behavior

**Description:**  
When the basket is empty, the cart icon shows “0”.  

**Expected:**  
No number displayed when basket is empty.

**Actual:**  
“0” appears next to the icon.  

**Status:** Verified / Closed
**Severity:** Trivial  

---

##  7. Catalog Button - Color & Alignment

**Description:**  
The catalog button background color and dropdown width differ from the Figma design.

**Expected:**
- Background color: `#6F4C9A`
- Catalog button and dropdown have the same width.

**Actual:**
- Background color changes to `#593D76` on hover.  
- Dropdown width misaligned with button width.  

**Status:** Verified / Closed 
**Severity:** Minor  

**Notes:** Confirmed with design team that correct hover color is `#6F4C9A`.  

---

##  8. Catalog (Hamburger Menu, <992px)

**Description:**  
At screen width  992px, opening the Hamburger menu shows an empty Catalog dropdown.  
At screen width <992px Selecting a category of Catalog Dropdown menu closes the menu instead of navigating.

**Expected:**  
- Catalog menu opens with category list.  
- Clicking category navigates to correct page.

**Actual:**  
- Empty dropdown at 992px.  
- Menu disappears when category is clicked.

**Status:** Open  
**Severity:** Major  

---

##  9. Miscellaneous UI Inconsistencies

**Description:**
- Long product names cannot be fully entered in search input.  
- User icon (after login) has incorrect hover color (should be white icon on green background).

**Severity:** Minor  
**Status:** Verified / Closed  
