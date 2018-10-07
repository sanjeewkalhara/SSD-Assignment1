# -SynchronizerTokens-php
 Cross-Site Request Forgery (CSRF) is a type of attack that occurs when a malicious web site, email, blog, instant message, or program causes a user’s web browser to perform an unwanted action on a trusted site for which the user is currently authenticated. The impact of a successful CSRF attack is limited to the capabilities exposed by the vulnerable application. For example, this attack could result in a transfer of funds, changing a password, or purchasing an item in the user's context. In effect, CSRF attacks are used by an attacker to make a target system perform a function via the target's browser without knowledge of the target user, at least until the unauthorized transaction has been committed.
 
Implement a web application that matches following criteria.
● User login. You may use hard coded user credentials for demonstration purpose.
● Upon login, generate session identifier and set as a cookie in the browser.
● At the same time, generate the CSRF token and store it in the server side. You may store it in-memory. The CSRF token is mapped to the session identifier.
● In the website, implement an endpoint that accepts HTTP POST requests and respond with the CSRF token. The endpoint receives the session cookie and based on the session identifier, return the CSRF token value.
● Implement a webpage that has a HTML form. The method should be POST and action should be another URL in the website. When this page loads, execute an Ajax call via a javascript, which invokes the endpoint for obtaining the CSRF token created for the session.
● Once the page is loaded, modify the HTML form’s document object model (DOM) and add a new hidden field that has the value of the received CSRF token.
● Once the HTML form is submitted to the action, in the server side, extract the received CSRF token value and check if it is the correct token issued for the particular session. You this, you need to obtain the session cookie and get the corresponding CSRF token for the session and compare that with the received token value.
● If the received CSRF token is valid, show success message. If not show error message.
