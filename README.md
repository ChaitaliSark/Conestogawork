<html>
<head>
<title> Assignment 4 </title>
<style> body {
background-image:url(sirpi-floral-leaf-pattern-wallpaper-metallic-glitter-heavy-weight-20590-p3723-9033_medium.jpg)
}
</style>
<script src='vali.js'></script>
</head>
<h1 style="font-family: Times New Roman;"><b>Enter Information: </b></h1>
<br> 
<header>
<form name="myForm" action="insert.php" method="post" onsubmit="return xyz()" >
<table>

<tr><td>Seller Name:</td>
<td><input type="text" placeholder="Seller Name" name="SellerName" id= "SellerName"/> </td> </tr>

<tr><td>Address:</td>
<td><input type="text" placeholder="Address" name="Addr" id= "Addr"/> </td></tr>

<tr><td>City:</td>
<td><input type="text" placeholder="City" name="City" id= "City"/> </td></tr>

<tr><td>Phone Number:</td>
<td><input type="tel" pattern="^[(]{0,1}[0-9]{3,3}[)/-]{0,1}[0-9]{3,3}[-]{1,1}[0-9]{4,4}$" placeholder="123-456-7891" name="Phone" id= "Phone"/> </td></tr>

<tr><td>Email Address:</td>
<td><input type="email" pattern="[a-zA-Z0-9.-_]{1,}@[a-zA-Z.-]{2,}[.]{1}[a-zA-Z]{2,}" placeholder="Email Address" name="Email" id= "Email"/> </td></tr>

<tr><td>Vehicle Make:</td>
<td><input type="text" placeholder="Vehical Make" name="Make" id= "Make"/> </td></tr>

<tr><td>Vehicle Model:</td>
<td><input type="text" placeholder="Vehical Model" name="Model" id= "Model"/> </td></tr>

<tr><td>Vehicle Year:</td>
<td><input type="text" placeholder="Vehical Year" name="Year" id= "Year"/> </td></tr>

<tr><td> </td>
<td> <input type="Submit" value="Submit"> <a href="Page1.html"><button> Home</button> </a> </td></tr>

</table>
</form>
</header>
</html>


<html>
<head>

<title> <h1> Assignement 4 </h></title>
<style> body {

background-image:url(858748.jpg)

}</body> 
</style>
</head>
<body>

<br> </br>	

<table>
<tr> <td> <h1><a href="i.html"><button> New </button></a></h1> </tr>
<td> <a href="database.php"> <button>Search </button> </a> </td> </tr>

</table>

</body>
</html>

using System;
using System.Text;
using System.Text.RegularExpressions;
using System.Threading;
using NUnit.Framework;
using OpenQA.Selenium;
using OpenQA.Selenium.Firefox;
using OpenQA.Selenium.Support.UI;

namespace SeleniumTests
{
    [TestFixture]
    public class SeleniumTestInputObsoleteCarDetailsReturnError
    {
        private IWebDriver driver;
        private StringBuilder verificationErrors;
        private string baseURL;
        private bool acceptNextAlert = true;

        [SetUp]
        public void SetupTest()
        {
            driver = new FirefoxDriver();
            baseURL = "https://www.katalon.com/";
            verificationErrors = new StringBuilder();
        }

        [TearDown]
        public void TeardownTest()
        {
            try
            {
                driver.Quit();
            }
            catch (Exception)
            {
                // Ignore errors if unable to close the browser
            }
            Assert.AreEqual("", verificationErrors.ToString());
        }

        [Test]
        public void TheSeleniumTestInputObsoleteCarDetailsReturnErrorTest()
        {
            driver.Navigate().GoToUrl("http://localhost/");
            driver.FindElement(By.LinkText("Chaitali/")).Click();
            driver.FindElement(By.LinkText("Chaitali/")).Click();
            driver.FindElement(By.LinkText("Page1.html")).Click();
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Search'])[1]/preceding::button[1]")).Click();
            driver.FindElement(By.Id("SellerName")).Click();
            driver.FindElement(By.Id("SellerName")).Clear();
            driver.FindElement(By.Id("SellerName")).SendKeys("anim");
            driver.FindElement(By.Id("SellerName")).SendKeys(Keys.Down);
            driver.FindElement(By.Id("SellerName")).Clear();
            driver.FindElement(By.Id("SellerName")).SendKeys("Anima");
            driver.FindElement(By.Id("Addr")).Click();
            driver.FindElement(By.Id("Addr")).Clear();
            driver.FindElement(By.Id("Addr")).SendKeys("ba");
            driver.FindElement(By.Id("Addr")).SendKeys(Keys.Down);
            driver.FindElement(By.Id("Addr")).Clear();
            driver.FindElement(By.Id("Addr")).SendKeys("Bajaj Nagar");
            driver.FindElement(By.Id("City")).Click();
            driver.FindElement(By.Id("City")).Clear();
            driver.FindElement(By.Id("City")).SendKeys("Nagpur");
            driver.FindElement(By.Id("Phone")).Click();
            driver.FindElement(By.Id("Phone")).Clear();
            driver.FindElement(By.Id("Phone")).SendKeys("7777");
            driver.FindElement(By.Id("Phone")).SendKeys(Keys.Down);
            driver.FindElement(By.Id("Phone")).Clear();
            driver.FindElement(By.Id("Phone")).SendKeys("777-777-7777");
            driver.FindElement(By.Id("Email")).Click();
            driver.FindElement(By.Id("Email")).Clear();
            driver.FindElement(By.Id("Email")).SendKeys("anima@gmail.com");
            driver.FindElement(By.Id("Make")).Click();
            driver.FindElement(By.Id("Make")).Clear();
            driver.FindElement(By.Id("Make")).SendKeys("maruti");
            driver.FindElement(By.Id("Model")).Click();
            driver.FindElement(By.Id("Model")).Clear();
            driver.FindElement(By.Id("Model")).SendKeys("altok20");
            driver.FindElement(By.Id("Year")).Click();
            driver.FindElement(By.Id("Year")).Clear();
            driver.FindElement(By.Id("Year")).SendKeys("2013");
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Vehicle Year:'])[1]/following::input[2]")).Click();
            driver.FindElement(By.Id("url")).Click();
        }
        private bool IsElementPresent(By by)
        {
            try
            {
                driver.FindElement(by);
                return true;
            }
            catch (NoSuchElementException)
            {
                return false;
            }
        }

        private bool IsAlertPresent()
        {
            try
            {
                driver.SwitchTo().Alert();
                return true;
            }
            catch (NoAlertPresentException)
            {
                return false;
            }
        }

        private string CloseAlertAndGetItsText()
        {
            try
            {
                IAlert alert = driver.SwitchTo().Alert();
                string alertText = alert.Text;
                if (acceptNextAlert)
                {
                    alert.Accept();
                }
                else
                {
                    alert.Dismiss();
                }
                return alertText;
            }
            finally
            {
                acceptNextAlert = true;
            }
        }

        public class SeleniumTestCheckSearchButtonReturnDetails
        {
            private IWebDriver driver;
            private StringBuilder verificationErrors;
            private string baseURL;
            private bool acceptNextAlert = true;

            [SetUp]
            public void SetupTest()
            {
                driver = new FirefoxDriver();
                baseURL = "https://www.katalon.com/";
                verificationErrors = new StringBuilder();
            }

            [TearDown]
            public void TeardownTest()
            {
                try
                {
                    driver.Quit();
                }
                catch (Exception)
                {
                    // Ignore errors if unable to close the browser
                }
                Assert.AreEqual("", verificationErrors.ToString());
            }

            [Test]
            public void TheSeleniumTestCheckSearchButtonReturnDetailsTest()
            {
                driver.Navigate().GoToUrl("http://localhost/");
                driver.FindElement(By.LinkText("Chaitali/")).Click();
                driver.FindElement(By.LinkText("Chaitali/")).Click();
                driver.FindElement(By.LinkText("Page1.html")).Click();
                driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='New'])[1]/following::button[1]")).Click();
                driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='https://jdpower.com/Cars/2016/mazda/c4'])[1]/following::button[1]")).Click();
                Assert.AreEqual("", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='New'])[1]/following::button[1]")).Text);
            }
            private bool IsElementPresent(By by)
            {
                try
                {
                    driver.FindElement(by);
                    return true;
                }
                catch (NoSuchElementException)
                {
                    return false;
                }
            }

            private bool IsAlertPresent()
            {
                try
                {
                    driver.SwitchTo().Alert();
                    return true;
                }
                catch (NoAlertPresentException)
                {
                    return false;
                }
            }

            private string CloseAlertAndGetItsText()
            {
                try
                {
                    IAlert alert = driver.SwitchTo().Alert();
                    string alertText = alert.Text;
                    if (acceptNextAlert)
                    {
                        alert.Accept();
                    }
                    else
                    {
                        alert.Dismiss();
                    }
                    return alertText;
                }
                finally
                {
                    acceptNextAlert = true;
                }
            }

            [TestFixture]
            public class SeleniumTestInputInvalidEmailAddressReturnError
            {
                private IWebDriver driver;
                private StringBuilder verificationErrors;
                private string baseURL;
                private bool acceptNextAlert = true;

                [SetUp]
                public void SetupTest()
                {
                    driver = new FirefoxDriver();
                    baseURL = "https://www.katalon.com/";
                    verificationErrors = new StringBuilder();
                }

                [TearDown]
                public void TeardownTest()
                {
                    try
                    {
                        driver.Quit();
                    }
                    catch (Exception)
                    {
                        // Ignore errors if unable to close the browser
                    }
                    Assert.AreEqual("", verificationErrors.ToString());
                }

                [Test]
                public void TheSeleniumTestInputInvalidEmailAddressReturnErrorTest()
                {
                    driver.Navigate().GoToUrl("http://localhost/");
                    driver.FindElement(By.LinkText("Chaitali/")).Click();
                    driver.FindElement(By.LinkText("Chaitali/")).Click();
                    driver.FindElement(By.LinkText("Page1.html")).Click();
                    driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Search'])[1]/preceding::button[1]")).Click();
                    driver.FindElement(By.Id("SellerName")).Click();
                    driver.FindElement(By.Id("SellerName")).Clear();
                    driver.FindElement(By.Id("SellerName")).SendKeys("urmi");
                    driver.FindElement(By.Id("Addr")).Click();
                    driver.FindElement(By.Id("Addr")).Clear();
                    driver.FindElement(By.Id("Addr")).SendKeys("weber street");
                    driver.FindElement(By.Id("City")).Click();
                    driver.FindElement(By.Id("City")).Clear();
                    driver.FindElement(By.Id("City")).SendKeys("hamilton");
                    driver.FindElement(By.Id("Phone")).Click();
                    driver.FindElement(By.Id("Phone")).Clear();
                    driver.FindElement(By.Id("Phone")).SendKeys("789-987-8888");
                    driver.FindElement(By.Id("Email")).Click();
                    driver.FindElement(By.Id("Email")).Clear();
                    driver.FindElement(By.Id("Email")).SendKeys("urmiatgmail.com");
                    driver.FindElement(By.Id("Make")).Click();
                    driver.FindElement(By.Id("Make")).Clear();
                    driver.FindElement(By.Id("Make")).SendKeys("suzuki");
                    driver.FindElement(By.Id("Model")).Click();
                    driver.FindElement(By.Id("Model")).Clear();
                    driver.FindElement(By.Id("Model")).SendKeys("swift");
                    driver.FindElement(By.Id("Year")).Click();
                    driver.FindElement(By.Id("Year")).Clear();
                    driver.FindElement(By.Id("Year")).SendKeys("2013");
                    driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Vehicle Year:'])[1]/following::input[2]")).Click();
                    driver.FindElement(By.Id("Email")).Click();
                    driver.FindElement(By.Id("Email")).Clear();
                    driver.FindElement(By.Id("Email")).SendKeys("urmi@gmail.com");
                    driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Vehicle Year:'])[1]/following::input[2]")).Click();
                    driver.FindElement(By.Id("url")).Click();
                    // ERROR: Caught exception [unknown command []]
                    Assert.AreEqual("", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Close navigation'])[1]/following::ul[1]")).Text);
                }
                private bool IsElementPresent(By by)
                {
                    try
                    {
                        driver.FindElement(by);
                        return true;
                    }
                    catch (NoSuchElementException)
                    {
                        return false;
                    }
                }

                private bool IsAlertPresent()
                {
                    try
                    {
                        driver.SwitchTo().Alert();
                        return true;
                    }
                    catch (NoAlertPresentException)
                    {
                        return false;
                    }
                }

                private string CloseAlertAndGetItsText()
                {
                    try
                    {
                        IAlert alert = driver.SwitchTo().Alert();
                        string alertText = alert.Text;
                        if (acceptNextAlert)
                        {
                            alert.Accept();
                        }
                        else
                        {
                            alert.Dismiss();
                        }
                        return alertText;
                    }
                    finally
                    {
                        acceptNextAlert = true;
                    }
                }
            }
        }

        [TestFixture]
        public class SeleniumTestInputObsoleteCarDetailsReturnError
        {
            private IWebDriver driver;
            private StringBuilder verificationErrors;
            private string baseURL;
            private bool acceptNextAlert = true;

            [SetUp]
            public void SetupTest()
            {
                driver = new FirefoxDriver();
                baseURL = "https://www.katalon.com/";
                verificationErrors = new StringBuilder();
            }

            [TearDown]
            public void TeardownTest()
            {
                try
                {
                    driver.Quit();
                }
                catch (Exception)
                {
                    // Ignore errors if unable to close the browser
                }
                Assert.AreEqual("", verificationErrors.ToString());
            }

            [Test]
            public void TheSeleniumTestInputObsoleteCarDetailsReturnErrorTest()
            {
                driver.Navigate().GoToUrl("http://localhost/");
                driver.FindElement(By.LinkText("Chaitali/")).Click();
                driver.FindElement(By.LinkText("Chaitali/")).Click();
                driver.FindElement(By.LinkText("Page1.html")).Click();
                driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Search'])[1]/preceding::button[1]")).Click();
                driver.FindElement(By.Id("SellerName")).Click();
                driver.FindElement(By.Id("SellerName")).Clear();
                driver.FindElement(By.Id("SellerName")).SendKeys("anim");
                driver.FindElement(By.Id("SellerName")).SendKeys(Keys.Down);
                driver.FindElement(By.Id("SellerName")).Clear();
                driver.FindElement(By.Id("SellerName")).SendKeys("Anima");
                driver.FindElement(By.Id("Addr")).Click();
                driver.FindElement(By.Id("Addr")).Clear();
                driver.FindElement(By.Id("Addr")).SendKeys("ba");
                driver.FindElement(By.Id("Addr")).SendKeys(Keys.Down);
                driver.FindElement(By.Id("Addr")).Clear();
                driver.FindElement(By.Id("Addr")).SendKeys("Bajaj Nagar");
                driver.FindElement(By.Id("City")).Click();
                driver.FindElement(By.Id("City")).Clear();
                driver.FindElement(By.Id("City")).SendKeys("Nagpur");
                driver.FindElement(By.Id("Phone")).Click();
                driver.FindElement(By.Id("Phone")).Clear();
                driver.FindElement(By.Id("Phone")).SendKeys("7777");
                driver.FindElement(By.Id("Phone")).SendKeys(Keys.Down);
                driver.FindElement(By.Id("Phone")).Clear();
                driver.FindElement(By.Id("Phone")).SendKeys("777-777-7777");
                driver.FindElement(By.Id("Email")).Click();
                driver.FindElement(By.Id("Email")).Clear();
                driver.FindElement(By.Id("Email")).SendKeys("anima@gmail.com");
                driver.FindElement(By.Id("Make")).Click();
                driver.FindElement(By.Id("Make")).Clear();
                driver.FindElement(By.Id("Make")).SendKeys("maruti");
                driver.FindElement(By.Id("Model")).Click();
                driver.FindElement(By.Id("Model")).Clear();
                driver.FindElement(By.Id("Model")).SendKeys("altok20");
                driver.FindElement(By.Id("Year")).Click();
                driver.FindElement(By.Id("Year")).Clear();
                driver.FindElement(By.Id("Year")).SendKeys("2013");
                driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Vehicle Year:'])[1]/following::input[2]")).Click();
                driver.FindElement(By.Id("url")).Click();
            }
            private bool IsElementPresent(By by)
            {
                try
                {
                    driver.FindElement(by);
                    return true;
                }
                catch (NoSuchElementException)
                {
                    return false;
                }
            }

            private bool IsAlertPresent()
            {
                try
                {
                    driver.SwitchTo().Alert();
                    return true;
                }
                catch (NoAlertPresentException)
                {
                    return false;
                }
            }

            private string CloseAlertAndGetItsText()
            {
                try
                {
                    IAlert alert = driver.SwitchTo().Alert();
                    string alertText = alert.Text;
                    if (acceptNextAlert)
                    {
                        alert.Accept();
                    }
                    else
                    {
                        alert.Dismiss();
                    }
                    return alertText;
                }
                finally
                {
                    acceptNextAlert = true;
                }
            }
            [TestFixture]
            public class SeleniumTestInputDetailsInformationIsSaved
            {
                private IWebDriver driver;
                private StringBuilder verificationErrors;
                private string baseURL;
                private bool acceptNextAlert = true;

                [SetUp]
                public void SetupTest()
                {
                    driver = new FirefoxDriver();
                    baseURL = "https://www.katalon.com/";
                    verificationErrors = new StringBuilder();
                }

                [TearDown]
                public void TeardownTest()
                {
                    try
                    {
                        driver.Quit();
                    }
                    catch (Exception)
                    {
                        // Ignore errors if unable to close the browser
                    }
                    Assert.AreEqual("", verificationErrors.ToString());
                }

                [Test]
                public void TheSeleniumTestInputDetailsInformationIsSavedTest()
                {
                    driver.Navigate().GoToUrl("http://localhost/");
                    driver.FindElement(By.LinkText("Chaitali/")).Click();
                    driver.FindElement(By.LinkText("Chaitali/")).Click();
                    driver.FindElement(By.LinkText("Page1.html")).Click();
                    driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Search'])[1]/preceding::button[1]")).Click();
                    driver.FindElement(By.Id("SellerName")).Click();
                    driver.FindElement(By.Id("SellerName")).Clear();
                    driver.FindElement(By.Id("SellerName")).SendKeys("Ashish");
                    driver.FindElement(By.Id("Addr")).Click();
                    driver.FindElement(By.Id("Addr")).Clear();
                    driver.FindElement(By.Id("Addr")).SendKeys("weber street");
                    driver.FindElement(By.Id("City")).Click();
                    driver.FindElement(By.Id("City")).Clear();
                    driver.FindElement(By.Id("City")).SendKeys("guelph");
                    driver.FindElement(By.Id("Phone")).Click();
                    driver.FindElement(By.Id("Phone")).Clear();
                    driver.FindElement(By.Id("Phone")).SendKeys("555-666-9999");
                    driver.FindElement(By.Id("Email")).Click();
                    driver.FindElement(By.Id("Email")).Clear();
                    driver.FindElement(By.Id("Email")).SendKeys("ashish@hotmail.com");
                    driver.FindElement(By.Id("Make")).Click();
                    driver.FindElement(By.Id("Make")).Clear();
                    driver.FindElement(By.Id("Make")).SendKeys("Honda");
                    driver.FindElement(By.Id("Model")).Click();
                    driver.FindElement(By.Id("Model")).Clear();
                    driver.FindElement(By.Id("Model")).SendKeys("City");
                    driver.FindElement(By.Id("Year")).Click();
                    driver.FindElement(By.Id("Year")).Clear();
                    driver.FindElement(By.Id("Year")).SendKeys("2013");
                    driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Vehicle Year:'])[1]/following::input[2]")).Click();
                    driver.FindElement(By.Id("url")).Click();
                    // ERROR: Caught exception [Error: locator strategy either id or name must be specified explicitly.]
                }
                private bool IsElementPresent(By by)
                {
                    try
                    {
                        driver.FindElement(by);
                        return true;
                    }
                    catch (NoSuchElementException)
                    {
                        return false;
                    }
                }

                private bool IsAlertPresent()
                {
                    try
                    {
                        driver.SwitchTo().Alert();
                        return true;
                    }
                    catch (NoAlertPresentException)
                    {
                        return false;
                    }
                }

                private string CloseAlertAndGetItsText()
                {
                    try
                    {
                        IAlert alert = driver.SwitchTo().Alert();
                        string alertText = alert.Text;
                        if (acceptNextAlert)
                        {
                            alert.Accept();
                        }
                        else
                        {
                            alert.Dismiss();
                        }
                        return alertText;
                    }
                    finally
                    {
                        acceptNextAlert = true;
                    }
                }
            }
        }
        }
    }
}

