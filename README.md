# Homework_14
14: Reverse Engineering Authentication
 
Config Folder
    contains:
 
        Middleware sub-folder
            contains:
 
                isAuthenticated.js 
                    The isAuthenticated.js file can determine what access a user has within the code.  This may limit access or grant access depending on how it is used.  For instance, if a user opens facebook and is not logged in, they are restricted from accessing people's profiles.  If the user is logged in they may access their own profile and may search others'.
 
        config.json 
            The config.json file loads the default configuration file then loads the specific configuration file that then overrides the default.  It is basically the key that allows the user to access the JSON files.
 
        passport.js {
            The passport.js file says which NPMs are required to be installed for the application to work.  It provides the logic that says we want to use a password and email/username to grant access for the user.  It will determine if the user's information is correct.  If the user's email or password or incorrect it will send you back to the sign in page.
 
Models Folder
    contains:
 
 
        index.js
            The index.js file handles your application startup, routing, and determines the required NPMs required in node.js.  If it says require('path') you will need to enter npm install path to download the files necessary to use the application.
 
        user.js {
            The user.js file handles customization settings for a specific profile.  It locks in certain preference settings by overriding preferences initialized by other preference files.
 
Public Folder
    contains:
 
        js sub-folder
            contains:
 
                login.js
                    The login.js file provides the logic that will determine if the user's information is correct.  For instance, If the user's email or password or incorrect it will send you back to the sign in page.  If it is correct it will send you to the next designated page (ex: homepage)
 
                members.js
                    The members.js file just determines who is logged in by doing a get request.  It compares information from the database to do so and updates your HTML from that.  So if you were logged in to your facebook, when you go to your profile, it will show the profile you created, not your friend Richard's page.  If it shows your friend's page, then your friend probably logged into your computer and forgot to log out.
                
                signup.js
                    The signup.js file runs the logic to determine if you have entered the minimum requirements that allow you to generate a new profile.  If you go to the facebook signup page and put .con instead of .com it will reject your signup and not generate the HTML based on that information.
 
        stylesheets sub-folder
            contains:
                
                style.css
                    The style.css file provides the aesthetic information about your HTML.  If you set your background to blue in the css file it will make the background blue (assuming you entered the correct information to do so).
        
        login.html
            The login.html file provides the basic information you will see when you are on the login page.  It will show the fields for you to enter your name/email/password.
 
        members.html
            The members.html file is your homepage.  It will provide whatever images or text you have set for it to display, often containing a navbar at the top of the page to easily travel to other pages.
 
        signup.html
            The signup.html file will show the barebones information on the login page.  like the login page, it will contain the fields required for you to enter information.  This information will be stored in the database to be compared to what you enter in the login page's fields.
 
Routes Folder
    contains:
 
        package.json
            The package.json file contains all the package info, node modules used, version info.
 
        server.js 
            The server.js file is the js file which brings it all together.  It says which packages are required to initialize, it sets up the PORT which will host the page, creates express and middleware, creates routes and syncs database / logs messages in the terminal on successful connection to the server.
