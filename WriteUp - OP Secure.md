This challenge is about JavaScript obfuscation, where code is intentionally obscured to hide its functionality. 

It is a login page. When we try to log in with an incorrect username and password, it displays a pop-up alert that tells the user whether the credentials they inserted are correct or not.

We know that this kind of pop-up alert is generated by JavaScript code, so maybe we can analyze the JavaScript code of this webpage. Before that, we can try to inspect the "Log In" button. The button has an attribute that calls the `on-click()` function with the parameter `checkCreds()`. It indicates that the `checkCreds()` function is being called after we click the "Log In" button.

Now we can begin to analyze the JavaScript code in this webpage. There is a JavaScript file named `login.js`. This JavaScript code has been obfuscated.

Now we need to de-obfuscate this JavaScript code. There is a function named `decode()` and it being called a few times in the `checkCreds()` function. By looking at the variables in `checkCreds()` function, we can assumed that the `decode()` function is used to decode the username and password.

We can use this function to decode that credential.

We get the credentials along with the flag. We can try to insert the obtained username and password in the login page to proves our finding.


The obtained credentials is correct. Now we can submit the flag.

### Alternative Way

We already know that there is a function named `decode()` and it being called a few times in the `checkCreds()` function. By analyzing the JavaScript code, we also know that the variable ... and ... stored the value of username and password inserted by the user. It then being compared with the other value in the variable ... and ... . So we can assume that the value in variable ... and ... are the correct username and password. In simple terms, the credentials inserted by the user are being compared with the correct username and password in this JavaScript code.


