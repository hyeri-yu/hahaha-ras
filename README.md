# hahaha-ras
꿈꾸며 나아가는 RAS 꿈나라 교실

<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>꿈꾸며 나아가는 RAS 꿈나라 교실</title>

<style>
:root {
  --purple: #70577F;
  --pink: #E58B9D;
  --mint: #83B99B;
  --yellow: #E9B65F;
  --lavender: #F2EAF7;
  --cream: #FFFAF2;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: "Malgun Gothic", sans-serif;
  background: linear-gradient(180deg, #FBF7FC, #FFFAF3);
  color: var(--purple);
}

/* 로고 */

header {
  text-align: center;
  padding: 30px 15px 15px;
}

.logo {
  font-size: clamp(23px, 4vw, 38px);
  font-weight: 900;
  line-height: 1.5;
  letter-spacing: -2px;
}

.pink { color: var(--pink); }
.mint { color: var(--mint); }
.yellow { color: var(--yellow); }
.purple { color: var(--purple); }

.subtitle {
  color: #A58EAD;
  font-size: 15px;
  letter-spacing: 3px;
  margin-top: 10px;
}

/* 메인 소개 */

.hero {
  margin: 20px auto;
  max-width: 1100px;
  width: 92%;
  padding: 45px 20px;
  text-align: center;
  border-radius: 30px;
  background: linear-gradient(135deg, #F2EAF7, #FFF0E8, #EAF6EF);
  box-shadow: 0 10px 30px #70577F15;
}

.hero h1 {
  font-size: clamp(24px, 4vw, 36px);
  margin: 10px 0;
}

.hero p {
  color: #887B91;
}

.hero-picture {
  font-size: 65px;
  margin: 25px 0;
}

.today {
  display: inline-flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
  margin-top: 15px;
}

.today span {
  background: white;
  border-radius: 30px;
  padding: 10px 16px;
  font-size: 14px;
}

/* 과목 카드 */

.section {
  max-width: 1100px;
  width: 92%;
  margin: 35px auto;
}

.section h2 {
  text-align: center;
  font-size: 25px;
}

.subjects {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
}

.subject {
  border: none;
  border-radius: 25px;
  padding: 25px 18px;
  min-height: 235px;
  cursor: pointer;
  transition: 0.2s;
  color: var(--purple);
  text-align: center;
}

.subject:hover {
  transform: translateY(-6px);
}

.read { background: #FCE9EF; }
.art { background: #FFF0D9; }
.sports { background: #DFF1E8; }

.subject .emoji {
  font-size: 55px;
}

.subject h3 {
  font-size: 21px;
}

.subject p {
  font-size: 14px;
  line-height: 1.7;
}

.tag {
  display: inline-block;
  background: #FFFFFFB8;
  padding: 7px 15px;
  border-radius: 30px;
  margin-top: 10px;
  font-size: 12px;
}

/* 날씨 */

.weather-box {
  max-width: 1100px;
  width: 92%;
  margin: 25px auto;
  padding: 22px;
  border-radius: 22px;
  background: white;
  text-align: center;
  box-shadow: 0 8px 25px #70577F10;
}

select {
  padding: 10px 15px;
  border: 1px solid #E9DDED;
  border-radius: 15px;
  color: var(--purple);
  background: white;
  font-size: 15px;
}

/* 속담 학습 화면 */

.page {
  display: none;
  max-width: 900px;
  width: 92%;
  margin: 20px auto 50px;
}

.page.active {
  display: block;
}

.back {
  border: none;
  background: var(--lavender);
  color: var(--purple);
  border-radius: 25px;
  padding: 12px 20px;
  cursor: pointer;
  margin-bottom: 20px;
}

.proverb-card {
  background: white;
  padding: 25px;
  border-radius: 25px;
  box-shadow: 0 10px 30px #70577F12;
}

.topics {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 20px;
}

.topics button {
  border: 1px solid #E9DDED;
  background: white;
  padding: 9px 15px;
  border-radius: 25px;
  color: var(--purple);
  cursor: pointer;
}

.topics button.selected {
  background: var(--purple);
  color: white;
}

.picture {
  min-height: 250px;
  border-radius: 20px;
  background: linear-gradient(135deg, #E9F5ED, #F8E9EF, #FFF2D9);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  cursor: pointer;
  padding: 20px;
}

.picture .scene {
  font-size: 90px;
}

.picture p {
  color: #88798E;
}

.result {
  display: none;
  background: #FFF7EB;
  padding: 22px;
  border-radius: 20px;
  margin-top: 20px;
  text-align: center;
}

.result.show {
  display: block;
}

.result h2 {
  color: #A67D91;
}

.teacher {
  background: #EFF6EF;
  padding: 15px;
  border-radius: 15px;
  margin-top: 15px;
  text-align: left;
}

.buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 20px;
}

.action {
  border: none;
  border-radius: 30px;
  padding: 12px 20px;
  background: var(--purple);
  color: white;
  cursor: pointer;
}

.action.secondary {
  background: var(--lavender);
  color: var(--purple);
}

footer {
  text-align: center;
  padding: 30px 15px;
  color: #A58EAD;
  font-size: 13px;
}

@media(max-width:700px) {
  .subjects {
    grid-template-columns: 1fr;
  }

  .subject {
    min-height: 190px;
  }

  .hero {
    padding: 30px 15px;
  }

  .logo {
    letter-spacing: -1px;
  }
}
</style>
</head>

<body>

<header>
  <div class="logo">
    <div>
      <span class="pink">꿈</span><span class="purple">꾸며 </span><span class="mint">나</span><span class="purple">아가는 </span><span class="yellow">RAS</span>
    </div>
    <div>
      <span class="pink">꿈</span><span class="mint">나</span><span class="yellow">라</span><span class="purple"> 교실</span>
    </div>
  </div>

  <div class="subtitle">READ · ART · SPORTS</div>
</header>

<!-- 메인 화면 -->

<main id="home" class="page active">

  <section class="hero">
    <h1>🌷 오늘은 무엇을 배우며 놀까요?</h1>
    <p>읽고, 표현하고, 움직이며 성장하는 아이들</p>

    <div class="hero-picture">🌈 📚 🎨 ⚽</div>

    <div class="today">
      <span id="date"></span>
      <span id="weekday"></span>
    </div>
  </section>

  <section class="section">
    <h2>✨ 배움의 문을 열어 볼까요?</h2>

    <div class="subjects">

      <button class="subject read" onclick="openPage('read')">
        <div class="emoji">📖</div>
        <h3>READ</h3>
        <p>읽고 생각하기</p>
        <p>하루에 하나씩 하는 속담풀이</p>
        <span class="tag">속담 풀이 시작하기</span>
      </button>

      <button class="subject art" onclick="openPage('art')">
        <div class="emoji">🎨</div>
        <h3>ART</h3>
        <p>표현하고 창조하기</p>
        <p>미술 · 만들기 · 음악 놀이</p>
        <span class="tag">준비 중</span>
      </button>

      <button class="subject sports" onclick="openSports()">
        <div class="emoji">⚽</div>
        <h3>SPORTS</h3>
        <p>움직이며 성장하기</p>
        <p>하하하 체육놀이</p>
        <span class="tag">체육 사이트 바로가기 ↗</span>
      </button>

    </div>
  </section>

  <section class="weather-box">
    <h3>🌤️ 오늘 우리 반 날씨</h3>
    <select id="weather" onchange="saveWeather()">
      <option>☀️ 맑아요</option>
      <option>🌤️ 구름 조금</option>
      <option>☁️ 흐려요</option>
      <option>🌧️ 비가 와요</option>
      <option>❄️ 눈이 와요</option>
      <option>🌬️ 바람이 불어요</option>
    </select>
    <p id="weatherText">오늘 날씨를 선택해 주세요.</p>
  </section>

</main>

<!-- 속담 풀이 -->

<section id="read" class="page">

  <button class="back" onclick="openPage('home')">
    ← RAS 메인으로
  </button>

  <h1 style="text-align:center">🌸 하루에 하나씩 하는 속담풀이</h1>
  <p style="text-align:center">그림을 먼저 보고 이야기해 보세요!</p>

  <div class="topics" id="topics">
    <button class="selected" onclick="chooseTopic('전체',this)">오늘의 속담</button>
    <button onclick="chooseTopic('친구와 협동',this)">친구와 협동</button>
    <button onclick="chooseTopic('노력과 끈기',this)">노력과 끈기</button>
    <button onclick="chooseTopic('말과 예절',this)">말과 예절</button>
    <button onclick="chooseTopic('배려와 나눔',this)">배려와 나눔</button>
    <button onclick="chooseTopic('지혜와 안전',this)">지혜와 안전</button>
  </div>

  <div class="proverb-card">

    <div class="picture" onclick="reveal()">
      <div class="scene" id="scene">🧒🏻 🤝 🧒🏻</div>
      <p>그림을 클릭하면 오늘의 속담을 만날 수 있어요!</p>
    </div>

    <div class="result" id="result">
      <h2 id="title"></h2>
      <p id="meaning"></p>

      <div class="teacher">
        <strong>👩‍🏫 선생님 질문</strong>
        <p id="question"></p>
      </div>

      <div class="teacher">
        <strong>🌷 오늘의 실천 약속</strong>
        <p id="practice"></p>
      </div>
    </div>

    <div class="buttons">
      <button class="action" onclick="reveal()">속담과 뜻 보기</button>
      <button class="action secondary" onclick="randomProverb()">🎰 다른 속담 뽑기</button>
    </div>

  </div>
</section>

<!-- ART 준비 화면 -->

<section id="art" class="page">
  <button class="back" onclick="openPage('home')">← RAS 메인으로</button>
  <div class="proverb-card" style="text-align:center;padding:60px 20px">
    <div style="font-size:65px">🎨</div>
    <h2>ART · 표현하고 창조하기</h2>
    <p>새로운 미술과 창의 놀이가 준비되고 있어요!</p>
  </div>
</section>

<footer>
  꿈꾸며 나아가는 RAS 꿈나라 교실<br>
  Read · Art · Sports<br>
  읽고, 표현하고, 움직이며 성장하는 아이들
</footer>

<script>

/* 날짜와 요일 자동 표시 */

const today = new Date();

document.getElementById("date").textContent =
  today.toLocaleDateString("ko-KR", {
    year:"numeric",
    month:"long",
    day:"numeric"
  });

document.getElementById("weekday").textContent =
  today.toLocaleDateString("ko-KR", {
    weekday:"long"
  });

/* 페이지 이동 */

function openPage(page) {
  document.querySelectorAll(".page").forEach(p => {
    p.classList.remove("active");
  });

  document.getElementById(page).classList.add("active");
  window.scrollTo(0,0);

  if(page === "read") {
    dailyProverb();
  }
}

/* 기존 체육 사이트 연결 */

function openSports() {
  window.open(
    "https://hahaha.qpfpahffo.workers.dev/",
    "_blank",
    "noopener,noreferrer"
  );
}

/* 날씨 선택 저장 */

function saveWeather() {
  const weather = document.getElementById("weather").value;

  document.getElementById("weatherText").textContent =
    "오늘은 " + weather + " 우리 반 날씨예요!";

  localStorage.setItem("rasWeather",weather);
}

const savedWeather = localStorage.getItem("rasWeather");

if(savedWeather) {
  document.getElementById("weather").value = savedWeather;
  saveWeather();
}

/* 속담 데이터 */

const proverbs = [

{
topic:"친구와 협동",
scene:"🧒🏻 🤝 🧒🏻",
title:"백지장도 맞들면 낫다",
meaning:"작은 일도 함께 힘을 모으면 더 쉽고 즐겁게 할 수 있어요.",
question:"친구와 함께해서 더 쉬웠던 일이 있었나요?",
practice:"오늘 친구와 장난감이나 교구를 함께 정리해요."
},

{
topic:"노력과 끈기",
scene:"🌱 ☀️ 🌼",
title:"천 리 길도 한 걸음부터",
meaning:"큰일도 작은 일부터 하나씩 시작하면 해낼 수 있어요.",
question:"새로운 일을 할 때 첫 번째로 무엇을 해볼까요?",
practice:"오늘 내가 해보고 싶은 일을 한 가지 시작해요."
},

{
topic:"말과 예절",
scene:"😊 💬 💗",
title:"가는 말이 고와야 오는 말이 곱다",
meaning:"내가 다정하게 말하면 다른 사람도 다정하게 대답해 줄 수 있어요.",
question:"친구의 마음을 기분 좋게 하는 말은 무엇일까요?",
practice:"오늘 친구에게 고운 말 한마디를 건네요."
},

{
topic:"배려와 나눔",
scene:"🍎 🧒🏻 🧒🏻",
title:"콩 한 쪽도 나누어 먹는다",
meaning:"아주 작은 것도 다른 사람과 나누면 기쁨이 커져요.",
question:"친구와 나누고 싶은 것이 있나요?",
practice:"놀이 도구나 재료를 친구와 사이좋게 나눠 써요."
},

{
topic:"지혜와 안전",
scene:"🚶‍♀️ 🌉 👀",
title:"돌다리도 두들겨 보고 건너라",
meaning:"잘 알고 있는 일도 한 번 더 살펴보면 더 안전해요.",
question:"길을 건너기 전에 무엇을 살펴봐야 할까요?",
practice:"이동할 때 멈추고 주변을 살펴본 뒤 천천히 움직여요."
},

{
topic:"노력과 끈기",
scene:"🐜 🌾 🏡",
title:"티끌 모아 태산",
meaning:"작은 것을 조금씩 모으면 나중에 큰 것이 될 수 있어요.",
question:"우리 반에서 조금씩 모으면 좋은 것은 무엇일까요?",
practice:"장난감과 책을 제자리에 하나씩 정리해요."
}

];

let currentProverb = 0;
let currentTopic = "전체";

/* 오늘의 속담 고정 */

function dailyProverb() {
  const date = new Date();
  const key = date.getFullYear() + "-" +
              (date.getMonth()+1) + "-" +
              date.getDate();

  let hash = 0;

  for(let i=0;i<key.length;i++) {
    hash = (hash * 31 + key.charCodeAt(i)) >>> 0;
  }

  currentProverb = hash % proverbs.length;
  showProverb();
}

/* 속담 표시 */

function showProverb() {
  const p = proverbs[currentProverb];

  document.getElementById("scene").textContent = p.scene;
  document.getElementById("title").textContent = p.title;
  document.getElementById("meaning").textContent = p.meaning;
  document.getElementById("question").textContent = p.question;
  document.getElementById("practice").textContent = p.practice;

  document.getElementById("result").classList.remove("show");
}

/* 뜻 공개 */

function reveal() {
  document.getElementById("result").classList.add("show");
}

/* 주제 선택 */

function chooseTopic(topic,button) {
  currentTopic = topic;

  document.querySelectorAll(".topics button").forEach(b => {
    b.classList.remove("selected");
  });

  button.classList.add("selected");

  const list = topic === "전체"
    ? proverbs
    : proverbs.filter(p => p.topic === topic);

  if(list.length > 0) {
    currentProverb = proverbs.indexOf(list[0]);
    showProverb();
  }
}

/* 랜덤 속담 뽑기 */

function randomProverb() {
  const list = currentTopic === "전체"
    ? proverbs
    : proverbs.filter(p => p.topic === currentTopic);

  if(!list.length) return;

  const selected = list[
    Math.floor(Math.random() * list.length)
  ];

  currentProverb = proverbs.indexOf(selected);
  showProverb();
}

</script>

</body>
</html>
