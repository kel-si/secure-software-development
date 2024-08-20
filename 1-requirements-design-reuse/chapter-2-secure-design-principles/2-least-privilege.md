# Chapter 2: Secure Design Principles

## Least Privilege
- limits potential damage and reduces complexity of security-related interactions
- extends to internals of a program
- can conflict with simple design


## Ways to Implement Least Privilege
#### 1. Don't give a program any special privileges where possible
- ex: Linux supports making programs inherit privileges from its owner (avoid if possible)
#### 2. Minimize special privileges a program gets, including what data is accessible
#### 3. Permanently remove privileges as soon as possible
- drop extra privileges as soon as no longer needed
#### 4. Minimize the time the privilege is active
#### 5. Break program into modules to separate privileges
- ideally privileges modules will not fully trust other parts (mutually suspicious design)
- separation mechanisms like containers, VMs, Linux seccomp, and other security wrappers
- often not foolproof but may reduce damage if succesfull attack
#### 6. Minimize attack surface
- 'attack surface' is set of operations a potential attacker can access
- ex: allowing public access to some method that is not necessary
#### 7. Validate input
- make sure attackers cannot bypass input validation (later in course)
- big issue
#### 8. Sanbox program
- run your program (or part) in an environment with intentionally-restricted capabilities
#### 9. Minimize privileges for files and other resources
- normally, you should not have files writable by everyone (even readable at times)
- on Android, a file writable by all could be changed by a different application

***

> Incorrect permissions are such a common cause of security vulnerabilities that it is 2021 CWE Top 25 #22 and 2019 CWE Top 25 #15. It is CWE-732 (Incorrect Permission Assignment for Critical Resource). Incorrect permissions are especially bad if the default permissions are insecure; that special case is CWE-276 (Incorrect Default Permissions).

## Examples of Least Privilege
- deny serving files that should not be served
- don't allow users to write configuration files by default
- limit who can write
- SQL GRANT statements so program doesn't have rights to change certain data