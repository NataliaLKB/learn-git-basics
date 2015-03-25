The command line
Before we start

You may want to set up a remote development environment (particulary if you are not running OS X or Linux).

Sign up for Nitrous.IO, have a quick read through the Getting Started guide and set up a Node.js box. You can then login and open up a console window.

Or, if you prefer, just open a terminal window on your computer.

Additional learning resources

After you have worked through the quick summary below, you can take a look at The Command Line Crash Course.

And to get the commands into your head, have a go at this course on Memrise.

A quick step-by-step summary of the basics

Where am I?

pwd
"Print Working Directory"

What's in my current directory?

ls
"LiSt"

Show me hidden files, as well:

ls -a
And show me details of each file:

ls -l
Show me both details and hidden files:

ls -al
Make a new directory called things:

mkdir things
"MaKe DIRectory"

Change to the things directory:

cd things
"Change Directory"

Go up a directory level:

cd ..
Return to my home directory:

cd ~
Create a new file with nothing in it:

touch one.txt
touch changes the access and modification time of a file (i.e. it touches it), but this also creates a new file if none exists with the name given.

Make a copy of it:

cp one.txt two.txt:
"CoPy"

Change its name:

mv one.txt three.txt
"MoVe"

And delete it:

rm three.txt
"ReMove"

Remove all files and folders without prompting and with no chance of recovery:

rm -rf .
"ReMove Recursively and Forcefully" everything in your current working directory. Don't do this. Instead, mkdir ~/tmp and mv anything you no longer want to there.

Remove a directory:

rmdir things
"ReMove DIRectory" (you need to empty it first)

Put some text into a file:

echo "hello" > greet.txt
And display the contents:

cat greet.txt
"conCATenate and list"

Complete the name of a file without having to type it all:

touch afilewithalongname
cat af<tab>
(i.e. use the tab key)

Create a file within a folder within a folder:

mkdir one
mkdir one/two
echo "hello" > one/two/three.txt
Read its contents:

cat o<tab><tab><tab>
(i.e. use the tab key three times in succession)

Cycle through previously-entered commands:

Use the up and down arrow keys

Edit a previously-entered command:

Use the left and right arrow keys