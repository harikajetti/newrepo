Authentication using firebase.

step1: Create a firebase account.
step2: Open a new project in android studio.
step3: Add firebase to the app. Create a JSON file.
step4: Use the Firebase Assistant

To open the Firebase Assistant in Android Studio:

Click Tools > Firebase to open the Assistant window.
Click to expand one of the listed features i.e., authentication, then click the provided tutorial link.
Click the Connect to Firebase button to connect to Firebase and add the necessary code to your app.
First, add rules to your root-level build.gradle file, to include the google-services plugin:

+  buildscript {
    // ...
   dependencies {
    // ...
   classpath 'com.google.gms:google-services:3.0.0'
    }
    }

Then, in your module Gradle file (usually the app/build.gradle), add the apply plugin line at the bottom of the file to enable the Gradle plugin:

+ apply plugin: 'com.android.application'

  android {
  // ...
  }

  dependencies {
  // ...
  compile 'com.google.firebase:firebase-core:10.2.1'
  
  // Getting a "Could not find" error? Make sure you have
  // the latest Google Repository in the Android SDK manager
  }

  // ADD THIS AT THE BOTTOM
  apply plugin: 'com.google.gms.google-services'
  
Step:5 we need to enable the settings in console.

email and password must be enabled in firebase console.

Step:6 declare firebaseauth and authstatelistener as objects 
step 7: in the oncreate method initialize the instance to track whenever the user signs in and sign out.
Step 8: Attach the listener to your FirebaseAuth instance in the onStart() method and remove it on onStop() 

Sign up to new  users
Create a new createAccount method which takes in an email address and password, validates them and then creates a new user with the createUserWithEmailAndPassword method.


step 9: Add a form to register new users with their email and password and call this new method when it is submitted.

sign in existing users

step 10: Create a new signIn method which takes in an email address and password, validates them, and then signs a user in with the signInWithEmailAndPassword method.

step 11: Add a form to sign in users with their email and password and call this new method when it is submitted.

Access user information

step 12: If a user has signed in successfully you can get their account data at any point with the getCurrentUser method.



