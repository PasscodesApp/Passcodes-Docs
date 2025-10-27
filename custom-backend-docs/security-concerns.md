# Security Concerns

This file highlight some of major security complications that may or may not happen in future, with the idea of have custom backend for passcodes app.
Due to this security releated problems, The custom backend feature will be hard to implement. But, still we will try our best to implement it. 

I am current (As in  29 Oct, 2025), have not a very good understanding of this security issue that may occur.. Therefore, As a effective decision in favor to security.
We have decide, that the custom backend feature will be implement in phrases or so, to speak in a series of steps.. 
Currently, We are suspending any sort of offical development for this "custom backend thing". 
We will come with a plan and will make a sort of decision, about how and when to continue further develeopment specfic to this "custom backend" thing.

> We here, by the word "SUSPENDING DEVELOPMENT" means that any updates in code, 
> will not be posted to passcodes app repository that can make api call to such a custom backend. other development in organization and in app repo is continue as same. 
> Also the docs will also be updated, even the docs that relates to custom backend..

Still if you wish you are free to develop your own api.. based on given specs for custom backend. but keep in mind that our app (as of now will not support custom backend in production).

Also, I am looking forward to hear from community & even researching myself about how to mitigate this sort of risks. 
for this, you talk to me directly on telegram or (It would more good if you can message in our [telegram community](https://t.me/passcodescommunity)).


## Why this sudden change?

When I first got the idea of this custom backend thing, I was like.. Yup it will be easy. before 6 months, it feels like a easy thing to me, 
because I was dumb enough to think that, I am make just a website (or rather app in our case) that present that data given by api and send data to api..
It me thinking like web developer. but I forget that I am not make a instgram clone or some sort of social media app, that I can follow & replicate step, that a typical youtube toutrail can provide.

I forget that we are build a very data heavy app & one that by defination "concerns with user's security". 
Overtime, many concepts / problems like database design, api design & version compatablity has made me relaizied,
that there is much more to software enginnerring then all youtube vidoe combine can ever teach. 

It not that, this type of secuirty concerns never arised utill now, in my mind or any of other collobrator's mind.
but as we (especially me) are mostly university students & have little to less exprience in security and in software engineering.
We always take https as secure. and think that https and ssl certificates can handle encryption for data packets.
and We don't need to worry about sending secrects like passwords, keys or jwt-tokens because it gets encrypted at end.

Especially my the converstaion that I had recently with my friend [@razorblade23](https://github.com/razorblade23) made me realizied that I was wrong, 
in taking bitwarden custom backend feature as easy peasy thing that I can too implement.. 
He made me realizied that there much more to web & api security then just https...


## Potentails Concerns For Security

1) **Plain Text Secrets**: We sending the secrets (user credentendial's) in plain text to api in its request's body. So, there is chance that the request can be intercepted by any person in middle. this is mainly venurable to man-in-middle-attact.

i.e, A user is in a coffee shop which has free wifi. user connect his phone and as he waits for his coffee, he think of checking his instagram.. user is bit hyped for security, so he login-logout each time when use instagram. user open instagram app, use passcodes autofill for credentails amd login. the passcodes app then to fullfill this autofill request, makes (`GET /passwords?domain=instagram`) request to get data from backend (one that run in his homelabs). user is unaware of a hacker sit in a neghibour table who can see all traffic on coffee shop network. the backed send data in plain text and hacker see it, and both user and hacker start using user instagram profile. but luckily the user has notification from insta, about that two login and he was saved by change password, but you might not. 

2) **Backend See Pure Data**: We are send pure&plain data to backend. So it can see the user credintails and likely storing them in some type of file. This means anyone who has a backend (access to underlying machine) can see users credentials.

i.e. A user has a guest (likely a evil kid) in his house who is bit mischivious, and see the users passwords, because (dumb-)backend was store it in a pure plain txt file & then that kid just see the password and change password on users website.

3) **Server Swapping**: It unlikely going to happen and is not a the reponsiblity of `passcodes`.. but there are arbitory chances that the backend running can be swapped.

i.e. A (non-tech) user has a laptop, where he run custom backend for passcodes at `https://localhost:8080`as shown in docs. so, that he store his passwords on laptop ssd, and not in phone internal storage. user thinks that his credintials is more safe in sdd then in phone internal storage. user like any other person start server use it then stop server. after some day user download a game or something. that also run the local server. on same url `https://localhost:8080`. initally every work well. because two server where never active at same time. one day user was playing that game so server of game running on `https://localhost:8080`. but suddenly user need to login somewhere, so user start the server. expecting that everything will go fine. but, as non tech user he don't know networking concepts. and server was up at `https://localhost:8081/` os assign the 8081 as 8080 was aquired. you may think that it not problem as the server running would never have api schema matching to password.. and the server would crash or throw `400 BAD REQUEST` when `GET /passwords` but problem is with `POST /password` because, that api (of gae server) could have logging implemented and suddenly user credentials are in crash logs of some random server. I hope that one how reading that logs is kind enough to contact user...


> I know that this illustion are bit dump and funny too. but i guess it represents the reality. Because, no one how has a business or concerns for security. will use passcodes app. they will probabaly use industry certificated app like bitwarden or nordpass or any other paid more secure password manager. which has **ZERO-KNOWLEDGE-ENCRYPTION** supports. this is more secure and realiable.

