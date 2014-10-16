[![star](http://github-svg-buttons.herokuapp.com/star.svg?user=ddavison&repo=getting-started-with-selenium-framework)](http://github.com/ddavison/getting-started-with-selenium-framework)
[![fork](http://github-svg-buttons.herokuapp.com/fork.svg?user=ddavison&repo=getting-started-with-selenium-framework)](http://github.com/ddavison/getting-started-with-selenium-framework/fork)

# Getting Started
Using maven, include it as a dependency:
```xml
<dependency>
  <groupId>io.ddavison</groupId>
  <artifactId>getting-started-with-selenium-framework</artifactId>
  <version>[1,)</version>
</dependency>
```

Create a Java Class, and extend it from `AutomationTest`

### Drivers
Drivers should be put in the root of your project, and be named like this:

#### Mac
chromedriver.mac

#### Windows
chromedriver.exe

#### Linux
chromedriver.linux

So as an example, your project structure could be:
```
Project
| src
|   main
|     java
|       TestClass.java
| pom.xml
| chromedriver.mac
| chromedriver.exe
| chromedriver.linux
```



# Goals
The primary goals of this project are to...
- Take advantage of method chaining, to create a fluent interface.
- Abstract the programmer from bloated scripts resulting from using too many css selectors, and too much code.
- Provide a quick and easy framework in Selenium 2 using Java, to get started writing scripts.
- Provide a free to use framework for any starting enterprise, or individual programmer.
- Utilize the power of CSS!

# Actions
You can perform any action that you could possibly do, using the inline actions.
- ```click(By)```
- ```setText(By, text)```
- ```getText(By)```
- ```hoverOver(By)```
- ```check(By)```
- ```uncheck(By)```
- ```navigateTo(url)```
- ```goBack()```
- ```isPresent(By)```
- ```getAttribute(By, attribute)```
- etc.

# In-line validations
This is one of the most important features that I want to _*accentuate*_.
- ```validateText```
- ```validateTextNot```
- ```validateChecked```
- ```validateUnchecked```
- ```validatePresent```
- ```validateNotPresent```
- ```validateTextPresent```
- ```validateTextNotPresent```

All of these methods are able to be called in-line, and fluently without ever having to break your tests.

# Switching Windows
Another nice feature that is offered, is the simplicity of window switching in Selenium.

- ```switchToWindow(regex)```
- ```waitForWindow(regex)```
- ```closeWindow(regex)```

All of these functions take a regular expression argument, and match either the url or title of the window that you want to interact with.

# Switching Frames
- ```switchToFrame(idOrName)```
- ```switchToDefaultContent()```

# Implicit Waiting
In addition to the Selenium 2 implicit waiting, the ```AutomationTest``` class extends on this concept by implenting a sort of ```waitFor``` functionality which ensures that an object appears before interacting with it.  This rids of most ```ElementNotFound``` exceptions that Selenium will cough up.


[See a working example](https://github.com/ddavison/getting-started-with-selenium/blob/master/src/tests/java/com/company/seleniumframework/functional/SampleFunctionalTest.java) of what a test script written using this framework might look like.

# Pull requests
If you have an idea for the framework, fork it and submit a pull-request!
