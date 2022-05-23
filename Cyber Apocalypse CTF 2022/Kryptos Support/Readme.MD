I first proceeded to start the Docker for this challenge;

<img src= "./kryptos start.png">

I then visited the homepage of the web application;

<img src= "./kryptos homepage.png">

As you can see in the picture above we have an input field for text;

I also can see there is a "backend" link which is clickable;

I visit the page to see what it is and what it does;

<img src= "./kryptos login.png">

Here we have a field for credentials to be filled out for logging in;

I dont have anything to fill out here;

Also I am not allowed to brute force my way in :) ;

I head back to the previous page to see what this is actually doing;

My thinking was 'this challenge is supposed to be an easy one'; 

So i go back to the start of the application;

I see that the page sends the input field to somewhere that gets some action afterwards;

I poked around in various ways to no avail;

I then remembered BLIND-XSS;

This is an attack that can and will fire when triggered from the "BACKEND";

<img src= "./xsshunter payload page.png">

Here we have examples of different Blind-XSS payloads;

I then used the basic payload;

I thought to start here first as this would be the best method;

Starting basic and working my way throught the payload difficulties;

<img src= "./kryptos home and payload.png">

Not knowing when or if these will fire is half of the fun with BLIND-XSS;

This is the type of attack that is famed for a $10,000 bounty by Telsa;

<img src= "./xsshunter payload fire.png">

This was a Quick fire BLIND-XSS!!!;

<img src= "./xsshunter report.png">

I then reviewed the report given from the payload;

As you can see above I was given the seesion cookie from the user who triggered my payload;

I knew Exactly what to do from here but as always i had 'teething problems' injecting the cookie;

I realised I was over thinking this problem and kept the cookie in its complete copied state;

I also didnt name the cookie either and let the server do this for me;

As I worked my way through all of the possible ways to inject this cookie and get it to save;

<img src= "./kryptos adding cookie homepage.png">

As you can see i injected the cookie using the Cookie Editor Extension;

This was the simplest way I could get the cookie successfully saved;

<img src= "./kryptos injecting cookie.png">

I then clicked the save icon and could see it had saved but nothing changed on this page?!?!;

I clicked the 'BACKEND' link;

I was redirected to this page;

<img src= "./kryptos tickets.png">

I was getting more and more excited by now;

I've had 2 successful attacks work in sequence towards the FLAG!!

I knew I had to be halfway or closer by now;

I carried on poking around by clicking the "SETTINGS" link;

<img src= "./kryptos settings.png">

I could see I could change the password to the account I had access to!?!?;

I opened BURP SUITE to see what this page was actually doing;

<img src= "./starting burpsuite.png">

Where the request was going to and what type for request way being sent;

I could seethat for the Moderator my 'UID' was 100;

Sent this to the repeater tab and continued to play with this field;

I tried numerous 'UID' inputs but only got success with 100 and 1;

I changed the password for 'UID' 1;

From previous knowledge on Linux/Debain based systems this is the Admin 'UID';

<img src= "./intercepted code in burpsuite.png">

Once I had changed the password for Admin;

I was shown the message below and knew it had been successful;

<img src= "./kryptos change password.png">

I then logged out;

I also had to delete the injected cookie from before;

<img src= "./kryptos admin login.png">

As soon as I was Logged in as admin i was greeted with this page;

<img src= "./kryptos vault flag.png">

And there we have it!!

The flag is ready to be submitted!!

Well done if you are able to follow my walk through for this challenge;
