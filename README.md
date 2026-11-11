
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>a lil thing for u </title>

<style>
:root {
  --pink: #f6a9c5;
  --deep: #b84d78;
  --ink: #60384a;
  --soft: #ffe3ed;
}

* { box-sizing: border-box; }

body {
  margin: 0;
  min-height: 100vh;
  padding: 24px 16px;
  display: grid;
  place-items: center;
  color: var(--ink);
  font-family: "Trebuchet MS", system-ui, sans-serif;
  background: linear-gradient(145deg, #fff3f7, #ffe1ec, #fff8fb);
}

.card {
  width: min(100%, 650px);
  padding: clamp(24px, 6vw, 46px);
  border: 2px solid white;
  border-radius: 28px;
  background: rgba(255,250,252,.96);
  box-shadow: 0 18px 55px rgba(166,77,112,.15);
  text-align: center;
}

.tiny {
  color: var(--deep);
  letter-spacing: .08em;
  font-size: .82rem;
}

h1 {
  color: var(--deep);
  font-size: clamp(2rem, 7vw, 3.2rem);
}

h2 { color: var(--deep); }

p { line-height: 1.65; }

.buttons {
  display: grid;
  gap: 13px;
  margin-top: 28px;
}

button {
  border: 0;
  border-radius: 16px;
  padding: 15px 20px;
  color: white;
  background: var(--deep);
  font: inherit;
  font-weight: bold;
  cursor: pointer;
  box-shadow: 0 5px 0 #8f3d60;
  transition: .15s;
}

button:hover {
  filter: brightness(1.08);
  transform: translateY(-2px);
}

button:active {
  transform: translateY(2px);
}

button.secondary {
  color: var(--deep);
  background: var(--soft);
  box-shadow: 0 5px 0 #edbfd0;
}

.hidden { display: none; }

.love-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 11px;
  margin: 24px 0;
}

.love-item {
  padding: 13px;
  border-radius: 14px;
  background: #fff0f5;
  border: 1px solid #f9d1df;
  font-weight: 600;
}

.question {
  padding: 18px;
  margin: 18px 0;
  border-radius: 18px;
  background: #fff0f5;
  font-size: 1.15rem;
  font-weight: bold;
}

.answers {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 11px;
}

.answers button { min-height: 56px; }

.feedback {
  min-height: 32px;
  margin: 20px 0 8px;
  color: var(--deep);
  font-weight: bold;
  font-size: 1.15rem;
}

.small { font-size: .9rem; opacity: .8; }

@media(max-width:420px) {
  .answers { grid-template-columns: 1fr; }
}
</style>
</head>

<body>
<main class="card">

<!-- HOME PAGE -->
<section id="home">
  <div class="tiny">ur christmas gift</div>
  <h1>hi u cutie</h1>
  <p>
    i made a lil something for u.<br>
    pick what u wanna do
  </p>

  <div class="buttons">
    <button onclick="showPage(love)">
      everything i love abt u
    </button>

    <button class="secondary" onclick="startQuiz()">
      take a lil quiz
    </button>
  </div>

  <p class="small">made with lots of love just for u</p>
</section>

<!-- LOVE PAGE -->
<section id="love" class="hidden">
  <div class="tiny">a whole page dedicated to u</div>
  <h1>everything i love abt u</h1>

  <p>where do i even start bc theres so much to love abt u</p>

  <div class="love-list">
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
    <div class="love-item">just being u</div>
  </div>

  <p>
    and honestly ts list could go on forever<br>
    i love so many things abt u
  </p>

  <button onclick="showPage(home)">← back home</button>
</section>

<!-- QUIZ PAGE -->
<section id="quiz" class="hidden">
  <div class="tiny">lets see what u know abt me</div>
  <h1>a lil quiz</h1>

  <p id="progress" class="small"></p>

  <div class="question" id="question"></div>

  <div class="answers" id="answers"></div>

  <div class="feedback" id="feedback"></div>

  <button id="next" class="hidden" onclick="nextQuestion()">
    next question →
  </button>

  <br><br>

  <button class="secondary" onclick="showPage(home)">
    ← back home
  </button>
</section>

<!-- FINISH PAGE -->
<section id="done" class="hidden">
  <div class="tiny">quiz complete</div>
  <h1>YAYYY</h1>

  <p>
    u finished the quiz!!<br>
    i hope u had fun my pookie
  </p>

  <p id="score"></p>

  <button onclick="startQuiz()">play again</button>

  <br><br>

  <button class="secondary" onclick="showPage(home)">
    back home
  </button>
</section>

</main>

<script>
const pages = ["home", "love", "quiz", "done"];

function showPage(page) {
  pages.forEach(id => {
    document.getElementById(id).classList.toggle(
      "hidden", id !== page
    );
  });
}

const questions = [
  {
    q: "what do i hate the most?",
    options: ["school", "u", "gd", "mm2"],
    answer: "school"
  },
  {
    q: "whens my birthday?",
    options: ["january", "april", "august", "november"],
    answer: "january"
  },
  {
    q: "r u beautiful?",
    options: ["yes", "no", "more beautiful than ever", "u look like shrek"],
    answer: "more beautiful than ever"
  },
  {
    q: "do i wanna come down to bulgaria and kiss u?",
    options: ["no", "yes"],
    answer: "yes"
  }
];

const rightMessages = [
  "YAY u did it!",
  "OMG YAY",
  "YIPPIE",
  "CONGRATS"
];

const wrongMessages = [
  "nuh uh thats WRONG",
  "thats VERY wrong :(",
  "if u get it wrong one more time i will uhh idk",
  "noob >:3"
];

let current = 0;
let score = 0;
let answered = false;

function randomMessage(list) {
  return list[Math.floor(Math.random() * list.length)];
}

function startQuiz() {
  current = 0;
  score = 0;
  showPage("quiz");
  renderQuestion();
}

function renderQuestion() {
  answered = false;

  const item = questions[current];

  document.getElementById("progress").textContent =
    `question ${current + 1} of ${questions.length}`;

  document.getElementById("question").textContent = item.q;
  document.getElementById("feedback").textContent = "";

  document.getElementById("next").classList.add("hidden");

  const answers = document.getElementById("answers");
  answers.innerHTML = "";

  item.options.forEach(option => {
    const button = document.createElement("button");

    button.className = "secondary";
    button.textContent = option;

    button.addEventListener("click", () => {
      chooseAnswer(option);
    });

    answers.appendChild(button);
  });
}

function chooseAnswer(choice) {
  if (answered) return;

  answered = true;

  const correct = choice === questions[current].answer;

  if (correct) score++;

  document.getElementById("feedback").textContent =
    correct
      ? randomMessage(rightMessages)
      : randomMessage(wrongMessages);

  document.querySelectorAll("#answers button").forEach(button => {
    button.disabled = true;
    button.style.opacity = ".65";

    if (button.textContent === questions[current].answer) {
      button.style.background = "#b85b83";
      button.style.color = "white";
    }
  });

  const next = document.getElementById("next");

  next.textContent =
    current === questions.length - 1
      ? "see results"
      : "next question →";

  next.classList.remove("hidden");
}

function nextQuestion() {
  current++;

  if (current < questions.length) {
    renderQuestion();
  } else {
    document.getElementById("score").textContent =
      `u got ${score} out of ${questions.length} right!`;

    showPage("done");
  }
}
</script>

</body>
</html>
