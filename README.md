# Angular8-Typescript-Webpack-singup
# SignUp Form

Do npm install
To build the application use command npm run build  -- open with port 8888 with domain localhost -- localhost:8888
                                                       It helps in analysing the size of chunks and other permance measures
To identify size of each chunks use command npm run performance
													It will create stats.json file with indepth information for analysis

To start this application use command npm run start

Application is built using
Typedscript , Angular 8 , Webpack 4

> The application has 3 routes
   > login
   > register
   > home

> The API shared doesn't save the registered user and doesn't give the information of the same User registered newely
> To build the whole flow I have used FakeBackend provider that will save the registered user after sucessful 200 Reponse from API in local storage and then use the login screen to login

> TO build a secure connection JWT module is also created that extends HttpInterceptor to add a auth token to the Authorization header if the user is logged in.

Few handlers have been written in a common way so that each Http request can be handled in secure way in terms of Error scenrios, Autentication

Few componnets are also created such as Alert and each route view is created as a separate component.
Alert component is used to notify proper messages (Error/Information) with different look and feel

Whats left ? 

 > Make the page responsive ?
 > Wite test cases ? 

Flow:

landing page is Login
> Click on Register link and you will open register screen
   > Fill in the details and check the validators as in the requirement
   > Once done click on Register button, based on the response from service the user modal may/maynot be stored in local storage 
   > If operation suceeds you will be redirected to Login Screen
   > If you again try to register the same user with same email Address, it wont allow you and show a error message

> on login screen, if username(email Address) and password matches, it will navigate to Home screen
> In Home screen , you have welcome message and option to deete the user from localstorage 
> Use log out to logout from the flow


>>Auth guard helper will identify if a success ful login is in place , If yes,
   you can navigate to Home screen directly

   and If not, you will be always promopt to Login screen where u can Login urself or register yourself
   You can also directly navigate to register screen if you dont have a valid session



