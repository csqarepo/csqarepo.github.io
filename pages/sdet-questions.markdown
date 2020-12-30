---
layout: page
title:  "SDET Interview Questions"
date:   2020-12-28 15:30:08 +0530

---
Please find below all the SDET Interview Questions. 

**1. How to perform back,forward and refresh action in selenium?**
driver.navigate().back()
driver.navigate().forward()
driver.navigate().refresh()

**2. What is the return type of findelements?**

List of elements with similar property

**3. What will happen if no webelement is found for findelements?**

It will return an empty list

**4. What will happen if no webelement is found for findelement?**

It will give error as :NoSuchElementException

**5. How to select value from dropdown in selenium?**

Using select class as below
Select technology = new Select(driver.findElement(By.xpath("//select[@id='effectTypes']")));
technology.selectByVisibleText("Drop");

**6. What are the methods provided in selenium to select from dropdown?**

    selectByVisibleText()
    selectByValue()
    selectByIndex()
   
**7. How to fetch text from UI in selenium?**

gettext()
getAttribute("propertyname")

**8. How to get current url,title and page source?**

driver.getCurrentUrl();
driver.getTitle();
driver.getPageSource();

**9. How to clear text using selenium?**

clear() — method is used to clear text from the text area
driver.findElement(By.xpath(“//input[@placeholder=’Username’]”)).clear();

**10. How to do Browser Initialization for all types of browser?**

• Firefox

	WebDriver driver = new FirefoxDriver();

• Chrome

	WebDriver driver = new ChromeDriver();

•    Internet Explorer

	WebDriver driver = new InternetExplorerDriver();

•    Safari Driver

	WebDriver driver = new SafariDriver();


**11. How to handle alerts and popups in selenium?**

	driver.switchTO().alert.accept()

to accept the alert box

	driver.switchTO().alert.dismiss()
	
to cancel the alert box

**12. How to retrive alert pop up message in selenium?**

	driver.switchTO().alert.getText() — to retrieve the alert message

**13. How to send data to alert box in Selenium?**

	driver.switchTO().alert.sendKeys(“Text”) — to send data to the alert box

**14. How to switch frames in selenium?**

	driver.switchTo.frame(int frameNumber) — mentioning the frame index number, the Driver will switch to that specific frame
	driver.switchTo.frame(string frameNameOrID) — mentioning the frame element or ID, the Driver will switch to that specific frame
	driver.switchTo.frame(WebElement frameElement) — mentioning the frame web element, the Driver will switch to that specific frame

**15. How to switch back to main window in frames?**

	driver.switchTo().defaultContent() — Switching back to the main window

**16. How to handle multiple windows and tabs in Selenium?**

	getWindowHandle() — used to retrieve the handle of the current page (a unique identifier)
	getWindowHandles() — used to retrieve a set of handles of the all the pages available

**17. How to switch between windows and tabs?**

	driver.switchTo().window(“windowName/handle”) — switch to a window

**18. How to close the cureent browser window?**

	driver.close() — closes the current browser window

**19. How to handle Implicit wait?**

Used to wait for a certain amount of time before throwing an exception
	
	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

**20. How to handle Explicit wait?**

Used to wait until a certain condition occurs before executing the code.
	
	WebDriverWait wait = new WebDriverWait(driver,30);
	wait.until(ExpectedConditions.presenceOfElementLocated(By.name("login")));