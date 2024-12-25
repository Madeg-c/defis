# defis
 
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Défis Secrets</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 20px;
    }
    input, button {
      padding: 10px;
      font-size: 16px;
    }
    #result {
      margin-top: 20px;
      font-weight: bold;
    }
  </style>
  <script>
    const challenges = {
      "Alice": "Faire fermer les volets à Martin",
      "Martin": "Donner un verre d'eau à Sarah",
      "Sarah": "Faire rire Alice",
      "Paul": "Chanter une chanson à Julie",
      "Julie": "Faire passer une serviette à Paul"
    };

    function getChallenge() {
      const name = document.getElementById("name").value.trim();
      const challenge = challenges[name];
      if (challenge) {
        document.getElementById("result").innerText = `Votre défi : ${challenge}`;
      } else {
        document.getElementById("result").innerText = "Nom introuvable ! Vérifiez l'orthographe.";
      }
    }
  </script>
</head>
<body>
  <h1>Défis Secrets</h1>
  <p>Entrez votre prénom pour découvrir votre défi :</p>
  <input type="text" id="name" placeholder="Entrez votre prénom">
  <button onclick="getChallenge()">Obtenir mon défi</button>
  <p id="result"></p>
</body>
</html>
