# Contemporary Web Applications (QHO640) - AE2
## Project Title: Students Time Management web application 

## Link to hosted web-app: 
- https://contemporary-web-app-6f54f.web.app
- https://contemporary-web-app-6f54f.firebaseapp.com


## My GitHub official/clean link: https://github.com/rusuot/Time_App_QHO640_OviR
###### My GitHub history link (drafts):  https://github.com/rusuot/MyTime_Mngmnt_App_Contemp_Web_app
I have worked on a separate repo as I'm facing some issues with pushing commits directly from Visual Code, hence each time I'm uploading files in GIT.
### Student Name: Rusu Ovidiu Tiberiu
### Student ID: 10179295

## Tech
What I have used for this project:
- [Visual Code](https://code.visualstudio.com/)
- [Google Firebase](https://firebase.google.com/)
- [node.js](https://code.visualstudio.com/docs/nodejs/nodejs-tutorial)
- [React](https://react.dev/)
- [Contemporary Web Applications (QHO640) courses Solent University](https://learn.solent.ac.uk/course/view.php?id=54766&section=9#tabs-tree-start)
- [Courses - GitHub support](https://joeappleton18.github.io/web-dev-2021-notes/sessions/week_1/#why-do-we-even-need-webpack)
- [Exercises solutions - GitHub support](https://github.com/joeappleton18/running-contemp-web-app-solutions/branches/stale)
- [Dillinger](https://dillinger.io/)



## Link to hosted web-app: 
- https://contemporary-web-app-6f54f.web.app
- https://contemporary-web-app-6f54f.firebaseapp.com

## Installation
Steps to follow for project installation:
1. Download the zip from GIT link: (need Visual Code..node.js)
2. Open Visual Code, open folder downloaded unzipped folder at step 1
3. Install dependencies by running next command in Visual Code Terminal:
```sh
npm install
```
4. Linking Firebare to project step.
In your downloaded files, you don't have file named ".env.dev" which should contain evironment variables to Firebase DB, hence this must be created. Please follow next step for this:
4.1 In Visual Code, in your root folder, from right click options select "New File".
4.2 Rename your new file created into: ".env.dev"
4.3 Add and save in your ".env.dev" next lines:
// environment variables (used for my firebase connection)
```sh
REACT_APP_API_KEY=""
REACT_APP_AUTH_DOMAIN=""
REACT_APP_PROJECT_ID=""
REACT_APP_STORAGE_BUCKET=""
REACT_APP_MESSAGING_SENDER_ID=""
REACT_APP_APP_ID=""
```
5. At this moment your personal Firebase DB is not created, hence please follow next steps to create it:
 5.1 Create an account into [Firebase](https://console.firebase.google.com/)
After you have logged in into your account, you need to create a project:
5.2 From "Add a project" you will be re-directed to "Let's start with a name for your project " and asked to insert your firebase project name.

- Create project step 1: Insert name example: "test" and copy and SAVE somewhere the unique identifier, in my case is: "test-c29bb" and press "Continue".
- Create project step 2: "Google Analytics for your Firebase project..." here press "Continue".
- Create project step 3: "Configure Google Analytics" - at "Choose or create a Google Analytics account" click on combo box and select "Default Account for Firebase" and press "Create project".
- In several seconds/1 minute you will see "Your Firebase project is ready" and press "Continue".
5.3 Now, a web application registration must be done, remain in this Firebase project page from previous step.
- You'll see something like: "Get started by adding Firebase to your app<some icons...> Add an app to get started".
- There are 5 icons, you can hover over them, please click on the 3rd one, hovering it you'll see "Web" text. The icon looks like: "</>".
- Once you selected "</>", you'll be bring up to "Add Firebase to your web app" page.
In here:
 - Register app: Insert app nickname, I've just put "test" and click on button "Register app". (do not select hosting now, we'll be done later).
 - Add Firebase SDK. In here you'll see:
Don't run yet anyting, just save these into a notepad or something, you'll need values from apiKey, authDomani .. and so on to put them in ".env.dev" file.
```sh
npm install firebase
...
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
import { getAnalytics } from "firebase/analytics";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
// For Firebase JS SDK v7.20.0 and later, measurementId is optional
const firebaseConfig = {
  apiKey: "AIzaSyBS7fKPcTG9tQ5CUDZefdOxk0uU1jKIoF8",
  authDomain: "test-c29bb.firebaseapp.com",
  projectId: "test-c29bb",
  storageBucket: "test-c29bb.appspot.com",
  messagingSenderId: "938069241895",
  appId: "1:938069241895:web:fb9d0121942872ab3b5e02",
  measurementId: "G-2ZED1913N3"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);
```
Now, bring your Visual Code and COPY and SAVE in your ".env.dev" file the values. SIMILAR with this (I've put mines):
```sh
REACT_APP_API_KEY="AIzaSyBS7fKPcTG9tQ5CUDZefdOxk0uU1jKIoF8"
REACT_APP_AUTH_DOMAIN="test-c29bb.firebaseapp.com"
REACT_APP_PROJECT_ID="test-c29bb"
REACT_APP_STORAGE_BUCKET="test-c29bb.appspot.com"
REACT_APP_MESSAGING_SENDER_ID="938069241895"
REACT_APP_APP_ID="1:938069241895:web:fb9d0121942872ab3b5e02"
```
Now, look on the firebsae website, you'll still on "2 Add Firebase SDK" page.
It's said "npm install firebase". Go into your Visual Code, in Terminal and run:
```sh
npm install firebase
```
At this moment you have installed the npm firebase and saved your variables in .env.de file.


Now, look on the firebsae website, you'll still on "2 Add Firebase SDK" page.
You have a button with "Continue to the console", please select it, now you should be back on your project firebase page.
5.4 Now, step for actually db creation with "enable email/password" authentication:

In your firebase project website page, select "Cloud Firestore".
Now, in the page you'll see the button option: "Create database". Please select it.
In the popup "Create database" don't change anything, just press "Next".
Let the default option selected "Start in production mode" and select button "Create". (in a few sec the db is created).
Now, you need to set the email - password auth, for this follow next steps:
- Come back in firebase website to your project page (from your project name you have a combo box with next options: See all projects, Add a project.... select See all, and after that just open your project page)
- In here, you'll see at "Store and sync app data in milliseconds" next options "Authentication", "Cloud Firestore"...
- Open "Authentication". In Authentication page, select "Get started".
- Under "Authentication" you have some menu options: "Users", "Sign-in method"...
- Select "Sign-in method" and from Native providers, select "Email/Password".
- Enable "Email/Password" (enable toggle button) and SAVE.
- Now that email/password auth is enabled, you need to go into the DB to change auth rules, for this follow:
-- In the left pane, under Project shortcuts you have "Firebase Datastore", "Authentication". Select "Firebase Datastore".
--You are now in your db page, you will have some menu options like: "Data", "Rules", "Indexes" and so on. Select "Rules".
--Default you'll have:

```sh
rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if false;
    }
  }
}
```

-- Delete them, and insert next: 
```sh
// Allow read/write access on all documents to any user signed in to the application
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null; }}}
```
Only FYI mention:  These rules definition were taken from [Firebase DOCS](https://firebase.google.com/docs/firestore/security/get-started)

After you have added the rules, select button "Publish".
At this moment all configs to firebase are done, next steps contain details on how to run the app locally.

## Start the App  - locally with Firebase DB
Having all set related to Firebase, run now the students time managemnet web application:
1. In Visual Code, in Terminal run next command:
```sh
npm run start
```
3. The app will start with success at: 
- http://localhost:3000/ 
Please Sign-up, create an account to eb able to login.
4. At http://localhost:3000/, after you log in:
In Web you will get next 3 Firebase Errors (see them in Network Tool - press F12):
- toast: "Error! Hint: Firebase indexes might not be created yet!!! The data can not be fetched. "
- Error in F12: "FirebaseError: The query requires an index. You can create it here: ..." 
If you open Network Tool-Console, you'll see something like:
```sh
FirebaseError: The query requires an index. You can create it here: https://console.firebase.google.com/v1/r/project/time-app-cont-web/firestore/indexes?create_composite=ClFwcm9qZWN0cy90aW1lLWFwcC1jb250LXdlYi9kYXRhYmFzZXMvKGRlZmF1bHQpL2NvbGxlY3Rpb25Hcm91cHMvaGlzdG9yeS9pbmRleGVzL18QARoICgR1c2VyEAEaDQoJY3JlYXRlZEF0EAIaDAoIX19uYW1lX18QAg
FirebaseError: The query requires an index. You can create it here: https://console.firebase.google.com/v1/r/project/time-app-cont-web/firestore/indexes?create_composite=ClFwcm9qZWN0cy90aW1lLWFwcC1jb250LXdlYi9kYXRhYmFzZXMvKGRlZmF1bHQpL2NvbGxlY3Rpb25Hcm91cHMvbXl0b2Rvcy9pbmRleGVzL18QARoICgR1c2VyEAEaDQoJY3JlYXRlZEF0EAIaDAoIX19uYW1lX18QAg
FirebaseError: The query requires an index. You can create it here: https://console.firebase.google.com/v1/r/project/time-app-cont-web/firestore/indexes?create_composite=ClRwcm9qZWN0cy90aW1lLWFwcC1jb250LXdlYi9kYXRhYmFzZXMvKGRlZmF1bHQpL2NvbGxlY3Rpb25Hcm91cHMvYWN0aXZpdGllcy9pbmRleGVzL18QARoICgR1c2VyEAEaDQoJY3JlYXRlZEF0EAIaDAoIX19uYW1lX18QAg
```
Select the url from all 3 errors received in order to create the 3 needed indexes in Firebase DB: mytodos, activities, history.
Selecting an URL, you'll be redirected to your Firebase website, and you'll see for e.g. a popup with "Create or update indexes. The history collection requires additional indexing to run your query".
--In here (popoup) select SAVE. - like this index for history will be enabled.
Repeat this step for all your 3 Firebase Errors links, all 3 indexes must be created: history, mytodos & activities.
In firebase website db: Indexes statuses will go from "Building.." into "Enabled" once they are successfully created.

Note: If the URL link doesn't redirect you to "Create or update indexes. The history collection requires additional indexing to run your query" to have the SAVE button, just try to select again the URL to reload it. No issues should be encountered in here.
Once all 3 indexes are successfully created will have the status: Enabled (in Firebase website)
Something similar with (in firebase website):
```sh
Collection ID	Fields indexed
Query scope		Status	
mytodos	user Ascending createdAt Descending __name__ Descending	Collection		Enabled	
history	user Ascending createdAt Descending __name__ Descending	Collection		Enabled	
activities	user Ascending createdAt Descending __name__ Descending	Collection		Enabled
```

5. Now you can use the Time Management App, as you wish.

#### Time Management App - Happy flow scenario
1. Open App
2. Login (Signup first if you don't have an account)
3. Add some free hours from Home App
4. Add an activity (think about activities as courses from University, hints are also provided in app). Currently activities/courses hints reflect the 3rd University year.
5. Add some TO-DO tasks (pick an activity/course) and link the TO-DO task to that activity.
6. Add some invested/burned hours from Home App, as you invest hours in that specific task

## Firebase Hosting 
## Link to hosted web-app: 
- https://contemporary-web-app-6f54f.web.app
- https://contemporary-web-app-6f54f.firebaseapp.com


#### (Already hosted, check "Link to hosted web-app" but here are the steps I followed if you want to obtain other hosted websites )
1. In Firebase website, at your project name, you have a combo box with options like: "See all projects", open your project page.
In section "Store and sync app data in milliseconds" you'll see: "Authentication", "Cloud Firestore", and you'll have a link for "See all Build features". Select this.
Search for "Hosting" and select it.
In "Hosting" page, select "Get started".
In page "Set up Firebase Hosting", follow:
step 1: "Install Firebase CLI":
--Copy the command and run it in Visual Code Terminal (ctrl + C and insert Y - to cancel localhost app run OR open another terminal ):
```sh
npm install -g firebase-tools
```
After you run the command in VC Terminal, go back to "Set up Firebase Hosting" firebse website page.
You're still on step 1:  "Install Firebase CLI"
Press NEXT.
step 2: "Initialise your project":
--In Visual Code Terminal run:
```sh
firebase login
```
The output in Terminal after running this, in my case is: "Already logged in as rusuot23@gmail.com".
and after run next command:
```sh
firebase init
```
Now in Terminal you are asked:
```sh
Are you ready to proceed? (Y/n)
```
Insert Y and hit enter.
Now in Terminal you are asked:
```sh
Which Firebase features do you want to set up for this directory? Press Space to select features, then Enter to confirm your choices.
```
With keyboard down arrow navigate to:
```sh
( ) Hosting: Configure files for Firebase Hosting and (optionally) set up GitHub Action deploys
```
Now, press SPACE keyboard key to select it.
It will look like:
```sh
>(*) Hosting: Configure files for Firebase Hosting and (optionally) set up GitHub Action deploys
```
Press ENTER.
Now in your Terminal you are asked:
```sh
Please select an option: (Use arrow keys)
```
Default is set on:
```sh
> Use an existing project
```
Let this default option as you have already the project and hit ENTER.
Now in your Terminal you are asked:
```sh
Select a default Firebase project for this directory: (Use arrow keys)
```
In here, if you have multiple projects, select your current project.
In my case, specified in this Readme file is: "time-app-cont-web (time-app-cont-web)"
I've selected and it looks like:
```sh
? Select a default Firebase project for this directory: 
  contemporary-web-app-6f54f (Contemporary Web App)     
> test-c29bb (test)
  time-app-cont-web (time-app-cont-web)
  time-app-cont-web-cbc05 (time-app-cont-web)
```
Press ENTER.
Now in your Terminal you'll see and be asked:
```sh
=== Hosting Setup
..
? What do you want to use as your public directory? (public)
```
delete public and write "build", like:
```sh
? What do you want to use as your public directory? build
```
Now in your Terminal you'll see and be asked:
```sh
? Configure as a single-page app (rewrite all urls to /index.html)? (y/N)
```
Insert N (as No!). 
Now in your Terminal:
```sh
? What do you want to use as your public directory? build
? Configure as a single-page app (rewrite all urls to /index.html)? (y/N) N
```
Press ENTER.
Now in your Terminal you'll be asked:
```sh
? Set up automatic builds and deploys with GitHub? (y/N)
```
Insert N, Like:
```sh
? Set up automatic builds and deploys with GitHub? (y/N)N
```
With N inserted, press ENTER.
You'll see now that you'll have a "build" folder in your project.
Now, in your Visual Code Terminal, you'll see next logs:
```sh
=== Hosting Setup

Your public directory is the folder (relative to your project directory) that
will contain Hosting assets to be uploaded with firebase deploy. If you
have a build process for your assets, use your build's output directory.

? What do you want to use as your public directory? build
? Configure as a single-page app (rewrite all urls to /index.html)? No
? Set up automatic builds and deploys with GitHub? No
? File build/404.html already exists. Overwrite? No
i  Skipping write of build/404.html
? File build/index.html already exists. Overwrite? No
i  Skipping write of build/index.html

i  Writing configuration info to firebase.json...
i  Writing project information to .firebaserc...

+  Firebase initialization complete!
```
----
Be sure that /public/index.html and /build/index.html have same content, if not, follow:

1. In Visual Code, expand your folder named "public".
2. In Visual Code, expand your folder named "build".
3. Copy the content from /public/index.html  into /build/index.html

----


Now, go into Firebase website, Hosting page, you have completed step 1 and step 2: "Initialise your project", you are at step 3 "Deploy to Firebase Hosting".
At this step 3 "Deploy to Firebase Hosting", copy the command and run it into Visual Code Terminal:
```sh
firebase deploy
```
After running the above command you'll have in VC Terminal next logs:
```sh
firebase deploy


=== Deploying to 'test-c29bb'...

i  deploying hosting
i  hosting[test-c29bb]: beginning deploy...
i  hosting[test-c29bb]: found 2 files in build
+  hosting[test-c29bb]: file upload complete
i  hosting[test-c29bb]: finalizing version...
+  hosting[test-c29bb]: version finalized
i  hosting[test-c29bb]: releasing new version...
+  hosting[test-c29bb]: release complete

+  Deploy complete!

Project Console: https://console.firebase.google.com/project/test-c29bb/overview
Hosting URL: https://test-c29bb.web.app
```

Now:
In Visual Code, root folder, you have a file named: "package.json".
Open the file, and check at "scripts", you have now:
```sh
  "scripts": {
    "start": "env-cmd -f .env.dev react-scripts start",
    "build": "react-scripts build",
    "serve": "serve build",
    "eject": "react-scripts eject",
    "build:deploy": "env-cmd -f .env.dev npm run build && firebase deploy -P contemporary-web-app-6f54f"
  },
```
Update your current project ID and name with:
```sh
  "scripts": {
    "start": "env-cmd -f .env.dev react-scripts start",
    "build": "react-scripts build",
    "serve": "serve build",
    "eject": "react-scripts eject",
    "build:deploy": "env-cmd -f .env.dev npm run build && firebase deploy -P test-c29bb"
  },
```
Mention only: "build:deploy": "env-cmd -f .env.dev npm run build && firebase deploy -P [Firebase Project Id]"  }
Save files, and in Visual Code Terminal run:
```sh
npm run build:deploy
```

Afetr running the above command, you'll have next logs in VC Terminal:
```sh
npm run build:deploy
..
> time-mngmnt-app@0.1.0 build:deploy
> env-cmd -f .env.dev npm run build && firebase deploy -P test-c29bb


> time-mngmnt-app@0.1.0 build
> react-scripts build        

Creating an optimized production build...
One of your dependencies, babel-preset-react-app, is importing the
"@babel/plugin-proposal-private-property-in-object" package without        
declaring it in its dependencies. This is currently working because        
"@babel/plugin-proposal-private-property-in-object" is already in your     
node_modules folder for unrelated reasons, but it may break at any time.   

babel-preset-react-app is part of the create-react-app project, which      
is not maintianed anymore. It is thus unlikely that this bug will
ever be fixed. Add "@babel/plugin-proposal-private-property-in-object" to  
your devDependencies to work around this error. This will make this message
go away.
  
Compiled successfully.

File sizes after gzip:

  275.23 kB  build\static\js\main.376b3455.js
  36.07 kB   build\static\css\main.14d121d1.css

The build folder is ready to be deployed.
You may serve it with a static server:

  npm install -g serve
  serve -s build

Find out more about deployment here:

  https://cra.link/deployment


=== Deploying to 'test-c29bb'...

i  deploying hosting
i  hosting[test-c29bb]: beginning deploy...
i  hosting[test-c29bb]: found 14 files in build
+  hosting[test-c29bb]: file upload complete
i  hosting[test-c29bb]: finalizing version...
+  hosting[test-c29bb]: version finalized
i  hosting[test-c29bb]: releasing new version...
+  hosting[test-c29bb]: release complete

+  Deploy complete!

Project Console: https://console.firebase.google.com/project/test-c29bb/overview
Hosting URL: https://test-c29bb.web.app

```

#### New hosted web links:
test-c29bb.web.app
test-c29bb.firebaseapp.com

### Troubleshoot:
Hints for a successfull run:
1. Be sure you copy the Firebase auth, api keys correctly.
2. For firebase hosting, public/index.html & build/index.html files needs to have same content. The original for the app is found in public. So copy from public into build:
-- In Visual Code, expand your folder named "public".
-- In Visual Code, expand your folder named "build".
-- Copy the content from /public/index.html  into /build/index.html
3. Any change in any file must be saved, and firebase init again.
4. Ref:  https://medium.com/@mahmud886/google-firebase-you-can-host-your-website-and-single-page-application-aba4d854139 

#### Notes/troubleshooting from Firebase Hosting:
----
- Where are Firebase Hosting details for website hosted?:
I have selected "Go To Console" in Firebase Hosting website, and in:
https://console.firebase.google.com/project/contemporary-web-app-6f54f/hosting/sites/contemporary-web-app-6f54f
In left pane, under Projects Shortcuts, in Hosting I have "Mange Site" Dashboard with:
contemporary-web-app-6f54f.web.app
contemporary-web-app-6f54f.firebaseapp.com
----
- Firebase Hosting (websites) should run without any issues, as the time expiration is set for the begining of march, but I will extend as days go by (there is a limit of 30 days), you should not have any issues.

- History of commands in Visual Terminal that might help:
npm install
npm install firebase
npm run start
npm install -g firebase-tools
firebase login
firebase init
firebase init
firebase init
firebase deploy
npm run build:deploy
---


