The Loginza.API is a single authentication mechanism that uses various algorithms for authenticating users with a wide range of accounts such as OpenID, Google, Yandex and so on.

The Loginza.API is a program layer that converts different authentication mechanisms into a common mechanism. In other words, by using the Loginza.API, you won’t have to get to grips with the different authentication programming nuances of any of the account providers we support.

We have made the Loginza.API as simple, convenient and, most importantly, secure a method of logging in using OpenID and accounts from other providers as we possibly could. The authorization process always looks the same in terms of the website using the Loginza.API, it doesn’t matter which login method or account provider the end user chooses.

The process of logging in through the Loginza.API can be divided into the following stages:

0. The site requests the user to log in through the Loginza.Widget. The end user has a selection of login methods at their disposal.
0. The user then picks a provider with which they have an account, for example, Google, Yandex, Rambler, OpenID etc.
0. The Loginza.Widget processes the user’s request and redirects them to the relevant account provider, and processes the responses returned.
0. No matter whether of not the authentication was successful, the Loginza.Widget redirects the user back to the URL address of the website requesting authorization.
0. A token variable will be included in the POST request to the URL when the user is redirected. The variable token contains a unique identifier of the location of the result of the authorization on the Loginza server.
0. The site requesting authentication should receive a POST value for the token variable, and, using the Loginza.API, request the results of the user authentication by transfering the token value.
0. In response to this token verification request, the Loginza.API returns a response in the JSON format. The response will either contain user profile data or errors (if any occur during the process).
0. On the basis of the response received, the site requesting authorization stores the user profile data and considers the user to be authorized (begins a session) or generates an error message for the user.
