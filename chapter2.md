# Install Fest

> Installs all the tools you need to be a successful developer

Before we even begin, make sure you have a text editor installed. In this class we support [Sublime Text (recommended)](http://www.sublimetext.com/3) or [Atom](https://atom.io)

Why do we recommend Sublime Text? Sublime Text has objectively better performance on any computer. If you have a computer that's over two years old then we recommend you use Sublime as it won't slow down your system. If you have a newer computer (less than 2 years old) feel free to use either Atom or Sublime. You can even try them both and decide which one you like best. Don't base your decision on looks alone - both Atom and Sublime can be themed.

## Welcome to Installfest!                         

Running these commands in a new terminal window will install all the required software you need to be successful in WDI.                        
### 0. Open a terminal window

Open the terminal application and ensure you're in your "Homme" directory by running this command: `cd`


### 1. Install Homebrew

Homebrew is a package manager for OS X. We'll be using it to install developer tools. Install Homebrew with this command:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Time out!

After some commands you'll need to refresh your terminal environment. Whenever you see __*"REFRESH TIME!"*__ you need to run this command:

```
source .bashrc && source .bash_profile
```

### 2. Install xcode CLI tools

These are some behind the scenes programs that allow you to install other programs (things like compilers get installed here). To install the Xcode developer tools run this command:

```
xcode-select --install
```

### 3. Install RVM

RVM stands for Ruby Version Manager. It allows you to install and switch between multiple versions of the Ruby programming language. There are two commands you'll need to run in order to install RVM. Run these commands before moving on:

```
# Part 1. If this fails let us know. This command has to do with securely downloading the RVM package
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3

# Part 2. This second command will do the job of actually installing RVM
\curl -sSL https://get.rvm.io | bash -s stable
```

__*REFRESH TIME*__

Source .bashrc and .bash_profile (just in case) so you can use RVM

```
source ~/.bashrc && source ~/.bash_profile
```

### 3a. Install Ruby

This command will install the latest version of Ruby (an open source programming language)

```
rvm install 2.3.1
```


### 4. Install nvm

nvm is like RVM but for Node.js. It allows you to install multiple versions of Node.js at the same time. Run this command to install nvm (which is purposely kept all lower-case):

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh | bash
```

__*REFRESH TIME*__

```
source ~/.bashrc && source ~/.bash_profile
```

### 4a. Install latest version of Node

This will install the latest version of Node.js and make it set it as your default Node version (if you were to have multiple Node.js versions installed, this would be the version used if you don't specify one for a project).

```
nvm install 6 default
```

### 5. Install MySQL

MySQL is a relational database engine. You install MySQL through Homebrew, your Mac's new package manager that we installed earlier, using this command:

```
brew install mysql
```

### 6. Install MongoDB

MongoDB is a non-relational (A.K.A. "NoSQL") database engine. You'll install MongoDB through Homebrew by running:

```
brew install mongodb
```

### 7. Install Xcode

Xcode is quite a large package so be prepared to wait a bit for it to download.

__Do you have the App Store app installed on your Mac?__

*If yes:* Open the App Store and search for "Xcode". It should be free. Press the button to install it.

*If no:* In your browser go to [https://developer.apple.com/xcode/download/](https://developer.apple.com/xcode/download/), download Xcode, then double click the package to begin installing once it's fully downloaded.

__Xcode is a large program and takes a while to download so don't worry if it seems slow__

### 8. Bonus material and extras

### Colored terminal

Your default terminal window is ugly. You can fix that by choosing a new theme in the Terminal applications prefrence pane or download one from the Internet. You might also want to have a multi-colored terminal like Jim and I have. To enable colored output you'll need to delete one character in your `.bashrc` file. If you want to prettify your terminal just get our attention and we'll be happy to help.

#### Sublime Text and Atom themes

Google is your friend. Let one of us know if you're interested in changing your editor's theme and we can point you in the right direction.

#### DB Browser for SQLite

This tool will come in handy later on in the course when we start using databases. The [SQLite Browser](http://sqlitebrowser.org) allows you to open a database file and browse it visually instead of through the command line.

#### Postman

[Postman](https://www.getpostman.com) is a tool that lets you create HTTP requests and explore and test local or remote APIs. This will come in handy later on in the course. This is basically a GUI application for the built in `curl` command.

#### Robomongo

[Robomongo is a GUI application](https://robomongo.org) that allows you to explore a MongoDB database visually, similar to the DB Browser for SQLite.

#### Sequel Pro

[Sequel Pro is a GUI application](http://sequelpro.com) that lets you explore a variety of remote or local databases visually. It works on most relational database egines (except SQLite) and is especially well suited to browsing local and remote MySQL repositories.

echo "\n"
echo ""
echo " You should now have all the required software for   "
echo " this course. If you have not installed Xcode yet do "
echo " so by searching for it on the App Store or head to  "
echo " https://developer.apple.com/xcode/download/ to      "
echo " download it manually.                               "
echo "-----------------------------------------------------"
echo " You may also want to download some of these great   "
echo " (but optional) helpful tools:                       "
echo "  * DB Browser for SQLite: http://sqlitebrowser.org  "
echo "  * Postman: https://www.getpostman.com              "
echo "  * Robomongo (MongoDB GUI): https://robomongo.org   "
echo ""
else
echo "Quitting InstallFest. Run me again when you're ready to install the required tools."
fi



BONUS STUFF FOR LATER?
----------------------
1. Colorize terminal
2. Install better terminal themes
