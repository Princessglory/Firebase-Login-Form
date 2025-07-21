# Firebase Authentification System 

### Email/Password Authentication with Firestore User Profiles

##  Overview

A complete authentication solution featuring secure email/password login, user registration, and session 
persistence using Firebase Auth and Firestore. This project implements modern auth flows with clean UI 
components and proper error handling.



##  Key Features

###  Secure Authentication
- Email/password registration and login flows
- Form validation with real-time feedback
- Comprehensive error handling (invalid credentials, existing email)

###  User Management
- Stores user profiles in Firestore (first name, last name, email)
- Session persistence using localStorage


###  Modern UI/UX
- Fully responsive design 
- Animated form fields with floating labels


###  Security
- Password protection with Firebase Auth
- Automatic session management
- Secure logout functionality

 Screenshots

1. Signup Page

![Screenshot](images/Signup.png)

2. Login Page

![Screenshot](images/Login.png)


##  Technology Used

| Category        | Technologies Used                          |
|-----------------|--------------------------------------------|
| **Frontend**    | HTML5, CSS3, JavaScript (ES6)              |
| **Backend**     | Firebase Authentication, Cloud Firestore   |
| **Styling**     | CSS Grid, Flexbox       |
| **Icons**       | Font Awesome 6                             |
| **Fonts**       | Google Fonts (Poppins)                     |
| **Deployment**  | Static Hosting (Firebase Hosting optional) |



##  Installation Guide

### Prerequisites
- Firebase project ([setup guide](https://firebase.google.com/docs/web/setup))
- Modern web browser

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/Princessglory/Firebase-Login-Form.git
   cd Firebase-Login-Form

Configure Firebase

Replace the config in both firebaseauth.js and homepage.js:

javascript

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_BUCKET.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};

Run the application

Open index.html directly in your browser

Or use VS Code Live Server extension

 Project Structure

plaintext

firebase-auth/
├── public/   # Static assets

│   ├── index.html        # Login/Signup page

│   ├── homepage.html     # Protected dashboard

│   └── assets/           # Images/icons

├── styles/               # CSS files
            
│   └── styles.css        # Global styles

├── scripts/              # JavaScript files

│   ├── script.js         # UI interactions

│   ├── firebaseauth.js   # Auth logic

│   └── homepage.js       # Protected routes

└── README.md             # Project documentation
 
 Code Highlights

User Registration Flow

javascript

// firebaseauth.js

createUserWithEmailAndPassword(auth, email, password)

  .then((userCredential) =>
  
   {

    const user = userCredential.user;
    
    // Save additional user data to Firestore
    setDoc(doc(db, "users", user.uid), {
      firstName: firstName,
      lastName: lastName,
      email: email,
      createdAt: serverTimestamp()
    });
  });

Session Management

javascript

// homepage.js

onAuthStateChanged(auth, (user) =>
 {
  const userId = localStorage.getItem('loggedInUserId');
  
  if (!userId)
   {
    window.location.href = 'index.html';
  }

   else
    {
    // Load user data from Firestore
    const docRef = doc(db, "users", userId);
    // ... fetch and display user data
  }
});


📬 Contact Me

📧 Email: [mofogofoluwa744@gmail.com]

🔗 LinkedIn: [www.linkedin.com/in/princess-glory-049270365]

🐱 GitHub:[https://github.com/Princessglory]



 Thanks for Visiting!

Feel free to explore, fork, or contribute to this project. Let’s connect and build something amazing together! 🚀
