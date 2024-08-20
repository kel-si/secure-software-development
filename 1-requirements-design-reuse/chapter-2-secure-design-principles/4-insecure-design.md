# Chapter 2: Secure Design Principles

> Insecure design is such a common mistake in web applications that it is 2021 OWASP Top 10 #4 (NEW)

## Insecure Design: Client-Side HTML Input Validation
- validations within html tags are trivial to bypass (ex: maxlength="100")
- never depend on a web browser to do any security-relevant checks

## Insecure Design: Client-Side JavaScript/WebAssembly Input Validation
- don't depend on frontend JS/WASM to do security checks
- any security checks sent to browser can be bypassed as web browsers are under someone else's control

## Secure Input Validation
- input validation on an environment you can trust (not the browser)
- security-related checks done in the server
- prevent direct database access if users do not need it

## Insecure Design: Mobile Application with Client-Side Checking
- cannot assume security checks done on mobile device will actually be made
- device / application could be modified
- also cannot trust the other applications

## Insecure Design: Client Application Depending on an Untrusted Server
- ex: writing a web browser, must trust the local operating system but cannot trust remote web servers

## Takeaway
- code you need to trust must run in an environment you trust
- fine to run checks on a system you don't fully trust to prevent unintentional mistakes
- security checks should be done, or redone, on a system you can fully trust
