# How To Install Anything

This is  repository to  help developers to install step by step software for Mac. If you are new to Mac, I hope this will help you.

Let start step by step.

### Install MongoDB for Mac

1. Check your MacOS version **(I have MacOs 13.5 )**

2. Check which version of MongoDB works according your MacOS version. Take a look at this link to know which one is right for you.      **https://www.mongodb.com/docs/manual/administration/production-notes/#std-label-prod-notes-supported-platforms**

3. Install Homebrew for Mac
Homebrew is package manager that is like an asistant for Mac that helps you install other programs like MongoDB.

Now, open your terminal (command + space key), then type **terminal**,  press **return** and terminal will appear. There paste this link:

    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

4. Check if Homebrew is installed correctly typing this in the terminal.

        `brew --version`

Something like this should appear in your terminal.

    Homebrew 4.3.1

5. Now proceed typing this to your terminal.

        `brew tap mongodb/brew`

6. Now type this to your terminal

        brew install mongodb-community 

If you type this into your terminal, brew will install the mongodb-community package more stable, that means the most compatible version according to your Operating System (OS).

7. At this point you are goint to be ask to allow keychain access related to github.com. So go to Keychain access ( or a window is goint to appear), then in the passwords column, double click on github.com, then go to **Access Control** and select **Allow all applicationsto access this item.**

8. Now type in your terminal:

        brew services start mongodb/brew/mongodb-community

Then you type:

    brew services list

And you should get:

    Name                Status          User                File
    mongodb-community   **started**     *YourUserName*      *~/Library/LaunchAgents/homebrew.mxcl.mongodb-community.plist*

9. Then to interact with the database and to see the data you storage, you should also install the **Mongo Shell.** I tell you this because after I did these steps when I typed mongo in my terminal I obtained this:

        -bash: mongo: command not found

to solve this run this command in your terminal:

        brew install mongodb-community-shell

Now you can run this command on your terminalto start the mongo shell

        mongo
        >

10. After these you are all set you start the mongo shell and storage your data in the database.



