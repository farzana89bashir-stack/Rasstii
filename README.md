<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Artificial Intelligence Quiz | Raasti Class 7</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #e1f5fe, #b3e5fc);
      margin: 0;
      padding: 20px;
    }
    .container {
      max-width: 850px;
      margin: auto;
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 0 20px rgba(0,0,0,0.15);
    }
    h1, h2 {
      text-align: center;
      color: #0288d1;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #0288d1;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
    .hidden {
      display: none;
    }
    .question {
      margin: 20px 0;
    }
    .result {
      font-size: 20px;
      text-align: center;
    }
    .smile {
      font-size: 40px;
      text-align: center;
    }
    textarea, input[type="text"] {
      width: 100%;
      padding: 10px;
      border-radius: 8px;
      border: 1px solid #ccc;
      margin-top: 5px;
    }
  </style>
</head>
<body>

<div class="container" id="page1">
  <h1>Artificial Intelligence Quiz</h1>
  <h2>Raasti Class 7</h2>
  <div style="text-align:center;">
    <button onclick="startQuiz()">Start Quiz</button>
  </div>
</div>

<div class="container hidden" id="page2">
  <h2>Attempt All Parts</h2>
  <form id="quizForm">
    <h3>🧠 Part A – Multiple Choice Questions (1 mark each)</h3>

    <div class="question">1. What does AI mainly try to do?<br>
      <input type="radio" name="q1" value="a"> a) Build physical robots only<br>
      <input type="radio" name="q1" value="b"> b) Create smart machines that can think and learn<br>
      <input type="radio" name="q1" value="c"> c) Make video games faster<br>
      <input type="radio" name="q1" value="d"> d) Replace electricity
    </div>

    <div class="question">2. Example of AI used daily?<br>
      <input type="radio" name="q2" value="a"> a) A ceiling fan<br>
      <input type="radio" name="q2" value="b"> b) A wall clock<br>
      <input type="radio" name="q2" value="c"> c) Voice assistant like Alexa or Siri<br>
      <input type="radio" name="q2" value="d"> d) Torchlight
    </div>

    <div class="question">3. Which is NOT an AI application?<br>
      <input type="radio" name="q3" value="a"> a) Self-driving cars<br>
      <input type="radio" name="q3" value="b"> b) Smart home assistants<br>
      <input type="radio" name="q3" value="c"> c) Weather prediction<br>
      <input type="radio" name="q3" value="d"> d) Playing hide and seek
    </div>

    <div class="question">4. Why should students learn AI?<br>
      <input type="radio" name="q4" value="a"> a) It’s a video game<br>
      <input type="radio" name="q4" value="b"> b) It helps in painting only<br>
      <input type="radio" name="q4" value="c"> c) To understand and create future technologies<br>
      <input type="radio" name="q4" value="d"> d) Because it's a magic trick
    </div>

    <div class="question">5. What does AI use to learn?<br>
      <input type="radio" name="q5" value="a"> a) Fairy tales<br>
      <input type="radio" name="q5" value="b"> b) Data and patterns<br>
      <input type="radio" name="q5" value="c"> c) Magic spells<br>
      <input type="radio" name="q5" value="d"> d) Wind power
    </div>

    <div class="question">6. Year AI began as study?<br>
      <input type="radio" name="q6" value="a"> a) 1980<br>
      <input type="radio" name="q6" value="b"> b) 1956<br>
      <input type="radio" name="q6" value="c"> c) 2001<br>
      <input type="radio" name="q6" value="d"> d) 1945
    </div>

    <div class="question">7. What makes AI smarter?<br>
      <input type="radio" name="q7" value="a"> a) Luck<br>
      <input type="radio" name="q7" value="b"> b) Data<br>
      <input type="radio" name="q7" value="c"> c) Chalk<br>
      <input type="radio" name="q7" value="d"> d) Batteries
    </div>

    <div class="question">8. What is AI?<br>
      <input type="radio" name="q8" value="a"> a) Making machines dance<br>
      <input type="radio" name="q8" value="b"> b) Making machines think and act like humans<br>
      <input type="radio" name="q8" value="c"> c) Painting robots<br>
      <input type="radio" name="q8" value="d"> d) Just coding
    </div>

    <div class="question">9. AI in healthcare:<br>
      <input type="radio" name="q9" value="a"> a) Makes medicine colorful<br>
      <input type="radio" name="q9" value="b"> b) Helps clean hospitals<br>
      <input type="radio" name="q9" value="c"> c) Helps diagnose diseases<br>
      <input type="radio" name="q9" value="d"> d) Replaces doctors
    </div>

    <div class="question">10. After data is given to AI:<br>
      <input type="radio" name="q10" value="a"> a) It sleeps<br>
      <input type="radio" name="q10" value="b"> b) It ignores it<br>
      <input type="radio" name="q10" value="c"> c) It processes the data and learns from it<br>
      <input type="radio" name="q10" value="d"> d) It eats the data
    </div>

    <h3>✍️ Part B – Brief Answer Questions</h3>

    <div class="question">
      1. What is Artificial Intelligence in simple words?<br>
      <input type="text" name="b1">
    </div>

    <div class="question">
      2. Give two examples of AI used in daily life.<br>
      <input type="text" name="b2">
    </div>

    <div class="question">
      3. Mention two areas where AI is being used today.<br>
      <input type="text" name="b3">
    </div>

    <div class="question">
      4. Why is learning AI important for the future?<br>
      <input type="text" name="b4">
    </div>

    <div class="question">
      5. In which year was AI introduced, and what was the event called?<br>
      <input type="text" name="b5">
    </div>

    <h3>🧾 Part C – Long Answer Question</h3>

    <div class="question">
      Explain how Artificial Intelligence works using an example.<br>
      <textarea name="c1" rows="5" placeholder="Start with the role of data, explain learning, decision-making, and deployment..."></textarea>
    </div>

    <div style="text-align:center;">
      <button type="button" onclick="submitQuiz()">Submit</button>
    </div>
  </form>
</div>

<div class="container hidden" id="page3">
  <div class="result" id="resultText"></div>
  <div class="smile" id="emoji"></div>
  <div style="text-align:center; margin-top:20px;">
    <button onclick="downloadResult()">Download Result</button>
  </div>
</div>

<script>
  function startQuiz() {
    document.getElementById('page1').classList.add('hidden');
    document.getElementById('page2').classList.remove('hidden');
  }

  function submitQuiz() {
    let score = 0;
    const correct = {
      q1: "b", q2: "c", q3: "d", q4: "c", q5: "b",
      q6: "b", q7: "b", q8: "b", q9: "c", q10: "c"
    };
    for (let q in correct) {
      const selected = document.querySelector(`input[name="${q}"]:checked`);
      if (selected && selected.value === correct[q]) {
        score++;
      }
    }

    document.getElementById('page2').classList.add('hidden');
    document.getElementById('page3').classList.remove('hidden');

    const resultText = document.getElementById('resultText');
    const emoji = document.getElementById('emoji');
    resultText.textContent = score >= 7
      ? `Good Job! You scored ${score}/10 in Part A`
      : `Try Again! You scored ${score}/10 in Part A`;
    emoji.textContent = score >= 7 ? "😊" : "😕";
  }

  function downloadResult() {
    const form = document.getElementById("quizForm");
    let result = document.getElementById("resultText").textContent + "\n\n";

    for (let i = 1; i <= 5; i++) {
      result += `Part B Q${i}: ${form[`b${i}`].value}\n`;
    }

    result += `\nPart C Answer:\n${form.c1.value}\n`;

    const blob = new Blob([result], { type: "text/plain" });
    const link = document.createElement("a");
    link.download = "AI_Quiz_Result.txt";
    link.href = URL.createObjectURL(blob);
    link.click();
  }
</script>

</body>
</html>
