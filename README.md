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

    <!-- MCQs omitted here for brevity: same as your original code -->
    <!-- ... Include all 10 MCQ questions as before -->

    <!-- Same as before: short answer questions -->
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

    // Part A: MCQs
    for (let q in correct) {
      const selected = document.querySelector(`input[name="${q}"]:checked`);
      if (selected && selected.value === correct[q]) {
        score++;
      }
    }

    // Part B: Short Answer (keyword matching)
    const form = document.getElementById("quizForm");
    const bAnswers = [
      { keywords: ["smart", "think", "learn"], input: form.b1.value.toLowerCase() },
      { keywords: ["siri", "alexa", "google", "assistant"], input: form.b2.value.toLowerCase() },
      { keywords: ["healthcare", "education", "transport", "security", "banking"], input: form.b3.value.toLowerCase() },
      { keywords: ["future", "technology", "important", "skills"], input: form.b4.value.toLowerCase() },
      { keywords: ["1956", "dartmouth"], input: form.b5.value.toLowerCase() }
    ];

    bAnswers.forEach(answer => {
      const matched = answer.keywords.some(word => answer.input.includes(word));
      if (matched) score++;
    });

    // Part C: Long Answer
    const c1 = form.c1.value.toLowerCase();
    const cKeywords = ["data", "learn", "decision", "example", "training"];
    const cMatch = cKeywords.filter(word => c1.includes(word)).length;
    if (cMatch >= 3) score += 2;

    // Result display
    document.getElementById('page2').classList.add('hidden');
    document.getElementById('page3').classList.remove('hidden');

    const resultText = document.getElementById('resultText');
    const emoji = document.getElementById('emoji');
    resultText.textContent = score >= 12
      ? `Excellent! You scored ${score}/17`
      : score >= 9
      ? `Good Effort! You scored ${score}/17`
      : `Keep Practicing! You scored ${score}/17`;
    emoji.textContent = score >= 12 ? "🌟" : score >= 9 ? "😊" : "😕";
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
