# Chapter 1. Security Basics

## What is Privacy and Why it is Important
>'[Privacy is] the right to be let alone, or freedom from interference or intrusion' ...
>'Information privacy is the right to have some control over how your personal information is collected and used...' -- International Association of Privacy Professionals (IAPP)


## Privacy Requirements
- simplest: don't collect personal information (PI)
- eliminating is the best from a privacy point of view
- minimize collected PI
- if you must collect PI, provide a variety of protections
- laws and regulations may apply

### Privacy Laws and Regulations
- differ within countries, provinces / states
#### United States Examples
- Family Educational Rights and Privacy Act (FERPA) for student records
- Health Insurance Portability and Accountability Act (HIPAA) for health related data
- Children's Online Privacy Protection Act (COPPA) for data related to children
- Fair and Accurate Credit Transactions Act (FACTA) for some financial data
- US Privacy Act for US Federal Agencies maintaining records about citizens and residents
- Individual states may have additional laws

#### European Union: General Data Protection and Regulation
- protects personal data of subjects who are in the EU, regardless of citizenship
> 'any information relating to an identified or identifiable natural person (‘data subject’); an identifiable natural person is one who can be identified, directly or indirectly, in particular by reference to an identifier such as a name, an identification number, location data, an online identifier or to one or more factors specific to the physical, physiological, genetic, mental, economic, cultural or social identity of that natural person'
- does not matter where the data processing takes place
- includes data connected to data that identifies an individual
- more sensitive data includes racial or ethnic origin, political opinions, religious or philisophical beliefs, trade union membership, genetic data, biometric data, health data, and data concerning sexual orientation / lifestyle
- 'processed' refers to any time an operation is performed on data including collecting, storing, viewing, transmitting, and deleting whether automated or not
- a 'controller' is the person / organization who determines purpose and means of processing
- a 'processor' is a thrid party that processes data on controller's behalf

##### 7 Primary Principles for Processing Personal Data
1. Lawfulness, fairness, and transparency - process data within the law, fairly, and transparently to the data subject
2. Purpose limitation - only process personal data for the purpose in which it was collected
3. Data minimization
4. Accuracy - keep data up to date and take reasonable steps to erase or update inacurrate data
5. Storage limitation - store in form that permits identification no longer than needed and only for purposes it was collected
6. Integrity and confidentiality
7. Accountability - controller is responsibile for these principles and demonstrating compliance

##### 6 Rights fpr EU residents
1. Right of Access - can ask whether personal data is processed, and can receive access (copy / screenshot) to it and information regarding processing
2. Right of Rectification - can have inaccurate data corrected
3. Right of Erasure (ie: Right to be Forgotten) - can have data erased in some circumstances
4. Right to Restriction of Processing - in certain circumstances can restrict processing, while still being stored
5. Right to Data Portability - in certain circumstances, subjects may have their data exported
6. Right to Object - in certain cicumstances, may object to having personal data processed

##### Criteria for Processing Data
- must meet one of the following criteria:
1. Compliance with law - necessary to meet a legal obligation
2. Performing a contract with the data subject
3. Legitimate business interests - unless overridden by data subject
4. Consent from data subject (specific, informed, clear affirmative action, and freely revocable)


##### Profiling
- under GDPR, any form of automated processing that involves personal data to evaluate aspects of that person
- usually requires explicit consent

### Privacy Requirements: Telemetry
- data about how the software is used or performing
- fraught with privacy and confidentiality issues
- opt-in agreement may not be adequate
- end users should be given full awareness of what data may be sent, to which parties, and the ability to control the transfer of that data
- Linux Foundation's [Telemetry Data Collection and Usage](https://www.linuxfoundation.org/telemetry-data-policy/)