# Problem Set 1 (continued)

## Due January 17 @ 11:59pm

---

### Part 4: Download and install Java 8 SDK

1. You might already have some components of Java installed on your computer. Unless you have a very good reason for keeping other versions of Java around, we recommend that you uninstall all existing versions of Java from your computer (instructions: [Mac](https://www.java.com/en/download/help/mac_uninstall_java.xml), [Windows](https://www.java.com/en/download/help/uninstall_java.xml)). 


2. Although there are several newer versions of Java, we'll be using Java 8. Download the Java SE Development Kit 8u191 (the last three numbers might be different, that's okay!) for your operating system from [here](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html). Don't forget to click the radio button indicating that you agree to the terms of the license.

3. After you download the .dmg (Mac) or .exe (Windows), double-click it to start the installation. Click as needed to complete the installation.


### Part 5: Configure and validate Java installation
#### Windows 10 users (If you are using Windows 7, proceed at your own risk.)

1. Launch ``Control Panel -> (Optional) System and Security -> System``. 

2. Click ``Advanced system setting`` in the left pane.

3. Select the ``Advanced`` tab, and click ``Environment Variables`` button.

4. Under ``System Variables`` (the bottom pane), the scroll down to select ``Path``, then select ``Edit...``.

5. In Windows 10, you will see a table listing all the existing ``PATH`` entries.  Click ``New`` then enter the JDK's ``bin`` directory, which should be ``c:\Program Files\Java\jdk-1.8.{x}\bin``, where `{x}` is replaced with the version number you installed in Part 4, Step 2, above. You can determine exactly what it is by looking in that directory called `Java`. Then Select ``Move Up`` to move this entry all the way to the top of the table.

6. Open a CMD shell by clicking the ``Start`` button, then selecting ``Windows System -> Command Prompt``.

7. Type ``path`` at the prompt, and you should see output that begins like this, where again the {x} is the exact version you installed from Oracle in Part 4, Step 2.

``PATH=c:\Program Files\Java\jdk-1.8.{x}\bin;``

8. Type ``java -version`` and you should see something like this:

```java

java version "1.8.0_191"
Java(TM) SE Runtime Environment (build 1.8.0_191-b12)
Java HotSpot(TM) 64-Bit Server VM (build 25.191-b12, mixed mode)

```

9. Type ``javac -version`` and you should see something like this:

```java

javac 1.8.0_191

```

10. If you get an error message (e.g., "command java not found") or if the numbers are different (e.g., java 1.7...), then something is not right. Email the instructor and the TAs.

#### Max OSX users ####
1. Launch a Terminal. You can do this by finding the Terminal app in your Applications folder, or by going up to the magnifying glass in the upper right corner of your screen and then searching for Terminal.

2. At the prompt in Terminal, type ``java -version`` and you should see something like this:

```java

java version "1.8.0_191"
Java(TM) SE Runtime Environment (build 1.8.0_191-b12)
Java HotSpot(TM) 64-Bit Server VM (build 25.191-b12, mixed mode)

```


3. Type ``javac -version`` and you should see something like this:

```java

javac 1.8.0_191

```

4. If you get an error message (e.g., "command java not found") or if the numbers are different (e.g., java 1.7...), then something is not right. Email the instructor and the TAs.


### Part 4: Install and configure Atom

In this course we'll be using GitHub's Atom editor to write our Java code, and we'll be using git and GitHub to distribute and collect problem sets. Fortunately, git and GitHub are nicely integrated into the Atom editor. You can find a lot of [video tutorials on using Atom](https://www.leveluptutorials.com/tutorials/atom-editor-tutorials) though you probably won't need much guidance since we'll be using only a small part of its functionality.

1. [Download Atom](https://atom.io). Double click the downloaded file unzip it (if necessary), then move Atom to a place on your computer where it will be easy to find (e.g., in the Applications folder or on your desktop).

2. Launch Atom. There are a few tabs or frames that open automatically, which you can close by clicking the "X" in the upper right corner of the tab or frame. (If all these windows keep popping up when start Atom, you can turn them off in the Preferences and by clicking on the ``Do not show Welcome message`` on the Welcome tab.)

3. You now need to install an Atom package that will customize Atom for use in this class. From Atom's menu bar, click the Atom menu, and then select Preferences to open the Settings menu. You can also access the settings via a keyboard shortcut: in MacOS hold down the ``command``key and type a comma; in Windows, hold down the ``control`` key and type a comma.

<img src="img/atommenu.png" width="300"  />

4. On the left of the Settings area, you’ll see a menu with items like Core, Editor, URI Handling, and so on. Click on the menu item that says Install, which has a plus-sign icon next to it.

<img src="img/install.png" width="600"  />

5. In the search box that appears, enter ``platformio-ide-terminal``. Click Install button for ``platform-ide-terminal``, and wait for installation to complete.


### Part 5: Get a local copy of the repository from GitHub

1. Create a folder on your computer for this class called ``CS2`` or ``CS1102``. I have mine on my Desktop so it's easy to find, but you are free to put it wherever is convenient for you.

2. Look up at the top of this webpage you are on right now, and locate the green ``Clone or download`` on the right. Click that button, and then copy the the URL beginning with ``https://`` that appears, which will look something like this, below:

<img src="img/clone.png" width="700"  />

3. In Atom, go to ``Packages -> Command Palette -> Toggle``.

4. In the pop-up window that opens, start typing ``GitHub``, and the GitHub: commands will appear. Select ``GitHub: Clone``.

5. Paste the URL from Part 1 in the first box, and the path to the **course folder** you created to Part 1 in the second box.

6. Click the ``Clone`` button. This will copy your personal ps0.5 repository to your computer. 

**NOTE:** If you end up with an empty repository following theese instructions, do one of the following (1) [use the GitHub Desktop app](https://desktop.github.com) to do your cloning (recommended for Windows users); or (2) in Atom, go to ``Packages -> platform-ide-terminal -> New Terminal``; then type ``git clone`` followed by the link to your repository, enter your GitHub username and password when prompted. Your repository will be cloned to your home directory.


### Part 6: Edit a file and push edits to GitHub

1. If you just did Part 5, you should see the contents of the repository in Atom. If you can't see the ps0.5 repository, then go to `File -> Open`, and navigate to your class folder, where you should find your local respoitory. Select it and click ``Open``.

2. You should now see something like this, below, with a tree structure showing the files in your current directory in the left pane and an empty pane on the right. (Feel free to close any of the pesky Welcome tabs and panes that Atom likes to open up.)

<img src="img/atom1.png" width="700"  />


3. Click on ``src`` to view the code for this assignment, then click on ``HelloWorld.java``. code will appear in the panel on the right. Find where you see this in the code:

```bash
System.out.println("Hello, World!")
```

Replace the words ``Hello, World!`` with your favorite greeting.

4. From the ``File`` menu, select ``Save`` (or use your usual keyboard shortcut for saving, like command-s in MacOS or control-s in Windows).

5. Go to ``Packages -> GitHub -> Toggle Git Tab``.

6. The Git tab will open, and you'll see something like this, below. Click ``Stage all``.

<img src="img/atom2.png" width="700"  />

7. Type a comment explaining what you did and why where it says ``Commit message``.

8. Click ``Commit to master``.

9. Click the ``Push`` on the right in the bottom menubar, between ``master`` and ``files``. 

9. Go to GitHub and find your respository for this problem set. You should see the changes reflected in your problem set repository and see ``last updated 1 minute ago`` (or thereabouts). This is what we will grade. Congratulations! You are ready for Problem Set 1.

