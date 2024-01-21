<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prom Invitation</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to right, #3498db, #2980b9);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }

    #invitation-container {
      background-color: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
      text-align: center;
    }

    #invitation-text {
      font-size: 20px;
      margin-bottom: 20px;
    }

    #yesButton, #noButton {
      background-color: #27ae60;
      color: #fff;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      margin: 10px;
      transition: background-color 0.3s ease;
    }

    #yesButton:hover, #noButton:hover {
      background-color: #219653;
    }

    #response-container {
      display: none;
      margin-top: 20px;
    }

    #response-text {
      font-size: 18px;
      margin-bottom: 10px;
    }

    #cat-photo {
      max-width: 25%;
      border-radius: 5px;
      margin-top: 10px;
    }

    #thanks-text {
      font-size: 16px;
      margin-top: 5px;
    }
  </style>
</head>
<body>

  <div id="invitation-container">
    <h2 id="invitation-text">Meow Meow Nigga, will you go to prom with me?</h2>
    <button id="yesButton" onclick="showResponse('yes')">Yes</button>
    <button id="noButton" onclick="showResponse('no')">No</button>

    <div id="response-container">
      <p id="response-text"></p>
      <img id="cat-photo" src="" alt="Cat Photo">
      <p id="thanks-text"></p>
    </div>
  </div>

  <script>
    function showResponse(answer) {
      var responseContainer = document.getElementById('response-container');
      var responseText = document.getElementById('response-text');
      var catPhoto = document.getElementById('cat-photo');
      var thanksText = document.getElementById('thanks-text');

      if (answer === 'yes') {
        responseText.innerHTML = 'Thanks &lt;3';
        catPhoto.src = 'https://i.imgur.com/1V0KcZF.jpeg'; // Replace with your happy cat image URL
        thanksText.innerHTML = 'Thanks <3';
      } else {
        responseText.innerHTML = 'Okay \'_\'';
        catPhoto.src = 'https://i.imgur.com/4jqU9kp.jpeg'; // Replace with your sad cat image URL
        thanksText.innerHTML = '';
      }

      responseContainer.style.display = 'block';
    }
  </script>

</body>
</html>
