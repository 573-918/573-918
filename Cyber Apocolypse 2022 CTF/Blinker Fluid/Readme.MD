Blinker Fluid

I first started the docker container;

<img src= "./blinker fluid start.png">

Once started I then copied the address in to the web browsers address bar;

<img src= "./blinker fluid start.png">

I then saw the homepage was hosting an invoice completeing software;

<img src= "./blinker fluid start.png">

I then started to dig around and see what interesting things i could find;

<img src= "./blinker fluid start.png">

I saw the page would complete the invoice no matter how i edited the text given to us;

<img src= "./blinker fluid start.png">

No matter if i deleted all the data the invoice would compile;

<img src= "./blinker fluid start.png">

I injected various xss payloads but then realised this was being sanitised fully for all of these kinds of attacks;

<img src= "./blinker fluid start.png">

So I went back to the start and saw that we had downloadable content for this challenge;

<img src= "./blinker fluid start.png">

I proceeded to download the files and inspect them;

<img src= "./blinker fluid start.png">

Upon doing so i saw we had a set of dependencies/libraries/included software;

<img src= "./blinker fluid start.png">

I searched for these and if they are all up-to-date;

<img src= "./blinker fluid start.png">

I found that MD-TO-PDF was vulnerable;

<img src= "./blinker fluid start.png">

I could see there is a github for this issue;

<img src= "./blinker fluid start.png">

I started to read this and found an example of the code that would exploit this application in the desired way;

<img src= "./blinker fluid start.png">

I would get Remote Code Execution!!!;

<img src= "./blinker fluid start.png">

While reading the example I saw that I would have to manipulate the code to do what I wanted;
