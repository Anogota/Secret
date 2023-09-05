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
