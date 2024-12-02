JWT and JWKS Server
This Node.js application serves as a JSON Web Token (JWT) and JSON Web Key Set (JWKS) server. It provides public keys with unique key identifiers (kid) for verifying JWTs, supports key expiration for enhanced security, and includes an authentication endpoint to issue JWTs.

Table of Contents
Introduction
System Requirements
Setup and Installation
Server Configuration
Running the Application
API Endpoints
/jwks
/auth
Testing
Contributing
License
Introduction
The JWT and JWKS Server simplifies JWT management by serving public keys in a JWKS format and issuing signed JWTs. It ensures better security with key expiration and robust configuration options.

System Requirements
Ensure you have the following installed:

Node.js: Version 14 or later
npm: Node Package Manager (bundled with Node.js)
Setup and Installation
Clone the Repository:

bash
Copy code
git clone https://github.com/Hasti0013/JWKS-Bulking-up-Project3
Navigate to the Project Directory:

bash
Copy code
cd jwt-jwks-server
Install Dependencies:

bash
Copy code
npm install
Server Configuration
The server is preconfigured to generate an RSA key pair for demonstration purposes. For production, replace this with a more secure and scalable key management solution. Configuration settings can be modified in the server.js file.

Running the Application
To launch the server, use:

bash
Copy code
npm start
By default, the server runs on port 8080. You can adjust this setting in the server.js file.

API Endpoints
/jwks Endpoint
Serves public keys in JWKS format.
Only returns non-expired keys for validation purposes.
/auth Endpoint
Issues signed JWTs via POST requests.
Accepts an expired query parameter to issue JWTs signed with expired keys for testing scenarios.
Testing
Run the test suite using the following command:

bash
Copy code
npm test
The testing setup uses Mocha and Chai for basic functionality checks. Enhance the test coverage for broader use cases and edge scenarios as needed.

Contributing
We welcome contributions! Report issues or submit pull requests to suggest improvements or fix bugs. Let’s collaborate to make this project even better.

License
This project is licensed under the MIT License. See the LICENSE file for further details.
