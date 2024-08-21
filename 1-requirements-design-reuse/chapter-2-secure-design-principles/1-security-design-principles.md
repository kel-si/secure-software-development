# Chapter 2: Secure Design Principles

## What Are Security Design Principles
- rules of thumb to help avoid bad design decisions
- an aid to thinking
- need to think about what components you can trust and to what extent
- 'trust boundary' is a boundary between components you trust and those you do not
- ex: mobile application that communicates with a server you control, you trust the server but do not trust communication path between server and device, nor other applications downloaded on device, nor the general internet

## Widely-Recommended Secure Design Principles

#### 1. Least privilege
- every user and program operates using the fewest privileges possible
#### 2. Complete mediation
- non-bypassability
- every access attempt is checked
#### 3. Economy of mechanism
- system as simple and small as possible
#### 4. Open design
- act as though mechanism is publicly known
- depend on passwords, private keys, etc. rather than ignorance
- if actually open, allows for extensive public scrutiny
#### 5. Fail-safe defaults
- default installation should be secure
- **allow lists over deny lists**
- ex: don't distrubute software with a blank password, require one is set when software is installed
#### 6. Separation of privilege
- access depends on more than one condition (ex: 2FA)
#### 7. Least common mechanism
- minimize shared mechanisms
- avoid sharing files, directories, OS kernel execution, or computers with something untrusted
#### 8. Psychological acceptability
- make it easy for users to use protection mechanisms correctly

