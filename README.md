# FitPeo Automation Assignment - README

## **Project Overview**
This project automates the navigation and interaction with the FitPeo website using Selenium WebDriver, Java, and TestNG in a **Page Object Model (POM)** framework. The goal is to ensure the web elements on the FitPeo homepage and revenue calculator page work as expected by executing the specified test cases.

---

## **Objective**
To automate the following tasks:
1. Navigate to the FitPeo Homepage.
2. Navigate to the Revenue Calculator Page.
3. Scroll down to the slider section and ensure visibility.
4. Adjust the slider to set its value to `820` and validate the update in the associated text field.
5. Enter `560` in the text field and validate the slider's position.
6. Select specific CPT Codes checkboxes.
7. Validate the total recurring reimbursement value.

---

## **Project Structure**
The project follows the **Page Object Model (POM)** design pattern for better code reusability, readability, and maintainability.

### **Key Classes**
1. **Page Classes (in `pages/`)**:
   - `HomePage.java`: Represents the FitPeo homepage.
   - `RevenueCalculatorPage.java`: Represents the revenue calculator page and handles interactions like scrolling, adjusting the slider, and selecting checkboxes.
2. **Base Class (in `base/`)**:
   - `BaseClass.java`: Sets up WebDriver and contains common methods.
3. **Test Classes (in `testcases/`)**:
   - `FitPeoTests.java`: Contains TestNG test methods for the defined tasks.

---

## **Technologies Used**
- **Programming Language**: Java
- **Testing Framework**: TestNG
- **Automation Tool**: Selenium WebDriver
- **Design Pattern**: Page Object Model (POM)
- **Build Tool**: Maven

---

## **Test Cases**
### 1. **Navigate to the FitPeo Homepage**
- **Steps**:
  1. Launch the browser.
  2. Navigate to the FitPeo homepage.
- **Expected Result**: The homepage is displayed successfully.

### 2. **Navigate to the Revenue Calculator Page**
- **Steps**:
  1. Click on the Revenue Calculator link on the homepage.
- **Expected Result**: The Revenue Calculator page is displayed.

### 3. **Scroll Down to the Slider Section**
- **Steps**:
  1. Scroll the page until the slider is visible.
- **Expected Result**: The slider becomes visible.

### 4. **Adjust the Slider**
- **Steps**:
  1. Move the slider to set its value to `823`.
  2. Because of non-accuate value of X-offset we choose to select 823 instead of 820.
- **Expected Result**: The associated text field displays the value `823`.

### 5. **Update the Text Field**
- **Steps**:
  1. Enter `560` in the text field.
- **Expected Result**: The slider's position updates to reflect the value `560`.

### 6. **Select CPT Codes**
- **Steps**:
  1. Scroll down to the CPT codes section.
  2. Select the checkboxes for `CPT-99091`, `CPT-99453`, `CPT-99454`, and `CPT-99474`.
- **Expected Result**: The selected checkboxes are checked.

### 7. **Validate Total Recurring Reimbursement**
- **Steps**:
  1. Verify the header displays `Total Recurring Reimbursement for all Patients Per Month: $110700`.
- **Expected Result**: The value is displayed as expected.

---

## **How to Run the Tests**
### **Pre-requisites**
1. Install Java (version 8 or above) and set up the environment variables.
2. Install Maven.
3. Download and configure the browser driver (e.g., ChromeDriver).

### **Steps to Execute**
1. Clone the repository:
   ```
   git clone https://github.com/PrakashKjsst/FitPeo.git
   ```
2. Navigate to the testNg.xml file:
   ```
   Right click and run as testNG suite
   ```

## **Dependencies**
The required dependencies are listed in the `pom.xml` file. Key dependencies include:
- Selenium Java
- TestNG
- WebDriverManager (optional, for automated driver management)
---

## **Future Enhancements**
1. Implement logging using Log4j for better debugging.
2. Add cross-browser testing support.
---

## **Contact**
For any queries, feel free to contact:
- **Name**: [Your Name]
- **Email**: [Your Email]
- **GitHub**: [Your GitHub Profile]
