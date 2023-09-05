![obraz](https://github.com/Anogota/Secret/assets/143951834/0359902e-6a0d-40cb-8193-de4b4a4e8b25)1. Which software is listening on port 80?

![obraz](https://github.com/Anogota/Secret/assets/143951834/44c39bec-b4ba-4000-80d7-7e50927fc14f)

I check the nmap, there we can find on port 80 nginx 1.18.0 :P i hope we can do something with it.

2. Which software is listening on port 3000? (Do not include the "." in the name.)
Still we can use as nmap scan, we can see there Node.js but the want answer without . it is just nodejs

3. The source code for the site includes which folder that is ascosiated with repositories?
First what we need to do is download Source code from website

![obraz](https://github.com/Anogota/Secret/assets/143951834/e0b71eae-ffe5-42d1-a300-933a55a63780)

then we must unzip this file: unzip files.zip, after this we got a direcory local-web, go this this directory and write here ls -al and we can see this:

![obraz](https://github.com/Anogota/Secret/assets/143951834/896160ba-417e-4a07-8cdf-7404e3bc103f)

and the answer for this question is .git

4.When we are dealing with local repositories, which git command can we use to view older commits? (Don't include git in your answer).
I don't know this answer, but when you do know something use -h, always help, and here is the answer 

![obraz](https://github.com/Anogota/Secret/assets/143951834/e2bdf342-16c2-4401-9060-a2b9ac9176d1)

5.Which git commit updates the source to remove a sensitive information?
First what we need to do is navigate to local-web, than write in terminal git log, check everything and what's look intresting on this screanshoot, i think removed .env for security reasons and this is a answer for this question: 67d8da7a0e53d8fadeb6b36396d86cdcd4f6ec78

![obraz](https://github.com/Anogota/Secret/assets/143951834/a01cfc8c-0d70-4b4e-82e1-394b507f1f89)

6.What is the variable that used to hold this secret?
This is pretty simple to see, first we need thisn long number from previous task and copy, after this we need write in terminal git show 67d8da7a0e53d8fadeb6b36396d86cdcd4f6ec78 this shows as a variable.

![obraz](https://github.com/Anogota/Secret/assets/143951834/030530cc-be29-4905-b920-04f0c33fd20b)

7.Which endpoint is vulnerable to command injection?
first what we need to do is write in terminal git show, this shows as a code, from this code we will find endpoit vulnerable, after the short analiz i know, this a /logs

![obraz](https://github.com/Anogota/Secret/assets/143951834/117eef13-2400-4e97-b53e-c877e015e923)

8. Which user must a JWT token show in order to use /logs?
Still we need to look a code and then we see this user. This is a pretty simple code, u can understand this code without background programing, focus on it and u will understand i hope :P lol

![obraz](https://github.com/Anogota/Secret/assets/143951834/66f544e2-07c0-4e5b-9e15-87f91af05ff1)

9.Submit the flag located in the dasith user's home directory.
Here will be many steps focus, first what we need to acces the /logs, after search i saw when i try go to the page /logs i got error, but there another way to go /logs, u need go to /api/logs and we can see there ![obraz](https://github.com/Anogota/Secret/assets/143951834/e1431f75-8d1c-4494-bcd9-1aefb7b0f945)
I found awesome tool, to create a JWT token jwi.io
Here how it must look, to create this JWT token, to access this page.

![obraz](https://github.com/Anogota/Secret/assets/143951834/ae222201-fe93-4c3d-a28b-34f48de40db6)

there is also secret key, u need insert this key from task 6, and also username from task 8, here u need collect in one, everything what's you have.
And then go to burp, intercept the trafic, write auth-token: <here ur token> here is example how it must look.

![obraz](https://github.com/Anogota/Secret/assets/143951834/4084cf5d-8780-4793-86eb-cc022d8f3628)

And if u do this, we see request.

![obraz](https://github.com/Anogota/Secret/assets/143951834/51bcae63-1d6a-4af9-ad03-70985b3322c0)

And we see cmd? What we can do with it, if u have more experience we can think about command injection, but if you don't have first what you need to do is, USE GOOGLE!

![obraz](https://github.com/Anogota/Secret/assets/143951834/b08cfba7-780a-45e8-a38f-236caa2d25e6)

I aprroved there is a command injection, we can inject some reverse shell, let's go and take a user flag :P and rember to setup a nc 
And finnaly we got this.

![obraz](https://github.com/Anogota/Secret/assets/143951834/2a69fe5e-7c6e-4f82-a4f9-be59dbf2a918)

rember to setup better shell by this command: python3 -c 'import pty; pty.spawn("/bin/bash")'
and here is the flag

![obraz](https://github.com/Anogota/Secret/assets/143951834/8493ebc8-fd02-4263-a2b8-8dc3a99b8a73)
