# Problem Set 1 (continued)

## Due January 17 @ 11:59pm

---

### Part 4: Download and install Java 8 SDK

1. You might already have some or all components of Java installed on your computer. Unless you have a very good reason for keeping other versions of Java around, we recommend that you to uninstall all existing versions of Java from your computer. 

This will happen relatively automagically with Mac OSX, but **with Windows 10** you might need to do this yourself, as follows: Go to ``Control Panel -> Programs -> Programs and Features``. Then un-install all programs beginning with ``Java`` or ``java``, such as ``Java SE Development Kit``, ``Java SE Runtime``, ``Java X Update``.

2. Although there are several newer versions of Java, we'll be using Java 8. Download the Java SE Development Kit 8u191 (the last three numbers might be different, that's okay!) for your operating system from [here](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html). Don't forget to click the radio button indicating that you agree to the terms of the license.

3. After you download the .dmg (Mac) or .exe (Windows), double-click it to start the installation. Click as needed to complete the installation.

### Part 5: Configure and validate Java installation
#### Windows 10 users *If you are using Windows 7, proceed at your own risk.*

1. Launch ``Control Panel -> (Optional) System and Security -> System``. 

2. Click ``Advanced system setting`` in the left pane.

3. Select the ``Advanced`` tab, and click ``Environment Variables`` button.

4. Under ``System Variables`` (the bottom pane), the scroll down to select ``Path``, then select ``Edit...``.

5. In Windows 10, you will see a table listing all the existing ``PATH`` entries.  Click ``New`` then enter the JDK's ``bin`` directory, which should be ``c:\Program Files\Java\jdk-8.{x}\bin``, where `{x}` is replaced with the version number you installed in Part 4, Step 2, above. Then Select ``Move Up`` to move this entry all the way to the top of the table.


#### Max OSX users ####
1. Launch a Terminal. You can do this by finding the Terminal app in your Applications folder, or by going up to the magnifying glass in the upper right corner of your screen and then searching for Terminal.

2. At the prompt, type `java -version` and you should see


### Part 4: Using GitHub 
1. Create a folder on your computer for this class called CS2 or CS1102. I have mine on my Desktop so it's easy to find.

2. By now you should have received an email with an invitation to accept Problem Set 0.5. If you didn't receive the email or can't find it, you can find the link to the invitation on Canvas. Accept the invitation, which will create a repository just for you to use to complete this assignment.

3. Follow the link to the repository that was created, and locate the green "Clone or download" on the right. Click that button, and then copy the the URL beginning with ``https://`` that appears, as shown below.

<img src="img/clone.png" width="700"  />

4. You will need the URL in Part 5, so paste it somewhere you can easily access it in a few minutes. And of course, you can always find it again by just going to github.com and selecting this problem set repository. 



### Part 5: Downloading and installing Atom



### Part 6: Writing your first Java program



### Part 7: Submitting your first problem set to GitHub Classroom
