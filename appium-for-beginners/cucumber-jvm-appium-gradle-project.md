# Cucumber-JVM-Appium - Gradle Project {#cucumber-jvm-appium---gradle-project}

### Creating Gradle Project {#creating-gradle-project}

You can choose to create a gradle project. Below steps will guide you for the same.

* Select **New Project**
* In the New Project window, select **Gradle** on the left side of the screen as shown below. If the SDK is already defined in IntelliJ then it will pick up from there, else click New and select the installation folder of the desired JDK. 
  ![](/assets/Screen Shot 2016-10-05 at 7.34.41 AM.png)
* Click **Next**
* Give a **GroupID**, **ArtifactID**, and a **Version **for the project. Click Next.![](/assets/Screen Shot 2016-10-05 at 7.35.04 AM.png)

* Select the option of "**Use auto-import**" and "**Create directories for empty content...**". Click Next![](/assets/Screen Shot 2016-10-05 at 7.35.18 AM.png)

* Lastly enter a **project name** and **project location** and click on **Finish**.![](/assets/Screen Shot 2016-10-05 at 7.35.32 AM.png)

It should create a project with following structure.![](/assets/Screen Shot 2016-10-05 at 7.52.09 AM.png)

### Adding dependencies to build.gradle {#adding-dependencies-to-buildgradle}

Open build.gradle file and copy the below two lines

`compile 'io.appium:java-client:4.0.0'`

    ```testCompile 'info.cukes:cucumber-java:1.2.4',
                'info.cukes:cucumber-junit:1.2.4'


### Adding app folder {#adding-app-folder}

Once the project is created, created folder called **apps** and put the **.apk** file there which is your application under test.



