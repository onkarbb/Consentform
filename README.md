# Consentform
#registration-form {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    background-color: #f2f2f2;
    border-radius: 10px;
  }
  #registration-form div {
    display: flex;
    flex-direction: column;
    margin-bottom: 10px;
    width: 100%;
    max-width: 500px;
  }
  h1 {
    text-align: center;
    margin-bottom: 20px;
    }
  #registration-form label {
    font-weight: bold;
    margin-bottom: 5px;
  }
  
  #registration-form input {
    padding: 10px;
    border-radius: 5px;
    border: none;
  }
  
  #registration-form button {
    padding: 10px;
    border-radius: 5px;
    border: none;
    background-color: #4CAF50;
    color: white;
    font-weight: bold;
    cursor: pointer;
  }
  
  #registration-form button:hover {
    background-color: #3e8e41;
  }
  
  //js
  const form = document.getElementById("registration-form");
const password = document.getElementById("password");
const confirm_password = document.getElementById("confirm-password");

// Validate password and confirm password match
function validatePassword() {
  if (password.value != confirm_password.value) {
    confirm_password.setCustomValidity("Passwords don't match");
  } else {
    confirm_password.setCustomValidity("");
  }
}

password.onchange = validatePassword;
confirm_password.onkeyup = validatePassword;

// Submit form and show success message
form.addEventListener("submit", function(event) {
  event.preventDefault();
  alert("Registration successful!");
});
