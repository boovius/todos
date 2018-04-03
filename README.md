CURRENT WORK
=============

# API LOGGING

problem: we are not getting account info into logging - instrumentation middleware

posits:

 - account is not set in middleware chain at all
 - account not set in middleware chain where we think it should be

solutions:

 1. pull account information out when we auth the token now and add account to request object
 1. use code from auth and factor out into another custom middleware or update instrumentation middleware


investigation steps:

 1. are we setting the account somewhare in the middleware chain at all?
 1. can we set it by making use of auth functionality (from auth token)

