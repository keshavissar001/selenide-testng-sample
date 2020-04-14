# Run Your Selenide Scripts on LambdaTest Selenium Grid

[Selenide](http://selenide.org/) Integration with [LambdaTest](https://www.lambdatest.com/).

<a href="https://www.automation.lambdatest.com">![LambdaTest Logo](https://www.lambdatest.com/static/images/logo.svg)</a>

<a href="http://selenide.org/"><img src ="http://selenide.org/images/selenide-logo-big.png" height = "110"></a>

## LambdaTest with Selenide Automation Framework : 

Selenide automation framework acts as a wrapper of Selenium WebDriver to help you write crisp and concise UI tests in Java. Selenide automatically takes care of browser shutdown, handling timeouts, test debugging, and StaleElement Exception, so you only focus on improving your business logic.

LambdaTest integration with Selenide automation framework will help you pace your test automation effort even further. Using our on-cloud Selenium Grid you will be able to run your automation script on more than 2000 real browsers & browser versions running across numerous devices & operating systems.

## Prerequisites for running tests using Selenide automation framework :

## Environment Setup 

1. Global Dependencies

   Make sure you have the latest Java installed in your system.
   
   For Windows :
   
   You can download Java for Windows from [here](http://www.java.com/en/download/manual.jsp)
   
   Run the installer and follow the setup wizard to install Java.
   
   and create a new JAVA_HOME environment variable and set variable value as path value to JDK folder.
   
   #### This is Windows environment variable location :
   Control Panel > All Control Panel Items > System > Advanced system settings > Environment Variables
   
   For Linux :
   
   use this command :
   ```
   sudo apt-get install openjdk-8-jre
   ```
   For Mac
   Java should already be present on Mac OS X by default
   
   Install Maven from [here](https://maven.apache.org/install.html)
   
2 Setup

•	You can download the file. To do this click on “Clone or download” button. You can download zip file.

   Go to “selenide-testng-sample-master” folder and copy its path.
   Open command prompt and run :
   
    cd <path> (that you have copied)
    
    (please ignore "<" , ">" symbols)

•	To clone the file, click on “Clone or download” button and copy the link.

•	Then open the command prompt in the folder you want to clone the file. Run the command:

      git clone <paste link here> 
      
* Install maven dependencies through this command :

    mvn compile
    
* Update `*.conf.json` files inside the `src/test/resources/conf` directory with your [LambdaTest Username and Access Key](https://accounts.lambdatest.com/profile)

   
3. Lambdatest Credentials
    * Set LambdaTest username and access key in environment variables.
    It can be obtained from [LambdaTest dashboard](https://automation.lambdatest.com/)    
    example:
    - For linux/mac
    ```
    export LT_USERNAME=<YOUR_USERNAME>
    export LT_ACCESS_KEY=<YOUR ACCESS KEY>
    
    ```
    - For Windows
    ```
    set LT_USERNAME=<YOUR_USERNAME>
    set LT_ACCESS_KEY=<YOUR ACCESS KEY>
    
    ```

4. Running your tests

Use these commands

- To run a single test :

   mvn test -P single

- To run a full suite of tests :

   mvn test -P suite
   
- To run parallel tests :

   mvn test -P parallel

 Want to calculate that how many parallel sessions you need by using our [Parallel Test Calculator](https://www.lambdatest.com/concurrency-calculator?ref=github)

#####  Routing traffic through your local machine
- Set tunnel value to `true` in test capabilities
> OS specific instructions to download and setup tunnel binary can be found at the following links.
>    - [Windows](https://www.lambdatest.com/support/docs/display/TD/Local+Testing+For+Windows)
>    - [Mac](https://www.lambdatest.com/support/docs/display/TD/Local+Testing+For+MacOS)
>    - [Linux](https://www.lambdatest.com/support/docs/display/TD/Local+Testing+For+Linux)

### Important Note:
Some Safari & IE browsers, doesn't support automatic resolution of the URL string "localhost". Therefore if you test on URLs like "http://localhost/" or "http://localhost:8080" etc, you would get an error in these browsers. A possible solution is to use "localhost.lambdatest.com" or replace the string "localhost" with machine IP address. For example if you wanted to test "http://localhost/dashboard" or, and your machine IP is 192.168.2.6 you can instead test on "http://192.168.2.6/dashboard" or "http://localhost.lambdatest.com/dashboard".

## About LambdaTest
[LambdaTest](https://www.lambdatest.com/) is a cloud based selenium grid infrastructure that can help you run automated cross browser compatibility tests on 2000+ different browser and operating system environments. LambdaTest supports all programming languages and frameworks that are supported with Selenium, and have easy integrations with all popular CI/CD platforms. It's a perfect solution to bring your [selenium automation testing](https://www.lambdatest.com/selenium-automation) to cloud based infrastructure that not only helps you increase your test coverage over multiple desktop and mobile browsers, but also allows you to cut down your test execution time by running tests on parallel.

### Resources

##### [SeleniumHQ Documentation](http://www.seleniumhq.org/docs/)
##### [Selenide Documentation](https://selenide.org/documentation.html)
