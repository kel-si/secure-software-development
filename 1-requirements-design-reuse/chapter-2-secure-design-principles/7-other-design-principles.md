# Chapter 2: Secure Design Principles

## Beware of Race Conditions
- 'race condition' happens when a system's correct behaviour depends on the sequence of events but there is no control over the sequence
- generally involve one or more processes or threads accessing shared resource
#### Time of Check / Time of Check of Use (TOCTOU)
- race condition very common
- situation changed between determining if request is authorized and acting on request
- allows a different action to be performed that was not authorized
- can often counter by use APIs that check authorization and perform action simultaneously
- for example, do not create a record and then reduce privileges; create a record with reduced privileges
- for Unix-like systems, do not call access() and then open(); use just open() as it includes a check for access
- somewhat common error on Unix-like systems is insecurely creating temporary files
- most languages have a routine / command to securely create temporary files


## Harden the System
- try to design system so a single defect is less likely to result in complete compromise
- Content Security Policy (CSP)
- Address Space Layout Randomization (ASLR)
- enable these or ensure users can enable them

## Keep Secrets Secret
- live secrets should not be in source code
- use iterated per-user salted hash algorithms (ex: bcrypt) to store passwords used for inbound authentication
- use https:// instead of http:// (encrypts data)
- avoid accepting and sending data (ex: private keys) as command line params wherever possible


## Trust Only Trustworthy Channels
- for example, https:// instead of http:// when contacting a server (enables checking if server has a valid cryptographic certificate and prevents snooping)


## Separate Data from Control
- separate passive data from programs that are executed
- another way to implement least privilege (don't give data thr right to run as a program)
- Content Security Policy (CSP) supported by modern web browsers
- CSP allows you to state that HTML being sent is only data and is not allowed to provide inline scripts or styles