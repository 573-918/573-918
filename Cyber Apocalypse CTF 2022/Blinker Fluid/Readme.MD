Blinker Fluid

I first started the docker container;

<img src= "./blinker fluid start.png">

Once started I then copied the address in to the web browsers address bar;

<img src= "./blinker fluid home.png">

I then saw the homepage was hosting an invoice completeing software;

<img src= "./blinker fluid invoice.png">

I then started to dig around and see what interesting things i could find;

<img src= "./blinker fluid new invoice.png">

I saw the page would complete the invoice no matter how i edited the text given to us;

Even if i deleted all the data the invoice would compile;

I injected various xss payloads but then realised this was being unsuccessful with any of these kinds of attacks;

On the app there was not a bot or admin for blind xss;

There wasnt any cookies or sessions being created so nothing to capture information wise here;

So I went back to the start and saw that we had downloadable content for this challenge;

I proceeded to download the files and inspect them;

<img src= "./blinkers index backend.png">

Upon doing so i saw we had a set of dependencies/libraries/included software;

<img src= "./blinkers package.json backend.png">

I searched for these and if they are all up-to-date;

I found that MD-TO-PDF was vulnerable;

I could see there is a github for this issue;

I started to read this and found an example of the code that would exploit this application in the desired way;

https://github.com/simonhaenisch/md-to-pdf/issues/99

I would get Remote Code Execution!!!;
While reading the example I saw that I would have to manipulate the code to do what I wanted;
I also saw another example of the code i could utilise for my payload;

<img src= "./github code.png">

I now had a new problem as i would be creating my own payload and have to get it to exploit the target; 
Finding the cve details and reading them are one thing but to understand it and be able to 
emulate the attack on to a different server can sometimes more difficult than it seems;
When I did fially get to the understanding of why i could run an exploit like this on this software I was ok;
I combined the two payloads pictured above and came up with the one pictured below;
I had numerous issues when trying to get the payload to run;

<img src= "./blinker fluid new invoice with payload.png">

The white space at the start seemed to be sanitized for code after new line or multiple but if you did not leave a white space Then

<img src= "./blinker fluid flag.png">
