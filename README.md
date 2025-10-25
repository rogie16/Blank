
document.getElementById("loginForm").addEventListener("submit", function(e) {
  e.preventDefault();

  const username = document.getElementById("username").value.trim();
  const password = document.getElementById("password").value.trim();
  const message = document.getElementById("message");

  // Simple login validation (replace with real backend logic)
  const validUser = "admin";
  const validPass = "1234";

  if (username === validUser && password === validPass) {
    message.style.color = "green";
    message.textContent = "Login successful!";
    setTimeout(() => {
      window.location.href = "dashboard.html"; // redirect to another page
    }, 1000);
  } else {
    message.style.color = "red";
    message.textContent = "Invalid username or password.";
  }
});
