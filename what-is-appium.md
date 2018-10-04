# What is Appium {#what-is-appium}

**Appium** is an _open source_ test automation tool for mobile applications. It allows you to test all the three types of mobile applications: _native_, _hybrid_ and _mobile web_.

It also allows you to run the automated tests on actual devices, emulators and simulators.

Today when every mobile app is made in at least two platform iOS and Android, you for sure need a tool, which allows testing cross platform. Having two different frameworks for the same app increases the cost of the product and time to maintain it as well.

The basic philosophy of Appium is that you should be able to reuse code between iOS and Android, and that’s why when you see the API they are same across iOS and android. Another important thing to highlight here is that unlike Calabash, Appium doesn’t modify your app or need you to even recompile the app.

Appium let’s you choose the language you want to write your test in. It doesn’t dictate the language or framework to be used.

## Architecture {#architecture}

So how does Appium do all this? Let’s try to understand what happens behind the scenes.

When you download the Appium app you are basically downloading the server. The server is written in Node.js and implements the Selenium WebDriver. It allows one to use available WebDriver client to fire your tests. And then your mobile app acts precisely like a web app where the DOM is represented by View hierarchy.

So this server basically exposes REST api which performs the following actions:

```
1) Receives connection from client
2) Listen command
3) Execute command
4) Respond back the command execution status

```

In terms of architecture diagram, below is how Appium can be explained.

![](/assets/Appium_Architecture.jpg "Screen")

