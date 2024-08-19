# Chapter 1. Security Basics

## Development Processes / Defense-In-Breadth: Individual Software Development & Deployment Processes
- defense-in-breath is considering security through all stages of development and deployment

### Development Processes
##### 1. Determine requirements
- what the software does
- what security requirements it needs to provide
- ex: data that should be kept confidential

##### 2. Determine architectural design
- how to divide problem into interacting components
- secure design principles (later in course)

##### 3. Select reusable components
- libraries, packages
- evaluate these components, including their dependencies

##### 4. Implement
- most vulnerabilities made during implementation are common
- learn and avoid

##### 5. Verify
- tests and analyzers

##### 6. Deploy
- help ensure users get correct version and can easily operate in a secure way

### Using These Processes Together
- do not need to execute these processes in a strict sequence (waterfall model) and can be a [mistake](https://dl.acm.org/doi/10.5555/41765.41801) to do so
- another common mistake is to implement components independently without integrating and testing together until everything is completed
- bounce between processes as new information is learned
***