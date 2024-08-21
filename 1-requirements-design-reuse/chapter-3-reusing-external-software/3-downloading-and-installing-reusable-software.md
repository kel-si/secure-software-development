# Chapter 3: Reusing External Software

## Downloading and Installing Reusable Software
### 1. Make sure name is exactly correct
- 'typosquatting' where a domain name or package name is maliciously similar
- most malicious packages mimic existing packages
- check common misleading name changes (ex: _ vs -, O vs 0, l vs I, or other unicode characters such as Cyrillic or Greek letters)
- check popularity of package (download counts, # of widely-used packages depending on it)
- **ignore advertised domains from a search engine - attackers may pay to advertise**
- check package release date

### 2. Download and install in a trustworthy way
- download directly from main site or trusted redistribution site (ex: package manager's standard repository)
- https: (TLS) instead of http:
- consider downloading software and waiting a few days to install to verify nothing has changed if practical
- try to avoid using pipe-to-shell (curl ... | sh) to download and install software (cannot download and delay install and attackers can detect a pipe-to-shell request and subvert those users, lose some version control - installed program can report any number)
- pipe-to-shell in a contained environment (ex: VM with limited privileges) where produced executables are thrown away is much less risky
- where practical, try to verify package is digitally signed by creators / re-distributors (often difficult to ensure you have correct corresponding public keys)
- beware of depending on being able to download / install components at run-time from external locations (use a reliable service like CDN)

### 3.Ensure system is not vulnerable to 'dependency confusion'
- also known as 'substitution attack'
- when using more than one repo
- system depends on package P to be retrieved from a typically private repository but nothing *requires* package P to be retrieved from its expected repository
- attacker can create a (typically) public repo with the same name and fool system into using that malicious package instead
- many ways to fool system such as giving malicious package larger version number
- attackers began exploiting this vulnerability in 2021
- clearly declare where package must be retrieved from
- prioritize feeds so most trusted are consulted first (less-trusted should never override more-trusted)
- can enforce dependency pinning / version pinning (require certain known version be used through digital fingerprint)
- integrity verification to verify downloaded package is identical to first time it was downloaded

> Relying on plugins, libraries, or modules from untrusted sources, and relying on untrustworthy content delivery networks, is considered part of 2021 OWASP Top 10 #8 (A08:2021), Software and Data Integrity Failures.