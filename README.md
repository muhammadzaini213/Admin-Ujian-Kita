## Pengenalan Aplikasi Admin Ujian Kita
Aplikasi ini adalah aplikasi berbasis web yang dapat digunakan untuk mengatur ujian online dan dapat digunakan secara gratis.<br>
Berikut adalah cara menggunakan aplikasi ini:

## Step 1) Download Semua Template excel dan Web
Download dapat dilakukan secara manual dengan mengekstrak file .rar dari [link berikut](hh). <br>
Anda juga bisa langsung clone repository ini menggunakan git bash: <br>
```
cd {file lokasi}
git init
git clone https://github.com/muhammadzaini213/Admin-Ujian-Kita.git
```
## Edit dan Upload File Excel Ke Google Spreadsheet
Anda dapat menemukan file template excel dalam folder 'templates', edit sesuai kebutuhan anda, perlu diingat ada beberapa bagian penting yang tidak boleh terhapus dari excel. Untuk permulaan, anda hanya perlu memodifikasi 'Template Sekolah' dan 'Template Data Murid'. <br>
Setelah upload selesai, anda perlu mengupload excel ke dalam google spreadsheet anda masing masing serta menyalakan 'dapat dibaca oleh semua orang yang memiliki link'
    
## Masuk ke dalam website admin
Website admin dapat dibuka melalui [link publik](admin-iota-brown.vercel.app) maupun dengan membuka file ```index.html``` yang dapat ditemukan dalam folder yang anda download.

## Login Atau Daftar
Jika anda baru pertama kali menggunakan aplikasi ini, ketuk ```Buat akun baru``` pada website admin. Masukkan email dan password yang ingin anda daftarkan. Setelah itu email akan dikirim agar anda dapat memverifikasi email anda. <br>
PERINGATAN! UNTUK KEAMANAN DISARANKAN UNTUK MENGGUNAKAN EMAIL YANG TIDAK TERDAFTAR DENGAN AKUN PENTING! <br>


**Remove the default margins, padding, and box-sizing from all of the elements on the page.**
``` css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: sans-serif;
}
```

**Choose a background color for the body of the page.**
``` css
body {
  background-color: lightblue;
}
```

**Center-align the main heading ("Log In") and add a bottom margin.**
``` css
h1 {
  margin-bottom: 8%;
  text-align: center;
}
```

**Style the paragraph element ("or") to be center with horizontal lines on each side.**
``` css
p {
  margin-top: 5%;
  margin-bottom: 5%;
  width: 100%;
  text-align: center;
  border-bottom: 1px solid #000;
  line-height: 0.1em;
}

p span {
  background:#fff;
  padding:0 10px;
}
```

**Add some breathing room around the input fields.**
``` css
input {
  margin-bottom: 3%;
}

input:last-of-type {
  margin-bottom: 0;
}

input, button {
  padding: 3%;
  width: 100%;
}
```

**Vertically and horizontally center the `login-container`.**
``` css
.login-container {
  background-color: white;
  padding: 7%;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  /* horizontal align */
  width: 40vw;
  margin-left: 30vw;
  /* vertical align */
  height: 70vh;
  margin-top: 15vh;
}
```

**Hide the `create-acct` div on the original loading of the page.**
```css
#create-acct {
  display: none;
}

```

**Style the `submit`, `create-acct-btn` and `return-btn`.**
``` css
button:hover {
  cursor: pointer;
  opacity: 0.8;
  transition: 0.3s;
}

#submit, #create-acct-btn {
  background-color: #0583D2;
  color: white;
  border: none;
  margin-top: 5%;
}

#return-btn {
  background: none;
  color: grey;
  text-decoration: underline;
  border: none;
  margin-top: 3%;
}

#sign-up {
  border: none;
}
```
 
## Step 6) JavaScript
``` java
import { initializeApp } from "https://www.gstatic.com/firebasejs/9.6.10/firebase-app.js";
import { getAnalytics } from "https://www.gstatic.com/firebasejs/9.6.10/firebase-analytics.js";
import { getAuth, signInWithEmailAndPassword, createUserWithEmailAndPassword } from "https://www.gstatic.com/firebasejs/9.6.10/firebase-auth.js";

const firebaseConfig = {
  apiKey: "AIzaSyCybmXAUWgGDCMNQWvcRdaMgE31I1GkF8M",
  authDomain: "log-in-authentication-ac1b6.firebaseapp.com",
  projectId: "log-in-authentication-ac1b6",
  storageBucket: "log-in-authentication-ac1b6.appspot.com",
  messagingSenderId: "735126972855",
  appId: "1:735126972855:web:b26c16bd1de14bf361e032",
  measurementId: "G-3GKSESXV7S"
};

const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);
const auth = getAuth(app);

const submitButton = document.getElementById("submit");
const signupButton = document.getElementById("sign-up");
const emailInput = document.getElementById("email");
const passwordInput = document.getElementById("password");
const main = document.getElementById("main");
const createacct = document.getElementById("create-acct")

const signupEmailIn = document.getElementById("email-signup");
const confirmSignupEmailIn = document.getElementById("confirm-email-signup");
const signupPasswordIn = document.getElementById("password-signup");
const confirmSignUpPasswordIn = document.getElementById("confirm-password-signup");
const createacctbtn = document.getElementById("create-acct-btn");

const returnBtn = document.getElementById("return-btn");

var email, password, signupEmail, signupPassword, confirmSignupEmail, confirmSignUpPassword;

createacctbtn.addEventListener("click", function() {
  var isVerified = true;

  signupEmail = signupEmailIn.value;
  confirmSignupEmail = confirmSignupEmailIn.value;
  if(signupEmail != confirmSignupEmail) {
      window.alert("Email fields do not match. Try again.")
      isVerified = false;
  }

  signupPassword = signupPasswordIn.value;
  confirmSignUpPassword = confirmSignUpPasswordIn.value;
  if(signupPassword != confirmSignUpPassword) {
      window.alert("Password fields do not match. Try again.")
      isVerified = false;
  }
  
  if(signupEmail == null || confirmSignupEmail == null || signupPassword == null || confirmSignUpPassword == null) {
    window.alert("Please fill out all required fields.");
    isVerified = false;
  }
  
  if(isVerified) {
    createUserWithEmailAndPassword(auth, signupEmail, signupPassword)
      .then((userCredential) => {
      // Signed in 
      const user = userCredential.user;
      // ...
      window.alert("Success! Account created.");
    })
    .catch((error) => {
      const errorCode = error.code;
      const errorMessage = error.message;
      // ..
      window.alert("Error occurred. Try again.");
    });
  }
});

submitButton.addEventListener("click", function() {
  email = emailInput.value;
  console.log(email);
  password = passwordInput.value;
  console.log(password);

  signInWithEmailAndPassword(auth, email, password)
    .then((userCredential) => {
      // Signed in
      const user = userCredential.user;
      console.log("Success! Welcome back!");
      window.alert("Success! Welcome back!");
      // ...
    })
    .catch((error) => {
      const errorCode = error.code;
      const errorMessage = error.message;
      console.log("Error occurred. Try again.");
      window.alert("Error occurred. Try again.");
    });
});

signupButton.addEventListener("click", function() {
    main.style.display = "none";
    createacct.style.display = "block";
});

returnBtn.addEventListener("click", function() {
    main.style.display = "block";
    createacct.style.display = "none";
});
```
