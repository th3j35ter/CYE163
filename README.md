# CYE-163
This is a writeup for the overthewire Bandit wargames.

- [Table of Content](#Table-of-Content)
- [Bandit](#bandit)
- [Bandit 0](#bandit-0)
- [Bandit 1](#bandit-1)
- [Bandit 2](#bandit-2)
- [Bandit 3](#bandit-3)
- [Bandit 4](#bandit-4)
- [Bandit 5](#bandit-5)
- [Bandit 6](#bandit-6)
- [Bandit 7](#bandit-7)
- [Bandit 8](#bandit-8)
- [Bandit 9](#bandit-9)
- [Bandit 10](#bandit-10)

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

[Back To Top](#Table-of-Content)

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
Since the objective of this level is to access the password located in a file called "-" I used ls to identify that the file was there.

![Screenshot 2024-02-12 082708](https://github.com/th3j35ter/CYE163/assets/57239953/49a58a9f-7537-4afc-94c9-52a73975f622)

Using the provided google search links by overthewire I was able to identify how I needed to format the "cat" command to pull the password.

![Screenshot 2024-02-12 082839](https://github.com/th3j35ter/CYE163/assets/57239953/3cb760a2-cf62-4914-92b5-a00d27eba8f7)

<details>
  <summary>
  The password is:
</summary>
  rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
</details>

# Bandit 2
In order to connect to Bandit2 I used the command:
  
  ssh bandit2@bandit.labs.overthewire.org -p 2220

![Screenshot 2024-02-12 083327](https://github.com/th3j35ter/CYE163/assets/57239953/9351e1b5-e101-4393-aee1-89e1050175b9)

The objective for this level is to get the password stored in a file called "spaces in this filename".

![Screenshot 2024-02-12 083528](https://github.com/th3j35ter/CYE163/assets/57239953/e549d987-0b91-4120-a90d-a7f97c25889f)

After my first attempt where i tried "cat spaces in this filename" this happened:

![Screenshot 2024-02-12 083827](https://github.com/th3j35ter/CYE163/assets/57239953/874f40a7-bfd4-494c-8722-b82203cc3298)

I figured if its checking each word individually for a filename then I should wrap the name in quotes. This worked and I was able to read the content of the file.

<details>
  <summary>The password is:</summary>
  aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
</details>

# Bandit 3
After identifying the password I exited from the server and connected to Bandit3.

![Screenshot 2024-02-12 084155](https://github.com/th3j35ter/CYE163/assets/57239953/b0534adb-3f9f-410a-b9ad-bbf186e087c9)

The goal for this level is to retrieve the password stored in a hidden file located in the inhere directory.

I utilized the 'find' command and identified the name of the file. 

![Screenshot 2024-02-12 084900](https://github.com/th3j35ter/CYE163/assets/57239953/7a1a40d1-05a2-4eeb-b908-cd8a2021ea50)

Using the 'cat' command it was simple to pull the password for the next level out.

<details>
  <summary>The password is:</summary>
  2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe  
</details>


![Screenshot 2024-02-12 085112](https://github.com/th3j35ter/CYE163/assets/57239953/73479f70-94f3-4ffd-b621-e38ac2bbb8d0)

# Bandit 4

The goal for this level is the get the password stored in the only human-readable file in the inhere directory.

![Screenshot 2024-02-12 091815](https://github.com/th3j35ter/CYE163/assets/57239953/4dca205e-b4a3-4423-ab1f-b1e0cfb3439c)

In order to find the filetype I figured the readable file would be text, so I dug into the find command link provided by overthewire and found this.

![Screenshot 2024-02-12 092248](https://github.com/th3j35ter/CYE163/assets/57239953/ef353535-3292-4171-b86d-50c862601e0f)


![Screenshot 2024-02-12 093402](https://github.com/th3j35ter/CYE163/assets/57239953/66190071-029b-43d0-b184-eaed8661ac7b)

Using these commands I ran this command:

find . -type f -exec file {} \;

![Screenshot 2024-02-12 093504](https://github.com/th3j35ter/CYE163/assets/57239953/554ca02e-e75d-45d4-9ae2-f5226ad337ed)

After identifying the human-readable file I was able to get the password and move on to the next level.
<details>
  <summary>The password is:</summary>
  lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
</details>

# Bandit 5

![Screenshot 2024-02-12 093817](https://github.com/th3j35ter/CYE163/assets/57239953/6b1bc658-0dc2-4434-83c1-1b85bb9ce7d3)

The objective for this level is to identify the file in the directory <b>inhere that has 3 properties:

-Human-Readable

-1033 bytes in size

-not executable

Since this included the parameter for the file to be human-readable which was the only requirement from the last level I figured my attempts could be structured around this.

Because of this I started with the same command as before:

<B>find . -type f -exec file {} \;<B>

However, since I need to test for the size of the file and require it to not be an executable I need to expand it from where it is now.

Using the provided links by overthewire I identified several additional parameters to add.

![Screenshot 2024-02-12 094943](https://github.com/th3j35ter/CYE163/assets/57239953/66aa651a-6499-41a7-948f-a1fc11f7d7a3)

Since I am not looking for executables i can replace it with <b>! -executable<b>.

Additionally I need to check the size so it is 1033 bytes. This requires that I append 'c' to my size parameter.

![Screenshot 2024-02-12 095229](https://github.com/th3j35ter/CYE163/assets/57239953/33a6d3bd-5ed0-4b35-852f-ff95f411748d)

With this in mind I was able to run the command:

find . -type f -size 1033c ! -executable -exec file {} \;

![Screenshot 2024-02-12 095444](https://github.com/th3j35ter/CYE163/assets/57239953/b3bc208b-2c72-4538-b620-788c56bf6855)


<details>
  <summary>The password is:</summary>
  P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
</details>

# Bandit 6

After exiting the server I logged into Bandit6.

![Screenshot 2024-02-12 095658](https://github.com/th3j35ter/CYE163/assets/57239953/8bac1fef-b776-4799-80f6-4df2dada3d25)

The objective for this level was to access a file somewhere on the server that was owned by user bandit7, owned by group bandit6, and was 33 bytes in size.

This means I need to search for the following:
- Username: bandit7
- Groupname: bandit6
- File size: 33 bytes

Utilizing the find command seems the most appropriate with the added parameters.

find / -user bandit7 -group bandit6 -size 33c

The user and group names come first to identify the owned properties before the size. However, when running this it results in a long list of permission denied messages. Assuming that this is an error message you can utilize 2>/dev/null to redirect the messages that aren't positive results to an output that isn't your screen.

Therefore, the correct command is:

find / -user bandit7 -group bandit6 -size 33c 2>/dev/null

![Screenshot 2024-02-12 100949](https://github.com/th3j35ter/CYE163/assets/57239953/ec6fc759-b189-45f3-b005-f1f0766f5b5b)

After extracting the password from the indicated filepath, the level is complete.

<details>
  <summary>The password is:</summary>
  z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
</details>

# Bandit 7

After exiting Bandit6 I entered into Bandit7 successfully.

The objective for this level was to use a password stored in the file 'data.txt' which was right next to the word <b>millionth

In order to do this I needed to use a command that identified patterns and printed them. Using the provided links by overthewire I found that 'grep' was suited for this usecase. 

![Screenshot 2024-02-12 104243](https://github.com/th3j35ter/CYE163/assets/57239953/be7b06e9-2e21-4f89-8866-11131ee804a6)

Since I'm looking for the word 'millionth' I can format the command this way:

grep 'millionth' data.txt

This results in the password being printed out alongside the pattern I searched up.
<details>
  <summary>
    The password is:
  </summary>
  TESKZC0XvTetK0S9xNwm25STk5iWrBvP
</details>

# Bandit 8

After exiting Bandit7 I entered in the retrieved password and logged into Bandit8.

The stated goal of this level is to use the only line of text in data.txt that occurs once as the password.

Since this is a file with multiple lines, the sort command is necessary to parse through each one. However, since the required password is the only line that is unique another command 'uniq' must be used to filter out any non-unique lines.

The command to find the password is:

sort data.txt | uniq -u

<details>
  <summary>
    The password is:
  </summary>
  EN632PlfYiZbn3PhVK3XOGSlNInNE00t
</details>

# Bandit 9

I logged into Bandit9 with the password obtained from Bandit8.

This objective is to retrive the password from data.txt where it is one of the few human-readable strings, preceded by several '=' characters.

Because the instructions indicate that the password is a string it is acknowledged that the 'strings' command will be used. Additionally, since it is preceded by '=' characters they can be used as patterns so 'grep' can also be used in conjunction.

Formatting the command like this will search for strings with the pattern of '=' in them:

strings data.txt | grep '==='

The output was slightly offskew but contained the necessary information to identify the password.

![Screenshot 2024-02-12 105815](https://github.com/th3j35ter/CYE163/assets/57239953/b6a3d872-917a-493f-a193-08d2f97eb7f8)

<details>
  <summary>
    The password is:
  </summary>
  G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
</details>

# Bandit 10

Using the password obtained from Bandit9 I was able to login to Bandit10.

![Screenshot 2024-02-12 110111](https://github.com/th3j35ter/CYE163/assets/57239953/a79f6c88-c822-4951-826c-5b99fac21d31)

The objective of this level is to obtain the password stored in data.txt, which contains base64 encoded data.

Since the data in the file is encoded, the command base64 is needed to append the decode option in order to read the data.

![Screenshot 2024-02-12 110407](https://github.com/th3j35ter/CYE163/assets/57239953/44584d88-d44e-4469-a538-e9a257321a30)

<details>
  <summary>The password is:</summary>
  6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
</details>
With the password obtained I am able to complete the level and move on to level 11 of the Bandit wargames.
