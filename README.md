<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="NEET PG Quick Revision Medical App">
  <meta name="theme-color" content="#0d6efd">
  <title>NEET PG Quick Revision</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 20px;
      background-color: #f4f6f9;
    }

    h1 {
      color: #0d6efd;
    }

    .question {
      font-size: 20px;
      margin: 20px;
      font-weight: bold;
    }

    button {
      padding: 10px 20px;
      margin: 8px;
      cursor: pointer;
      border-radius: 6px;
      border: none;
      background-color: #0d6efd;
      color: white;
    }

    button:hover {
      background-color: #084298;
    }

    #result {
      font-size: 18px;
      margin-top: 15px;
      font-weight: bold;
    }
  </style>
</head>

<body>

<h1>NEET PG Question of the Day</h1>

<div class="question" id="question"></div>
<div id="options"></div>
<p id="result"></p>

<script>
const quiz = [
  {
    question: "Most common cause of death in blood transfusion?",
    options: ["Anaphylaxis", "Hemolytic reaction", "TRALI", "Infection"],
    answer: "Hemolytic reaction"
  },
  {
    question: "Drug of choice in Myasthenia Gravis?",
    options: ["Atropine", "Pyridostigmine", "Propranolol", "Phenytoin"],
    answer: "Pyridostigmine"
  }
];

let current = 0;

function loadQuestion() {
  document.getElementById("question").innerText = quiz[current].question;
  let optionsHTML = "";
  quiz[current].options.forEach(option => {
    optionsHTML += `<button onclick="checkAnswer('${option}')">${option}</button>`;
  });
  document.getElementById("options").innerHTML = optionsHTML;
}

function checkAnswer(selected) {
  if (selected === quiz[current].answer) {
    document.getElementById("result").innerText = "Correct ✅";
  } else {
    document.getElementById("result").innerText = "Wrong ❌";
  }
}

loadQuestion();
</script>

</body>
</html><img width="1024" height="1024" alt="IMG_7207" src="https://github.com/user-attachments/assets/47fc3ecb-18a5-406c-b595-796ffc6017e7" />
