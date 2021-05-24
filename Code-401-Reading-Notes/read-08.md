# Access Control (ACL)

### When is Basic Authorization used vs. Bearer Authorization?

 The Basic authentication schemes are dedicated to the authentication using a username and a secret
Bearer depends on the encryption of the data (tokens) and it send it in the header


### What does the JSON Web Token package do?

It allow us to generate (Sing) tokens and define it's payload and secret, also allow us to verify the tokens of the user.

### What considerations should we make when creating and storing a SECRET?

* Use encryption to store secrets within .git repositories
* Use environment variables
* Use "Secrets as a service" solutions
  
* Never store unencrypted secrets in .git repositories
* Avoid git add * commands on git
* Add sensitive files in .gitignore
* Don’t rely on code reviews to discover secrets
* Use automated secrets scanning on repositories

### TERMS

1. encryption : is the process of converting data and information into a secret code to hide it's true meaning.

token :  is a single element of a programming language. There are five categories of tokens: 1) constants, 2) identifiers, 3) operators, 4) separators, and 5) reserved words

bearer : is an authentication type that holds a token with it and used after the sing in process.

secret : is a private data between your app/api and the authorization server that grant token only to the eligible users.

JSON Web Token : JWT is a package that allow us to define generate and verify tokens to the user.

## RBAC
 is the idea of assigning system access to users based on their role in an organization. It's important to remember that not every employee needs a starring role.

 Benefits of RBAC?
 it easy to implement, and will make the ongoing management of access rights much easier and more secure.

The data breach you prevent may be your own.

**Access control lists (ACL)**

An ACL is a means of defining access rights by a given user or user group, to a specific object, such as a document.  As a simple example, an ACL 
could be **used to allow users from one department to make changes to a document**, **while only allowing users from other departments to read the document.**

**Attribute-based access control (ABAC)**
sometimes known as policy-based access control, can use a variety of attributes, including user department, time of day, location of access, type of access required, etc. to determine whether a user’s access request should be granted.

**RBAC implementation** 

1. Inventory your systems
2. Analyze your workforce and create roles
3. Assign people to roles
4. Never make one-off changes
5. Audit
   



     
