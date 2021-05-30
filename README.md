# React Streams App
This is an app similar to Twitch using React, Redux, and React Router DOM.

The differences between twitch and the react app.

**Twitch**
User can only have one channel for streaming.

**Streams React App**
User can create unlimited channels for streaming. 



---  

## App Notes

**App Goals**
- User has the ability to navigate around the separate pages of the app.
- User can login/logout.
- Learn to handle forms in Redux.
- Master `CRUD` (Create, Read, Update, Destory) operations in React/Redux.
- Plan for user errors by providing good error handling.  


---  

### React Router DOM
**IMPORTANT**

Never use `<a>` tags with react-router-dom.  Using them can wipe your data restarting the app, all previous data will be lost!

The `<Link>` Tag
- Using the `<Link>` tag overrides the `<a>` tag behavior of refreshing the HTML page when navigating through the pages of the app. 

- Preventing an HTML reload is the basis of a **SPA**(Single Page App).  

---
### Authentication

Autentication that will be used
: Google's OAuth 2.0 Flow. 

**Classic Email/Password Authentication**
- A record is stored in a database with the User's email and password.
- When a User tries to login, what the user inputs is compared with what is stored in the database.
- The user is logged in when they enter the correct email/password.

**OAuth Authentication**
- User authenticates with outside service provider (Google, Linkedin, Facebook)
- The user authorized the app to access their info. 
- Outside provider tell the app about the user.
- The outside provider is trusted with correctly handling the identification of the user.
- OAuth can be used in the app being built for user id in the app and the app making actions on behalf of the user. 

**The Difference between OAuth for Servers and OAuth for JS Browser Apps:**

**OAuth for Servers**
- Results in a 'token' that a server can use to make requests on behalf of the user.
- *Usually* used when an app needs to access user data when they are not logged in. 
- Difficult to set up because a large volume of data for the user has to be stored. 


**OAuth for JS Browser Apps**  
-  Results in a 'token' that a server can use to make requests on behalf of the user.
- *Usually* used when an app needs to access user data when they are logged in. 
- Very easy to set up thanks to Google's JS library to automate flow. 

**Steps for Setting Up OAuth**
1. Create a new project at console.developers.google.com/.
2. Set up an OAuth confirmation screen.
3. Generate an OAuth Client ID.
4. Install Google's API library, initialize it with the OAuth Client ID.
5. Make sure the library gets called any time the user clicks on the 'Login with Google' button. 

[**gapi documentation**](https://developers.google.com/identity/sign-in/web/reference)  

---

### Redux  

#streams-app
