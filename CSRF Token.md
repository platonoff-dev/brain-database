#Web #ClientServer #Security
This token is necessary for identify that request has came from yours site.
This token:
- Must be unique for each operation
- Must be disposable (work only 1 time)
- Must has limited lifetime
- Must be generated with cryptographically strong pseudo-random number generator

Before all unsafe methods (POST, PUT, PATH, DELETE) we need to check this token

This method for secure from CSRF-attack is very simple and uses on many servers.

+Simple
-Need to store token on backend

1.  When session starts server generate token
2.  Token saves in server database
3.  In response that initialize session server returns token. It may be in HTML or in `X-CSRF-Token`
4.  With all future requests server must sent token too.
5.  If request method is unsafe server must check that CSRF token is valid.
6.  If token is valid, all is OK :) else You need to log event and don't do nothing more