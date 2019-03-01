1. What is the purpose of using _sessions_?
-We use sessions to allow the user to stay logged in without having to re-log in every time they visit the site by having authentication information stored on the server and each device will have a unique session. Cookies are also used to transmit that information between the client and server.

2. What does bcrypt do to help us store password in a secure manner.
-bcrypt allows us to hash passwords so if someone were to hack our database and look into our saved info, the woud not be able to see the password details as it would be encrypted. bcrypt also has its own method for checking if two hashed passwords are equal to see if the user logged in with the right password.

3. What does bcrypt do to slow down attackers?
-bcrypt hashes a password multiple times (known as rounds) to slow down attackers as they would need to have the hash, know the algorithm used, and how many rounds were used to generate the hash in the first place. We can never fully protect our information but our best defense is to slow them down so much that it would be almost impossible to decode sensitive information.
4. What are the three parts of the JSON Web Token?
-A JSON Web Token is composed of a header, a payload and a signature.The header contains the algorthm that was used to create the hash and the token type. The payload stores the users info like name the date they created the token and also conains a token id. To create a signature, we must create a string by base64 encoding the header and payload together, and then signing it with a secret.
