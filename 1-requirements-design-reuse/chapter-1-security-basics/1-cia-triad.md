# Chapter 1. Security Basics

## CIA Triad
1. Confidentiality
- access only by authorized users

2. Integrity
- no unauthorized modification (additions, changes, and deletions)

3. Availability
- information is available when needed

### Supporting Mechanisms
- non-repudiation / accountability (an action cannot be denied)
- identification & authentication
- authorization (what actions an authorized user may do)
- auditing / logging (record keeping)


## Security Requirements
- anything required by law or regulation
- anything important to (potential) customers / users
- good idea to record high-level security requirements in one place
- others may be tracked on an issue / bug tracker or not tracked at all

## Common Security Objectives
- think about specific requirements for each category of CIA triad
- think about how each one applied to the kind of info your program will manage

### Confidentiality
- identify information that should not be publicly revealed
- who should have access to info about people and systems
- what info can be limited (cannot leak / reveal what you don't have)
- how will info be stored

### Integrity
- identify info that some people may modify

### Availability
- what is the impact if system / info is unavailable (severity)
- DDos is always a risk if system accessible via internet
- focus on bigger-risk items
- develop software that is not easy to overwhelm or take down with simple inputs
- make it possible to scale up by rapidy adding new servers
- make it easy to quickly recover when attack ends
- data should be easily backed up
- plan for backups
- data backed up to 'cold storage'
- limitations

### Non-repudiation
- may not be critical, but sometimes is

### Identify & authentication (I&A)
- how users will prove who they are
- prevent spoofing of legitimate users
- support 2FA

### Authorization
- who's allowed to do what
- think about people's roles in addition to thinking about info to protect

### Auditing / Logging
- at least record login / logout and important events like user creation / deletion
- typically records when something happened, what happened, what system component did it, and who took the action

### Tips for Finding Security Requirements
- 'subject' refers to something taking an action (ex: user, process)
- 'object' refers to what is being acted on (ex: file, network port)
- can create 'abuse cases' or 'misuse cases' (similar to regular use cases for features)
- define how the system counters such abuse / misuse
- think about what kind of attackers you expect (ex: attacker with limited resources and not highly targeted vs. nation-state threat actor with unlimited resources, etc.)
- [Common Criteria for Information Technology Security Evaluation](https://www.commoncriteriaportal.org/index.cfm)
- look at comparable software's security capabilities if possible



## The Need for Risk Management






