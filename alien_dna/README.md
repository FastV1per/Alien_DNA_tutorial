"Hello world!"

Welcome to a small introduction of bioinformatics. What is bioinformatics? Bioinformatics is a sub-branch of biotechnology where we take biological data to understand and analyze with multiple interface programs. Before we get started, we need to download some software and that would depend on your operating system. Your operating system (OS) is the program that runs your computer. For example, WindowsOS and MacOS are operating systems. How you're seeing this "README.md" file is through your operating system. Although bioinformatician use Windows and Mac for day to day use, where they store data and compile their analysis is through LinuxOS. How do you check what operating system you have? All apple products have MacOS, anything else uses WindowsOS EXCEPT Chrombook. Chrombook uses ChromeOS. 

# Requirements for this Lab
* A laptop
* Good internet
* A Github account
* LinuxOS
* Storage space (At least 15GB)
* An open mind set

# What is not required 
* Any prior history of coding

# Setting up your Github account
In order to access the data and use these programs. Please sign up to Github. Github is used by all computer science majors, huge tech companies, and researchers alike. For those who are interested in the world of bioinformatics or computer sicence, I would suggest keeping this account for future use. 

# Downloading LinuxOS

**PLEASE HAVE AT LEAST 2.7 GB OF FREE STOREAGE SPACE**
These programs are BIG so please save any homework or projects on the cloud or on a hard drive and uninstall any games or apps on your computer that you haven't palyed in a long time. 

## Windows
Please download the following programs here:


## Mac
MacOS is a Unix based operating system. Unix and Linux are sister programs, so bascially you'll have an easier time running linux programs anywhere. Please download the following program here:

## Chrombook
ChromeOS is a Linux based operating system. You should be relieved as you only need to enable it. Please follow the following intstructions here: 

1. On your Chromebook, at the bottom right, select the time
2. Select Settings > Advanced > Developers 
3. Next to "Linux development environment" select Turn ON
4. Follow the on-screen instructions. Setup can take 10 minutes or more. 
5. A terminal window opens. That is what you'll be working on. You have a Debian 11 (Bullseye) environment. Side note: Not alot of researchers use Debian but a couple of gaming companies use this if they wanted to remaster old PC games. 

## Once you have all the required software/ programs
Once you have all the requirements to start the lab, let's have you open your shell or your terminal. It is a black blox and it would say either terminal or shell. to make sure you're on the Linux OS you must have a "$" at the end of your name. If not, please make sure you have followed the directions above carefully and ask your teacher for help. Let's dowload the "Alien_DNA_tutorial" program. Copy and paste (Ctrl + C | Ctrl + V for windows or command + C| command +V for mac) this code in your terminal/shell without the $:

```
$ git clone https://github.com/FastV1per/Alien_DNA_tutorial.git
```

git is github, clone is the command to download, and the URL is the link to this tutorial.

In english, I've asked github to send me a copy of this program for me to work on.

### The two commands that you will forever use

There are two commands that you will be using for the rest of your coding careers and that's (1) how to look into a file and (2) how to get into or out of a file.

#### ls
How do I know if Alien_DNA_tutorial file is downloaded into linux? You should be able to see your files by typing: ls

ls is the command for list, so if you want to know where you are in a directory, type this command.

#### cd
What if I want to get into a file called alien_dna? You can jump into that directory by typing the command cd, here's how it looks like:

```
$ cd Alien_DNA_tutorial
```
Cd is the command for change directory

Type 'ls' and you should see a README.md file and a alien_dna file. If alien_dna is highlighted a different color, that means you can jump into that file using the cd command. 

Go ahead and get use to using these commands by exploring your computer.

If you do not see Alien_DNA_tutorial as a file make sure you have copied and pasted correctly, LinuxOS is case sensitive, meaning, if there is one letter off, linux will give you a error and will not run your code. Otherwise, good luck on the lab!

# DNA from outer space
You and your team of researchers were sent on a mission to record the location of a local meteor shower. When you and your team got there, some of the debris remained intact. Excited to see pieces of rock fallen from the shy, you and your collegues ruch to collect any pieces that you could find in order to test their components.One night, one of your team members analyzed these strange rocks and have found strange alien DNA on them. Quickly, your colleague has collected a couple of more samples and put them into a sequencer to sequence the data into a file. When you were given the data. You wonder if this alien DNA could bre realted to a known species here on earth.


## Goals of Today
* Using basic C language using LinuxOS 
* Understand biological data stored through a FAFSTA file
* Editing and transforming your data to fit a program's needs
* Analyze data using BLAST

### Acessing your data

Let's get the data, to do this, change the directory to alien_dna

