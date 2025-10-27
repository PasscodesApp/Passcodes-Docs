# Security Concerns

This file highlight some of major security complications that may or may not happen in future, with the idea of have custom backend for passcodes app.
Due to this security releated problems, The custom backend feature will be hard to implement. But, still we will try our best to implement it. 

I am current (As in  29 Oct, 2025), have not a very good understanding of this security issue that may occur.. Therefore, As a effective decision in favor to security.
We have decide, that the custom backend feature will be implement in phrases or so, to speak in a series of steps.. 
Currently, We are suspending any sort of offical development for this "custom backend thing". 
We will come with a plan and will make a sort of decision, about how and when to continue further develeopment specfic to this "custom backend" thing.

> We here, by the word "SUSPENDING DEVELOPMENT" means that any updates in code, 
>will not be posted to passcodes app repository that can make api call to such a custom backend. other development in organization and in app repo is continue as same. 
>Also the docs will also be updated, even the docs that relates to custom backend..

Still if you wish you are free to develop your own api.. based on given specs for custom backend. but keep in mind that our app (as of now will not support custom backend in production).

Also, I am looking forward to hear from community & even researching myself about how to mitigate this sort of risks. 
for this, you talk to me directly on telegram or (It would more good if you can message in our [telegram community](https://t.me/passcodescommunity)).


## Why this sudden change?

When I first got the idea of this custom backend thing, I was like.. Yup it will be easy. before 6 months, it feels like a easy thing to me, 
because I was dumb enough to think that, I am make just a website (or rather app in our case) that present that data given by api and send data to api..
It me thinking like web developer. but I forget that I am not make a instgram clone or some sort of social media app, that I can follow & replicate step, that a typical youtube toutrail can provide.

I forget that we are build a very data heavy app & one that my defination "concerns with user's security". 
Overtime, may concepts / problems like database design, api design & version compatablity has made me relaizied,
that there is much more to software enginnerring then all youtube vidoe combine can ever teach. 

It not that, this type of secuirty concerns never arised utill now, in my mind or any of other collobrator's mind.
but as we (especially me) are mostly universtiy students & have little less exprience in security and in software engineering.
We always take https as secure. and think that https and ssl certificates can handle encryption for data packets 
and i don't need to worry about sending secrects like passwords, keys or jwt-tokens because it gets encrypted.

Especially my the converstaion that I had recently with my friend [@razorblade23](https://github.com/razorblade23) made me realizied that I was wrong, 
in taking bitwarden custom backend feature as easy peasy thing that I can too implement.. 
He made me realizied that there much more to web & api security then just https...

