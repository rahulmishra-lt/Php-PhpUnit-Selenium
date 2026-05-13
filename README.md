# Run Selenium Tests With PHPUnit — TestMu AI (Formerly LambdaTest)

![image](https://user-images.githubusercontent.com/70570645/171654186-aaea4617-43c6-443a-97f2-f6dc45082cd8.png)

<p align="center">
  <a href="https://www.testmuai.com/blog/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium" target="_bank">Blog</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/support/docs/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium" target="_bank">Docs</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/learning-hub/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium" target="_bank">Learning Hub</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/newsletter/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium" target="_bank">Newsletter</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/certifications/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium" target="_bank">Certifications</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.youtube.com/@TestMuAI" target="_bank">YouTube</a>
</p>
&emsp;
&emsp;
&emsp;

_Learn how to use PHPUnit framework to configure and run your PHP automation testing scripts on the TestMu AI platform_

[<img height="58" width="200" src="https://user-images.githubusercontent.com/70570645/171866795-52c11b49-0728-4229-b073-4b704209ddde.png">](https://accounts.lambdatest.com/register?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium)

## Table Of Contents

- [Pre-requisites](#pre-requisites)
- [Run Your First Test](#run-your-first-test)
- [Parallel Testing With PHPUnit](running-parallel-tests-using-php-unit-framework)
- [Local Testing With PHPUnit](#testing-locally-hosted-or-privately-hosted-projects)

## Prerequisites

Before you begin automation testing with Selenium and PHPUnit, you would need to:

- Make sure that you have the latest **PHP** installed on your system. You can download and install **PHP** using following commands in the terminal:

- **MacOS:** Previous versions of **MacOS** have **PHP** installed by default. But for the latest **MacOS** versions starting with **Monterey**, **PHP** has to be downloaded and installed manually by using below commands:

  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  brew install php
  ```

- **Ubuntu:**

  ```bash
  sudo apt-get install curl libcurl3 libcurl3-dev php8.3 php8.3-zip
  ```

**Note:** For **Windows**, you can download **PHP** from [here](http://windows.php.net/download/). Also, refer to this [documentation](http://php.net/manual/en/install.windows.php) for ensuring the accessibility of PHP through Command Prompt(cmd).

- Download **composer** in the project directory ([Linux/MacOS](https://getcomposer.org/download/), [Windows](https://getcomposer.org/doc/00-intro.md#installation-windows)).

- Make sure that you have latest **Composer** installed in in your system.

**Note:** To use the **composer** command directly, it either should have been downloaded in the project directory or should be accessible globally which can be done by the command below:

```bash
mv composer.phar /usr/local/bin/composer
```

### Installing Selenium Dependencies And Tutorial Repo

**Step 1:** Clone the TestMu AI’s Php-PhpUnit-Selenium repository and navigate to the code directory as shown below:

```bash
git clone https://github.com/LambdaTest/Php-PhpUnit-Selenium
cd Php-PhpUnit-Selenium
```

**Step 2:** Install the composer dependencies in the current project directory using the command below:

```bash
composer install
```

### Setting Up Your Authentication

Make sure you have your TestMu AI credentials with you to run test automation scripts. You can get these credentials from the [TestMu AI Automation Dashboard](https://automation.lambdatest.com/build?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium) or by your [TestMu AI Profile](https://accounts.lambdatest.com/login?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium).

**Step 3:** Set TestMu AI `Username` and `Access Key` in environment variables.

- For **Linux/macOS**:

```bash
export LT_USERNAME="YOUR_USERNAME" export LT_ACCESS_KEY="YOUR ACCESS KEY"
```

- For **Windows**:

```bash
set LT_USERNAME="YOUR_USERNAME" set LT_ACCESS_KEY="YOUR ACCESS KEY"
```

## Run Your First Test

> **Test Scenario**: Check out the sample [LambdaTest.php](https://github.com/LambdaTest/Php-PhpUnit-Selenium/blob/master/tests/LambdaTest.php) that we used for running a sample test using PHPUnit. This LambdaTest.php script tests a sample to-do list app by marking couple items as done, adding a new item to the list and finally displaying the count of pending items as output.

### Configuration Of Your Test Capabilities

**Step 4:** In [TestMu AISetup.php](https://github.com/LambdaTest/Php-PhpUnit-Selenium/blob/master/lib/TestMu AISetup.php) file, you need to update your test capabilities. This will validate your TestMu AI credentials for authentication purpose. Later, the code will select the basic capabilities such as OS, browser, browser version and so on.

> **Note:** You can generate capabilities for your test requirements with the help of **[Desired Capability Generator](https://www.testmuai.com/capabilities-generator/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium)**.

### Executing The Test

**Step 5:** The tests can be executed in the terminal using the following command:

```bash
composer single
```

Your test results would be displayed on the test console (or command-line interface if you are using terminal/cmd) and on TestMu AI Automation Dashboard.

## Running Parallel Tests Using PHPUnit Framework

Check out the sample [TestMu AIParallel.php](https://github.com/LambdaTest/Php-PhpUnit-Selenium/blob/master/tests/TestMu AIParallel.php) that we used for running parallel tests using PHPUnit.

### Executing Parallel Tests Using PHPUnit

To run parallel tests using **PHPUnit**, we would have to execute the below commands in the terminal:

```bash
composer parallel
```

Your test results would be displayed on the test console (or command-line interface if you are using terminal/cmd) and on TestMu AI Automation Dashboard.

## Executing All The Tests

To run both single and parallel tests at once using **PHPUnit**, we would have to execute the below command in the terminal:

```bash
composer test
```

## Testing Locally Hosted Or Privately Hosted Projects

You can test your locally hosted or privately hosted projects with TestMu AI Selenium grid using TestMu AI Tunnel. All you would have to do is set up an SSH tunnel using tunnel and pass toggle `tunnel = True` via desired capabilities. TestMu AI Tunnel establishes a secure SSH protocol based tunnel that allows you in testing your locally hosted or privately hosted pages, even before they are live.

Refer our [TestMu AI Tunnel documentation](https://www.testmuai.com/support/docs/testing-locally-hosted-pages/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium) for more information.

Here’s how you can establish TestMu AI Tunnel.

Download the binary file of:

- [TestMu AI Tunnel for Windows](https://downloads.lambdatest.com/tunnel/v3/windows/64bit/LT_Windows.zip)
- [TestMu AI Tunnel for macOS](https://downloads.lambdatest.com/tunnel/v3/mac/64bit/LT_Mac.zip)
- [TestMu AI Tunnel for Linux](https://downloads.lambdatest.com/tunnel/v3/linux/64bit/LT_Linux.zip)

Open command prompt and navigate to the binary folder.

Run the following command:

```bash
LT -user {user’s login email} -key {user’s access key}
```

So if your user name is lambdatest@example.com and key is 123456, the command would be:

```bash
LT -user lambdatest@example.com -key 123456
```

Once you are able to connect **TestMu AI Tunnel** successfully, you would just have to pass on tunnel capabilities in the code shown below :

**Tunnel Capability**

```
 "tunnel" => true
```

## Additional Links

- [Advanced Configuration for Capabilities](https://www.testmuai.com/support/docs/selenium-automation-capabilities/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium)
- [How to test locally hosted apps](https://www.testmuai.com/support/docs/testing-locally-hosted-pages/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium)
- [How to integrate TestMu AI with CI/CD](https://www.testmuai.com/support/docs/integrations-with-ci-cd-tools/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium)

## Documentation & Resources :books:

Visit the following links to learn more about TestMu AI's features, setup and tutorials around test automation, mobile app testing, responsive testing, and manual testing.

- [TestMu AI Documentation](https://www.testmuai.com/support/docs/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium)
- [TestMu AI Blog](https://www.testmuai.com/blog/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium)
- [TestMu AI Learning Hub](https://www.testmuai.com/learning-hub/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium)

## TestMu AI Community :busts_in_silhouette:

The [TestMu AI Community](https://community.testmuai.com/?utm_source=github&utm_medium=repo&utm_campaign=Php-PhpUnit-Selenium) allows people to interact with tech enthusiasts. Connect, ask questions, and learn from tech-savvy people. Discuss best practises in web development, testing, and DevOps with professionals from across the globe 🌎

## What's New At TestMu AI ❓

To stay updated with the latest features and product add-ons, visit [Changelog](https://changelog.lambdatest.com/)

## 🚀 LambdaTest is Now TestMu AI

👋 Welcome to TestMu AI, the next evolution of LambdaTest. As of January 2026, [LambdaTest is Now TestMu AI](https://www.testmuai.com/lambdatest-is-now-testmuai/) - we have evolved from a cross-browser testing cloud into a unified, AI-native quality engineering platform designed for the modern DevOps era.

Whether you have been part of the LambdaTest community for years or are just discovering TestMu AI, our mission remains the same: to help you ship faster with high-scale test execution, autonomous testing, and deep quality analytics.

### 🔄 Our Rebrand Journey

In 2017, we introduced LambdaTest with a clear mission: to become the world's most trusted cloud testing platform. We built a scalable, high-performance test cloud that eliminated flakiness, improved developer feedback cycles, and accelerated release velocity for teams worldwide.

As LambdaTest grew, we expanded the platform into Test Intelligence, Visual Regression Testing, Accessibility Testing, API Testing, and Performance Testing, covering the entire testing lifecycle. These capabilities enabled teams to test any stack, on any technology, at enterprise scale.

Over time, we rebuilt the architecture to be AI-native from the ground up. What began as LambdaTest's high-performance testing cloud has now evolved into TestMu AI, an AI-native, multi-agent platform redefining modern quality engineering.

We chose the name TestMu AI to reflect our shift towards intelligent, autonomous testing. While our identity has changed, our core technology and commitment to the testing community stay the same.

👉 Find [LambdaTest's New Home](https://www.testmuai.com/).

### 🔭 Explore TestMu AI

The same infrastructure LambdaTest customers relied on, now delivered through autonomous AI agents.

- [KaneAI](https://www.testmuai.com/kane-ai/)
- [Agent-to-Agent Testing](https://www.testmuai.com/agent-to-agent-testing/)
- [HyperExecute](https://www.testmuai.com/hyperexecute/)
- [Real Device Cloud](https://www.testmuai.com/real-device-cloud/)
- [Pricing](https://www.testmuai.com/pricing/)
- [Documentation](https://www.testmuai.com/support/docs/)