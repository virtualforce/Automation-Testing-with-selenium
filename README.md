# Automation Testing with selenium

# 1. What is Selenium
	Selenium automates browser. Selenium is a set of tools and library that automate browser actions. Selenium provides tools   that can interact with browser and can automate browser actions like click, input, select etc with the help of script. Selenium is not a tool but library of tools

# 2. Features of Selenium
   Flexible & Extensible
   Mutiple Language support
   Mutiple browser support

# 3. Components of Selenium
  ## Selenium IDE 
    Record & playback plugin used for prototype testing
  ## Selenium RC(remote Control) or Selenium 1 
   Used to execute scripts using javascript
   Deprecated
  ## WebDriver
    API used to send commands directly to the browser
   	Is a successer to selenium RC
  ## Selenium Grid
    A tool to run tests in parallel across different machines and different browser simutaneously
    Used to minimize execution time

# Selenium Versions
## Selenium 1 (Selenium RC)
## Selenium 2 (Selenium RC + WebDriver)
## Selenium 3 (WebDriver)

# selenium-webdriver gem
  WebDriver is a web automation framework that allows you to execute your tests against different browsers, not just Firefox, Chrome
Example of using Selenium with Ruby
    `await this.driver
      .findElement(By.xpath("//*[contains(text(),'This field is required')]"))
      .isDisplayed();

    let emailErr = await this.driver
      .findElement(By.css("[data-val='emailError']"))
      .getText();

    let passwordErr = await this.driver
      .findElement(By.css("[data-val='passwordError']"))
      .getText();

    await assert.equal(emailErr, 'This field is required', 'Validation Error');
    await assert.equal(
      passwordErr,
      'This field is required',
      'Validation Error',
    );`
 # ChaiJS
  Chai is a BDD / TDD assertion library for node and the browser that can be delightfully paired with any javascript testing framework
Example 
  await assert.equal(emailErr, 'This field is required', 'Validation Error');
# Jasmine
Jasmine is a behavior-driven development framework for testing JavaScript code. It does not depend on any other JavaScript frameworks. It does not require a DOM. And it has a clean, obvious syntax so that you can easily write tests.
Example

    ` describe('it should cover Admin Authentication  Testcases', () => {
    it('use case - it should cover signin validation scenarios with admin login details', async () => {
      await homePage.visit();
      await loginPage.visit();
      await loginPage.submitAdminFormWithValidation();
      await dashboard.signout();
    });
    });
   `
