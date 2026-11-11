
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>for my pookie</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: "Trebuchet MS", sans-serif;
  background: #ffe6f0;
  color: #743b55;
  text-align: center;
}

.page {
  display: none;
  min-height: 100vh;
  padding: 35px 20px;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.page.active {
  display: flex;
}

.card {
  background: #fff7fa;
  padding: 30px 24px;
  border-radius: 25px;
  width: 100%;
  max-width: 600px;
  box-shadow: 0 8px 25px #e9a9c5;
}

h1 {
  color: #d65d91;
  font-size: 32px;
}

p {
  font-size: 18px;
}

button {
  background: #f3a6c5;
  color: #743b55;
  border: none;
  border-radius: 18px;
  padding: 14px 22px;
  margin: 9px;
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
  transition: 0.2s;
}

button:hover {
  background: #e985af;
  transform: scale(1.04);
}

.love-item {
  background: #ffe0ed;
  border-radius: 15px;
  padding: 12px;
  margin: 9px;
  font-size: 18px;
}

#answers {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

#feedback {
  font-size: 20px;
  font-weight: bold;
  min-height: 30px;
  margin-top: 15px;
}

#progress {
  color: #bd648a;
  font-size: 15px;
}

</style>
</head>

<body>

<div id="home" class="page active">
  <div class="card">
    <h1>hi pookie</h1>
    <p>i made a lil something for u</p>
    <p>choose one</p>

    <button onclick="showPage('love')">
      everything i love abt u
    </button>

    <button onclick="startQuiz()">
      take a lil quiz
    </button>
  </div>
</div>


<div id="love" class="page">
  <div class="card">
    <h1>everything i love abt u</h1>
    <p>here are some things i love abt u</p>

    <div class="love-item">ur sweet</div>
    <div class="love-item">ur nice</div>
    <div class="love-item">ur personality</div>
    <div class="love-item">ur face</div>
    <div class="love-item">ur voice</div>
    <div class="love-item">ur funny</div>
    <div class="love-item">ur grateful</div>
    <div class="love-item">ur cute</div>
    <div class="love-item">ur beautiful</div>
    <div class="love-item">u make me happy</div>
    <div class="love-item">ur laugh</div>
    <div class="love-item">the way u talk</div>
    <div class="love-item">all ur lil habits</div>
    <div class="love-item">how u make my days better</div>
    <div class="love-item">js being u</div>
    <div class="love-item">everything abt u</div>
    <div class="love-item">how u make me smile</div>
    <div class="love-item">ur lil reactions</div>
    <div class="love-item">how u care abt me</div>
    <div class="love-item">the way u make me feel</div>

    <p>and so much more</p>

    <button onclick="showPage('home')">go back</button>
  </div>
</div>


<div id="quiz" class="page">
  <div class="card">
    <h1>a lil quiz</h1>

    <p id="progress"></p>
    <h2 id="question"></h2>

    <div id="answers"></div>

    <p id="feedback"></p>

    <button id="nextButton" onclick="nextQuestion()" style="display:none">
      next question
    </button>

    <button onclick="showPage('home')">go home</button>
  </div>
</div>


<div id="done" class="page">
  <div class="card">
    <h1>YAYYY</h1>
    <p>u finished the quiz</p>
    <p>i hope u enjoyed it pookie</p>
    <p>i love u so much</p>

    <button onclick="showPage('home')">go back home</button>
  </div>
</div>


<script>

function showPage(pageId) {
  document.querySelectorAll(".page").forEach(page => {
    page.classList.remove("active");
  });

  document.getElementById(pageId).classList.add("active");
}


// quiz questions

const originalQuestions = [

  {
    question: "what do i hate the most",
    answers: ["school", "you", "gd", "mm2"],
    correct: "school"
  },

  {
    question: "whens my birthday",
    answers: ["january", "april", "august", "november"],
    correct: "january"
  },

  {
    question: "r u beautiful",
    answers: ["yes", "no", "more beautiful than ever", "u look like shrek"],
    correct: "more beautiful than ever"
  },

  {
    question: "do i wanna come down to bulgaria and kiss u",
    answers: ["no", "yes"],
    correct: "yes"
  }

];


const rightMessages = [
  "YAY u did it",
  "omg yay",
  "yippie",
  "congrats"
];

const wrongMessages = [
  "nuh uh thats wrong",
  "thats VERY wrong",
  "if u get it wrong one more time i will uhh idk",
  "noob"
];


let questions = [];
let currentQuestion = 0;
let answered = false;


// shuffle anything in an array

function shuffle(array) {
  const shuffled = [...array];

  for (let i = shuffled.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));

    [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
  }

  return shuffled;
}


// start quiz with a random question order

function startQuiz() {
  questions = shuffle(originalQuestions).map(question => {
    return {
      ...question,
      answers: shuffle(question.answers)
    };
  });

  currentQuestion = 0;

  showPage("quiz");
  displayQuestion();
}


// display current question

function displayQuestion() {
  answered = false;

  const question = questions[currentQuestion];

  document.getElementById("question").textContent = question.question;

  document.getElementById("progress").textContent =
    "question " + (currentQuestion + 1) + " of " + questions.length;

  document.getElementById("feedback").textContent = "";

  document.getElementById("nextButton").style.display = "none";

  const answersDiv = document.getElementById("answers");

  answersDiv.innerHTML = "";

  question.answers.forEach(answer => {
    const button = document.createElement("button");

    button.textContent = answer;

    button.onclick = () => checkAnswer(answer, button);

    answersDiv.appendChild(button);
  });
}


// check answer

function checkAnswer(answer, clickedButton) {
  if (answered) return;

  answered = true;

  const question = questions[currentQuestion];
  const feedback = document.getElementById("feedback");

  const buttons = document.querySelectorAll("#answers button");

  buttons.forEach(button => {
    button.disabled = true;
  });

  if (answer === question.correct) {
    feedback.textContent =
      rightMessages[Math.floor(Math.random() * rightMessages.length)];

    clickedButton.style.background = "#a9e6b2";

  } else {
    feedback.textContent =
      wrongMessages[Math.floor(Math.random() * wrongMessages.length)];

    clickedButton.style.background = "#f3a6a6";
  }

  document.getElementById("nextButton").style.display = "inline-block";

  if (currentQuestion === questions.length - 1) {
    document.getElementById("nextButton").textContent = "finish";
  } else {
    document.getElementById("nextButton").textContent = "next question";
  }
}


// move to next question

function nextQuestion() {
  if (!answered) return;

  currentQuestion++;

  if (currentQuestion >= questions.length) {
    showPage("done");
  } else {
    displayQuestion();
  }
}

</script>

</body>
</html>
