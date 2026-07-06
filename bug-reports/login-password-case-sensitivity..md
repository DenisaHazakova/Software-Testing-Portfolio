| Field              | Description                                                                                                                                                          |
| :----------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Title              | Login - password is not case-sensitive.                                                                                                                              |
| Priority           | High                                                                                                                                                                 |
| Environment        | Chrome 148.0.7778.168, macOS 12                                                                                                                                      |
| Actual Result      | Login successful with a lowercase password                                                                                                                           |
| Expected Result    | Login not successful because it is required that password is case sensitive                                                                                          |
| Attachment         | ![Screenshot of login bug with password](/images/login-password-case-insensitive.png)                                                                                |
| Status             | New                                                                                                                                                                  |
| Steps to reproduce | 1. open a link https://practicelogin.netlify.app/ <br> 2. fill in email: tester@nezam.com <br> 3. fill in password: tester@123 <br> 4. click on the button "Sign in" |
