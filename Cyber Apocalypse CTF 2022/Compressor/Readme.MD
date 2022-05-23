I began by starting the Docker instance 

<img src= "./compressor start.png">

I tried to connect to this challenge using a web browser;

This wasnt unsuccessful but returned errors;

The errors returned gave me an understanding of why this would not connect;

I knew now that I needed to connect using a different method;

I used my knowledge base;

I tried to use NetCat;

At first I was getting my syntax wrong;

I then started to look at examples of using NetCat to connect to various types of instances;

I then could see where I was going wrong;

I corrected my syntax;

Once I was connected to the instance;

I could see the challenge was giving me a set of different actions I was able to complete;

I poked around using the different actions available;

I could see that I had access to the CAT action;

I know this reads the contents of a file;

I also know that inside Linux File Systems we have a way of escaping such actions;

With this I know that I can use this action with an escape;

This enables us to access files that are not supposed to be accessed;

i.e. the files in the folder above the working directory

I knew this was what i needed to do to complete this challenge;

In the process of capturing this flag I tried alot of ways to escape the cat action;

The returning errors given always helped me on my way to capturing this flag;

You will see this in the image below;

<img src= "./compressor all.png">


