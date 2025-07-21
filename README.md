#  Firebase Authentication System  
### Email/Password Authentication with Firestore User Profiles

---

##  Overview
A complete authentication solution featuring secure email/password login, user registration, and session persistence using Firebase Auth and Firestore.

---

##  Key Features
###  Secure Authentication
- Email/password registration and login flows
- Form validation with real-time feedback
- Comprehensive error handling

### 👤 User Management
- Stores user profiles in Firestore
- Session persistence using localStorage

###  Modern UI/UX
- Fully responsive design
- Animated form fields with floating labels

---

##  Screenshots
| Signup Page | Login Page |
|-------------|------------|
| ![Signup](images/Signup.png) | ![Login](images/Login.png) |

---

##  Technology Used
| Category       | Technologies Used |
|----------------|-------------------|
| **Frontend**   | HTML5, CSS3, JavaScript |
| **Backend**    | Firebase Authentication, Firestore |
| **Styling**    | CSS Grid, Flexbox |

---

##  Installation Guide
### Prerequisites
- Firebase project
- Modern web browser

### Setup
1. Clone the repository:
```bash
git clone https://github.com/Princessglory/Firebase-Login-Form.git
cd Firebase-Login-Form 

```
2. Configure Firebase
```bash
// In firebaseauth.js and homepage.js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID"}
```
📂 Project Structure

firebase-auth/

├── public/
│   ├── index.html
│   └── homepage.html

├── styles/
│   └── styles.css

├── scripts/
│   ├── firebaseauth.js
│   └── homepage.js

└── images/
    ├── Signup.png
    └── Login.png
    
    
User Registration

```
    createUserWithEmailAndPassword(auth, email, password)
  .then((userCredential) => {
    setDoc(doc(db, "users", user.uid), {
      firstName: firstName,
      lastName: lastName
    });
  });
```

📬 Contact Me

📧 Email: [[mofogofoluwa744@gmail.com](https://mailto:mofogofoluwa744@gmail.com/)]

🔗 LinkedIn: [https://linkedin.com/in/princess-glory-049270365]

🐱 GitHub:[[github.com/Princessglory](https://github.com/Princessglory)]

Thanks for Visiting!

Feel free to explore, fork, or contribute to this project. Let’s connect and build something amazing together! 🚀
