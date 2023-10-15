Welcome to a small introduction of bioinformatics. What is bioinformatics? Bioinformatics is a sub-branch of biotechnology where we take biological data to understand and analyze with multiple interface programs. Before we get started, we need to download some software and that would depend on your operating system. Your operating system (OS) is the program that runs your computer. For example, WindowsOS and MacOS are operating systems. How you're seeing this "README.md" file is through your operating system. Although bioinformatician use Windows and Mac for day to day use, where they store data and compile their analysis is through LinuxOS. How do you check what operating system you have? All apple products have MacOS, anything else uses WindowsOS EXCEPT Chrombook. Chrombook uses ChromeOS. 

# Requirements for this Lab
* A laptop
* A Github account
* LinuxOS
* Storage space (At least 15GB)
* An open mind set

# What is not required 
* Any prior history of coding

# Setting up your Github account
In order to access the data and use these programs. Please sign up to Github. Github is used by all computer science majors, huge tech companies, and researchers alike. For those who are interested in the world of bioinformatics or computer sicence, I would suggest keeping this account for future use. 

# Downloading LinuxOS

> PLEASE HAVE AT LEAST 2.7 GB OF FREE STOREAGE SPACE

These programs are BIG so please save any homework or projects on the cloud or on a hard drive and uninstall any games or apps on your computer that you haven't palyed in a long time. 

## Windows
Windows is a bit weird due to the fact that you need a virtual machine to support the linuxOS. VirtualBox is a free virtual machine program that can run all linuxOS. Lubuntu is the most light and most compatible linuxOS for windows and for VirtuaBox. Please download the following programs here:

- VirtualBox (https://www.virtualbox.org/) Downloads --> VirtualBox 7.0.10 platform packages section --> Windows hosts
- Lubuntu (https://lubuntu.me/) On the top left click on downloads --> click on the Desktop 64-bit for 22.04.3 LTS (jammy Jellyfish)

Once you have downloaded these two, **DO NOT TOUCH your lubuntu file!!** 
1. Double click on the virtualbox application file. Say yes to everything and do NOT change anything. 
2. Once you open the VirtualBox Manager, click on new --> in the 'Name' section put anything (ex. your_world)
3. In the ISO Image section click on the arrow to scroll for lubuntu in your folder
4. Version should be ubuntu (64-bit). Click next.
5. Once you click next, click next for the rest of them and do NOT change the settings. 
6. On the left hand side you will see your virutal world that you named, double click on it and give it a couple of minutes to set up. 

## Mac
MacOS is a Unix based operating system. Unix and Linux are sister programs, so essentially you have linux bulit into your OS. Your specific version of Unix is called Darwin. You can get access your program through the *Terminal* application. However, you night not have the git command and other developer tools installed by defult. To install these, type the folowing in your terminal and follow the instructions: 

```
xcode-select --install
```
Then hit return. By default, your home directory might not be shown in your sidebar. If you want it there, change that in Finder -> Preferences.

## Chrombook
ChromeOS is a Linux based operating system. You should be relieved as you only need to enable it. Please follow the following intstructions here: 

1. On your Chromebook, at the bottom right, select the time
2. Select Settings > Advanced > Developers 
3. Next to "Linux development environment" select Turn ON
4. Follow the on-screen instructions. Setup can take 10 minutes or more. 
5. A terminal window opens. That is what you'll be working on. You have a Debian 11 (Bullseye) environment. Side note: Not alot of researchers use Debian but a couple of gaming companies use this if they wanted to remaster old PC games. 

## Once you have all the required software/ programs
Once you have all the requirements to start the lab, let's have you open your shell/terminal. It is a black box and it would say either terminal or shell. To make sure 
you're on the Linux/Unix operating system you must have a "$" (or a "%" for Unix) at the end of your computer's name. If not, please make sure you have followed the 
directions above carefully and ask your teacher for help. Let's dowload the "Alien_DNA_tutorial" program. 

For MacOS users, please change your directory to your desktop by copying and pasting this code: 

```
$ cd desktop
```
Copy and paste (Ctrl + C | Ctrl + V for windows or command + C| 
command +V for mac) this code in your terminal/shell without the $:

```
$ git clone https://github.com/FastV1per/Alien_DNA_tutorial.git
```
Hit return/enter

git is github, clone is the command to download, and the URL is the link to this tutorial.

In english, I've asked github to send me a copy of this program for me to 
use on my own computer.

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
cd is the command for change directory

Type 'ls' and you should see a README.md file and a alien_dna file. If alien_dna is highlighted a different color, that means you can jump into that file using the cd 
command. 

Go ahead and get use to using these commands by exploring your computer.

If you want to go back to a previous directory type:

```
$ cd ..
```
Typing cd by itself will result in you going to the root directory. The root directory is the computer's own homepage and you will see all the files that your computer is carrying.

MacOS users, as a reminder you will be working on your desktop directory, so when you feel 
comfortable moving around the inside of your computer, please cd to your desktop to work on this lab.

> Tip: Instead of writing the directory out word by word, you can write the first 2-3 words of the directory you want and hit tab and hit enter/return.   

If you do not see Alien_DNA_tutorial as a file make sure you have copied and pasted correctly, LinuxOS is case sensitive, meaning, if there is one letter off, linux will give you a error and will not run your code. Otherwise, good luck on the lab!

# DNA from outer space
You and your team of researchers were sent on a mission to record the location of a local meteor shower. When you and your team get there, you noticed some of the rocks remainded 
intact. Excited to see pieces of space rock, you and your collegues rush to collect them in order to test their components.One night, one of your team members analyzed something 
peculiar. These strange rocks are carrying alien DNA! Quickly, your colleague has collected a couple of more samples and put them into a sequencer to 
sequence. The next day, you see the data and wonder; does any of this alien DNA have a distant relative of a known species here on earth?

## Goals of Today
* Using basic C language using LinuxOS 
* Understand biological data
* Editing and transforming your data to fit a program's needs
* Analyze data using BLAST and UCSC Genome Browser

### Accessing your data

In order to acess the data, you should've already git clone the Alien_DNA_tutorial file into your directory (for Windows it's your files folder and for Mac/chrome it should show up 
on your desktop page.)

1. You data is going to be found in the alien_dna directory, so change your directory to go there.

2. Once you're in the alien_dna directory there should be a dateset called: "alien_dataset.fasta". A FASTA file is a text-based format for representing either nucleotide sequences or 
protein sequences, in which based pairs or amino acids are represented using single-letter codes. Because of how long DNA/protein sequences can get, a fasta file is a great way to compress 
this data. Here is an example of a FASTA file below:

> ![Screenshot of a fasta file](fasta.file_example.png)

Top line is a simgle-line description of the species it is, the region of 
the gene it's in, and then followed by the sequence itself.

* Q1. Is this a DNA sequence or a protein sequence? Why?

3. Since our computers wont allow is to open the data itself, we can preview our dataset by typing this:

```
$ zless alien_dataset.fasta
```
Hit enter/return

You should see something like this:

[insert image here]

To exit out of viewing a file press q on your keyboard.

* Q2. Does this file look right to you? What do you think these 'N' mean?

* Q3. Is this supposed to be a DNA sequence or a protein sequence? Why?

### Editing your data
Normally, you do not have to edit your data, however, if by chance that a program doesn't take your sequenced data, you may have to edit the datafile to fit the program's needs. To do this 
we need to tell our computer that we want to take out any letters that are not DNA base pairs.

##BLAST
After you have edited the data to fit the blast program, go to the main blast website here: (https://blast.ncbi.nlm.nih.gov/Blast.cgi) 

1. Since we are working with nucleotides we want to compare our data to other nucleotides. Click on the Nucleotide BLAST tab
2. In the Enter Query Sequence, copy and paste the edited sequence only. 
3. Under the Program Selection, click on somewhat similar sequences (blastn). 
> The reason being is that we are not certain if there will be any spieces that has the exact same DNA sequence to our alien dna. If we were to select the Highly similar sequence option: (1) It will take a long time for blast to sort thorugh all of its stored sequences and (2) Two different spieces 
will not have the exact DNA sequence. So by selecting somewhat similar sequences we are guaranteed a better hit of species that could be related to our sampled DNA. 
4. Once you have selected all of the right parameters, at the bottom click on BAST!
5. After blasting the sequence, record the spieces that the alien could be related to.
6. Repeat these steps for the other samples.

## Understanding your output

* Q4. Which animals is our alien DNA sample most closely related to and by how much? Would you say that the percentage of how relative they are is accurate? Why?
* Q5. Do you think this alien looks like its most closely related spiecies here on Earth? Why or Why not?
