# CYE163

# This is a writeup for the overthewire Bandit wargames. 

# Bandit
This level required me to use ssh to gain access to the information needed for level 1. I read through the SSH link provided by overthewire ![Screenshot 2024-02-10 180553](https://github.com/th3j35ter/CYE163/assets/57239953/14f5a8fc-980a-4a10-8ee9-5a1acde6d5d7)

The instructions required a specific port connection and when i first tried this by using this line:

ssh bandit.labs.overthewire.org -p 2220

![Screenshot 2024-02-10 180850](https://github.com/th3j35ter/CYE163/assets/57239953/c0985d79-7447-4bfa-9f5b-8a4fab99220e)

Since the first attempt resulted in failure I used the "-l" option to pass in the username "bandit0". This attempt looked like this:

ssh bandit.labs.overthewire.org -p 2220 -l bandit0

![Screenshot 2024-02-10 181138](https://github.com/th3j35ter/CYE163/assets/57239953/95cbe079-31c1-449e-ae4b-f884175a5f12)

With this allowing me access I successfully completed the first level.

![Screenshot 2024-02-10 181245](https://github.com/th3j35ter/CYE163/assets/57239953/63333162-17b3-4a4d-a52d-518ebb5b1be4)

# Bandit 0

The goal for this level is to access the password stored in a file named "readme" which is located in the home directory. 

I opt to use the ls (list directory contents) command which is provided in a link by overthewire on the page.

![Screenshot 2024-02-10 182551](https://github.com/th3j35ter/CYE163/assets/57239953/a2872431-8938-41a9-99c9-ee8b5a4448ae)

This identifies the file "readme" in my directory and I use another command provided by overthewire called cat (concatenate files and print on the standard output) which prints out the password that I copy.

![Screenshot 2024-02-10 182714](https://github.com/th3j35ter/CYE163/assets/57239953/10347754-bd84-4860-b287-255e7e4986c9)

![Screenshot 2024-02-10 182832](https://github.com/th3j35ter/CYE163/assets/57239953/9de8567c-727a-4e73-abdf-75c9457fb563)

# Bandit 1

Before continuing, I need to exit out of the server to move on to the next level so I log out of the server.

![Screenshot 2024-02-10 183036](https://github.com/th3j35ter/CYE163/assets/57239953/d3423baf-5372-47bb-8e5b-ffed60bd66c2)

I used an incorrect hostname at first but corrected it to access the next level:

ssh bandit1@bandit.labs.overthewire.org -p 2220 

![Screenshot 2024-02-10 183724](https://github.com/th3j35ter/CYE163/assets/57239953/58415b12-5eb8-4b51-8bb6-ff1149496ddb)

After messing up the password several times I copy and pasted it into the terminal, gaining access to the home directory of bandit1.
