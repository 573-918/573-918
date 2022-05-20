Blinker Fluid

I first started the docker container;

<img src= "./blinker fluid start.png">

Once started I then copied the address in to the web browsers address bar;
I then saw the homepage was hosting an invoice completeing software;
I then started to dig around and see what interesting things i could find;
I saw the page would complete the invoice no matter how i edited the text given to us;
No matter if i deleted all the data the invoice would compile;
I injected various xss payloads but then realised this was being sanitised fully for all of these kinds of attacks;
So I went back to the start and saw that we had downloadable content for this challenge;
I proceeded to download the files and inspect them;
Upon doing so i saw we had a set of dependencies/libraries/included software;
I searched for these and if they are all up-to-date;
I found that MD-TO-PDF was vulnerable;
I could see there is a github for this issue;
I started to read this and found an example of the code that would exploit this application in the desired way;
I would get Remote Code Execution!!!;
While reading the example I saw that I would have to manipulate the code to do what I wanted;
