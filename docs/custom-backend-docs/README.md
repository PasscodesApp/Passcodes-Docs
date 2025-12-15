# Custom Backend Docs

> [!IMPORTANT]
> We don;t support custom backend offically, we will do that in far future (2026). 
>
> But this serve as a earlier docs, for understanding, how you can build custom backend for passcodes app.

**Inspiration**: the idea is greatly inspired from **Bitwarden**.

Here, you will find docs for how to build custom backend for passcodes app.
This docs will be a single source truth for communication between passcodes developers and custom backend developers.
There might be infomation availiabe here which is ahead of time. But we will ensure that it never go behind the time.

As we all know that make a backend for app is compilicated & need serious attention. And here it more complicated,
As we build app and you build backend end. if attention is not paid, there might compatablity issues.

Here, In this docs you will find infomation about all the things that passcodes app expect from your custom backend.

 - The Minimal API Interface (Protocol).
 - And Some Security Enforcement.

Yes, the api protocol will be define by passcodes app & we will also enforce some security best practices on your backend.
Apart from this there might other things also. This api interface will be minimal requirement that your backend need to fullfill,
to count as valid custom backend for passcodes. otherwise there might be compatablity issues.. 
ofcourse, you can extend the api interface but can't alter it.

Also have a look into database design docs to get more idea on topic for custom backend..

## Custom Backend Version System

Yes, for custom backend that wanna stay forward-backward compatible. This will really useful.

- The version system will start from `0 to N`.
- The version system will be a integer system. `v0, v1, v2, v3......`
- This version system will be complete seperate from app version system.
- The version system will expect in your api path. `https://custom.backend.com/v0/`
- And as always with passcodes, v0 will be reserve for initial testing & proof of concept & alpha stage. (like we do in passcodes app & database)

---

========== COMING SOON ==========

Further infomation about the api interface will be avaliable soon.

