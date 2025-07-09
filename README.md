# Tech-for-girls-registration-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Tech For Girls Registration</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="container">
    <h1>Tech For Girls Registration</h1>
    <form id="registrationForm">
      <label for="name">Name</label>
      <input type="text" id="name" required>

      <label for="email">Email</label>
      <input type="email" id="email" required>

      <label for="age">Age</label>
      <input type="number" id="age" required>

      <label for="screenshot">Upload Screenshot</label>
      <input type="file" id="screenshot" accept="image/*" required>

      <button type="submit">Submit</button>
    </form>

    <div class="whatsapp-share">
      <button id="whatsappShare">Share on WhatsApp</button>
      <p id="shareCount">Shared: 0 times</p>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
.container {
  max-width: 500px;
  margin: auto;
  background: white;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

h1 {
  text-align: center;
  color: #d63384;
}

form label {
  display: block;
  margin-top: 15px;
  font-weight: bold;
}

form input[type="text"],
form input[type="email"],
form input[type="number"],
form input[type="file"] {
  width: 100%;
  padding: 10px;
  margin-top: 5px;
  border-radius: 5px;
  border: 1px solid #ccc;
}

button {
  margin-top: 20px;
  width: 100%;
  padding: 12px;
  background-color: #20c997;
  color: white;
  border: none;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
}

button:disabled {
  background-color: #6c757d;
}

.whatsapp-share p {
  margin-top: 10px;
  font-size: 14px;
  text-align: center;
}
let shareCount = localStorage.getItem("whatsappShareCount") || 0;
document.getElementById("shareCount").innerText = `Shared: ${shareCount} times`;

document.getElementById("whatsappShare").addEventListener("click", () => {
  const message = encodeURIComponent("Check out Tech For Girls Registration Page!");
  const url = encodeURIComponent(window.location.href);
  const whatsappUrl = `https://wa.me/?text=${message}%20${url}`;

  window.open(whatsappUrl, "_blank");

  shareCount++;
  localStorage.setItem("whatsappShareCount", shareCount);
  document.getElementById("shareCount").innerText = `Shared: ${shareCount} times`;
});
