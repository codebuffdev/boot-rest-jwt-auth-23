# boot-rest-jwt-auth-23
Boot rest api with jwt authentication 

# JWT `Json Web Token`

Security
1. Authentication - Who u are?
2. Authorization - What do u want?

JWT is in the format of x.y.z . 

x = Header 
   - Consists of two parts:
      - The signing algorithm that's being used.
      - The type of token, which, in this case, is mostly "JWT".

y = Payload - The payload contains the claims or the JSON object.

z = Signature - A string that is generated via a cryptographic algorithm that can be used to verify the integrity of the JSON payload.

Token Example - 
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c

Let's break down each part of this token:

1. The header: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9 . This is a JSON object that describes the cryptographic algorithm used to sign the token (in this case, HMAC SHA-256) and the type of token (JWT).

2. The payload: eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ . This is also a JSON object that contains the claims or information about the user, such as the user ID (sub), name (name), and creation time (iat).

3. The signature: SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c . This is a string that is created by hashing the header and payload together with a secret key. The signature is used to verify the authenticity of the token and ensure that it has not been tampered with.

Together, these three parts make up a JWT token, which can be used to securely transmit information between parties. 
