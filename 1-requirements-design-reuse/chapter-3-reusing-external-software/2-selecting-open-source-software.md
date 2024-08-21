# Chapter 3: Reusing External Software

## Selecting (Evaluating) Open Source Software
### - Open Source Security Foundation (OpenSSF) has developed a [Concise Guide for Evaluating Open Source Software](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Concise-Guide-for-Evaluating-Open-Source-Software.md#readme)
- can you avoid adding it?
- is it the correct version? ('typosquatting')
- is it maintained?
- is there evidence the developers work to make it secure?
- easy to use securely?
- instructions on how to report vulnerabilities?
- significant use?
- software's license? ([OSI](https://opensource.org/licenses)) - likely to follow other good practices
- test its addition, preferably in an isolated env
- results of code evaluation?

### Software Bill of Materials (SBOM)
- nested inventory identifying components making up a larger piece of software
- check if available, often easier to use that data to help answer above questions
- good to provide a SBOM to potential users of your software for same reasons
- [Software Package Data Exchange (SPDX)](https://spdx.dev/)
- [NIST Software ID (SWID)](https://csrc.nist.gov/Projects/Software-Identification-SWID/)
- [CycloneDX](https://github.com/CycloneDX/specification)

### Other Sources
- [The Tidelift guide to choosing packages well (February 2021)](https://tidelift.com/subscription/choosing-open-source-packages-well), Tidelift
- [How to Evaluate Open Source Software / Free Software (OSS/FS) Programs](https://dwheeler.com/oss_fs_eval.html)
- [deps.dev - open source insights / understand your dependencies search](https://deps.dev/)
- [OpenHub](https://openhub.net/)
- [Libraries.io - search open source packages, frameworks, libraries](https://libraries.io/)
- [OpenSSF Resources and Guides](https://openssf.org/resources/guides/)

> On 2019-12-01 German software developer Lukas Martini discovered that two Python libraries in the popular PyPI (Python Package Index) repository implemented typosquatting attacks. These malicious packages would steal SSH and GPG private keys from developers who used them. The malicious package jeIlyfish imitated the non-malicious jellyfish package and did the damage (note that in the malicious package's name the third character is an uppercase "I", not a lowercase "l"). The same attacker also uploaded a malicious package named python3-dateutil which imitated the popular dateutil library for Python3. The malicious package python3-dateutil didn't include any malicious code itself, but instead loaded the malicious package jeIlyfish as a dependency. 