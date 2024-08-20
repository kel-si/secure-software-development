# Chapter 2: Secure Design Principles

## Warning Signs
#### 1. HTML or other data format sent to client performing security-related input validation
#### 2. JavaScript or other code sent to the client performing security checks
#### 3. Mobile app that does security-relevant input validation
#### 4. Database directly accessible via the network for use by a client application (ex: web browser) - must ensure all operations a user is allowed to perform are authorized
- often better to use a program to mediate access
#### 5. Network communication channel that an attacker can hijack
- use TLS (ex: https:) / SSH to resist hijacking


