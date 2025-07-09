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
