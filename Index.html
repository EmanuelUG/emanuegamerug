<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Quiz Uíge</title>
<style>
body {
  font-family: Arial;
  background: linear-gradient(135deg,#1e3c72,#2a5298);
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
.container {
  background: white;
  padding: 20px;
  border-radius: 15px;
  width: 95%;
  max-width: 500px;
  text-align: center;
  box-shadow: 0 10px 30px rgba(0,0,0,0.3);
}
h1 { color:#2a5298; }
#options button {
  display: block;
  width: 100%;
  margin: 10px 0;
  padding: 12px;
  border: none;
  border-radius: 8px;
  background: #3498db;
  color: white;
  font-size: 16px;
  cursor: pointer;
}
#options button:hover { background: #2980b9; }
.correct { background: #2ecc71 !important; }
.wrong { background: #e74c3c !important; }
.controls {
  display: flex;
  gap: 10px;
  margin-top: 10px;
  flex-wrap: wrap;
}
.controls button {
  flex: 1;
  padding: 10px;
  border: none;
  border-radius: 8px;
  background: #f39c12;
  color: white;
  font-weight: bold;
  cursor: pointer;
}
#next-btn {
  margin-top: 15px;
  background: #27ae60;
  color: white;
  padding: 12px;
  border: none;
  border-radius: 10px;
  width: 100%;
  cursor: pointer;
}
#restart-btn {
  display: none;
  margin-top: 10px;
  background: #8e44ad;
  color: white;
  padding: 12px;
  border: none;
  border-radius: 10px;
  width: 100%;
  cursor: pointer;
}
</style>
</head>
<body>
<div class="container">
<h1>Sou do Uíge conheço Uíge</h1>
<h3 id="etapa"></h3>
<p id="question"></p>
<div id="options"></div>

<div class="controls">
<button onclick="help()">🆘 Ajuda</button>
<button onclick="skip()">⏭ Pular</button>
<button onclick="shareGame()">📤 Partilhar</button>
<button onclick="support()">📞 Suporte</button>
</div>

<button id="next-btn">Próxima</button>
<button id="restart-btn">🔄 Reiniciar Jogo</button>

<h3 id="scoreDisplay"></h3>
<div id="ranking"></div>
</div>

<audio id="correctSound">
<source src="https://assets.mixkit.co/sfx/preview/mixkit-game-success-alert-2039.mp3">
</audio>
<audio id="wrongSound">
<source src="https://assets.mixkit.co/sfx/preview/mixkit-player-losing-or-failing-2042.mp3">
</audio>

<script>
let playerName = prompt("Digite seu nome") || "Jogador";

const questions = [
{ question:"Qual é a capital da Provincia do Uíge?", options:["Negage","Kitexe","Uíge","Mucaba"], answer:"Uíge"},
{ question:"Qual é a área de extensão da Provincia do Uíge?", options:["58698km2","58798km2","38688km2","120698km2"], answer:"58698km2"},
{ question:"Quantos municipio tem a Provincia do Uíge?", options:["16","22","24","23"], answer:"23"},
{ question:"Qual é o nome do Primeiro Estadio de futebol no Uíge?", options:["4 de Janeiro","Vice António"], answer:"4 de Janeiro"},
{ question:"Quem desenvolveu este jogo?", options:["Emanuel Da Costa","Costa Eduardo","Luísa Pedro","Maria Tussamba"], answer:"Emanuel Da Costa"},
{ question:"Qual é o significado da sigla IPU?", options:["Instituto Politecnico Uíge","Instituto Polivalente do Uíge","Instituto Privado do Uíge","Instituto Privado"], answer:"Instituto Politecnico Uíge"},
{ question:"Qual é o melhor instituto Politecnico medio do Uige?", options:["IPU","EVRAMAN","CARSU","IPUG"], answer:"IPU"},
{ question:"A cidade do Uíge celebrou quantos anos em 2025?", options:["100anos","109anos","108anos","120anos"], answer:"108anos"},
{ question:"Qual é a Língua Materna da Provincia do Uíge?", options:["Português","Kikongo","Kimbundo","Ombundo"], answer:"Kikongo"},
{ question:"Qual destes Municipios esta localizado As Grutas Nzenzo?", options:["Ambuíla","Songo","Kimbele","Bembe"], answer:"Ambuíla"}
];

let currentQuestion = 0;
let score = 0;

const questionEl = document.getElementById("question");
const optionsEl = document.getElementById("options");
const nextBtn = document.getElementById("next-btn");
const etapaEl = document.getElementById("etapa");
const scoreDisplay = document.getElementById("scoreDisplay");
const restartBtn = document.getElementById("restart-btn");

const correctSound = document.getElementById("correctSound");
const wrongSound = document.getElementById("wrongSound");

/* Função para embaralhar array */
function shuffle(array){
  for(let i=array.length-1;i>0;i--){
    const j=Math.floor(Math.random()*(i+1));
    [array[i],array[j]]=[array[j],array[i]];
  }
}

/* Embaralhar perguntas no início */
shuffle(questions);

/* Mostrar pergunta atual */
function showQuestion(){
  let etapa = Math.floor(currentQuestion/5)+1;
  etapaEl.innerText = "Etapa " + etapa;

  const q = questions[currentQuestion];
  questionEl.textContent = q.question;

  optionsEl.innerHTML = "";
  let shuffledOptions = [...q.options];
  shuffle(shuffledOptions);

  shuffledOptions.forEach(option=>{
    const button = document.createElement("button");
    button.textContent = option;
    button.onclick = selectAnswer;
    optionsEl.appendChild(button);
  });

  scoreDisplay.innerText = "Dinheiro: " + score + " Kz";
}

/* Verificar resposta */
function selectAnswer(e){
  const selected = e.target.textContent;
  const correct = questions[currentQuestion].answer;

  Array.from(optionsEl.children).forEach(button=>{
    if(button.textContent===correct) button.classList.add("correct");
    else button.classList.add("wrong");
    button.disabled = true;
  });

  if(selected===correct){
    score+=100;
    correctSound.play();
  }else{
    wrongSound.play();
  }
}

/* Botão próxima pergunta */
nextBtn.onclick = ()=>{
  currentQuestion++;
  if(currentQuestion<questions.length){
    showQuestion();
  }else{
    alert("Fim do jogo! Você ganhou "+score+" Kz");
    saveRanking();
    restartBtn.style.display="block";
    nextBtn.style.display="none";
  }
}

/* Reiniciar jogo */
restartBtn.onclick = function(){
  currentQuestion = 0;
  score = 0;
  shuffle(questions);
  restartBtn.style.display="none";
  nextBtn.style.display="block";
  showQuestion();
}

/* Ajuda - remove duas opções erradas */
function help(){
  const correct = questions[currentQuestion].answer;
  let removed = 0;
  Array.from(optionsEl.children).forEach(button=>{
    if(button.textContent!==correct && removed<2){
      button.style.display="none";
      removed++;
    }
  });
}

/* Pular pergunta */
function skip(){
  currentQuestion++;
  if(currentQuestion<questions.length){
    showQuestion();
  }
}

/* Ranking */
function saveRanking(){
  let ranking = JSON.parse(localStorage.getItem("ranking"))||[];
  ranking.push({nome:playerName,pontos:score});
  ranking.sort((a,b)=>b.pontos-a.pontos);
  localStorage.setItem("ranking",JSON.stringify(ranking));
  showRanking();
}

function showRanking(){
  let ranking = JSON.parse(localStorage.getItem("ranking"))||[];
  let html="<h3>🏆 Ranking</h3>";
  ranking.slice(0,5).forEach((r,i)=>{
    html+="<p>"+(i+1)+"º "+r.nome+" - "+r.pontos+" Kz</p>";
  });
  document.getElementById("ranking").innerHTML = html;
}

/* Partilhar jogo */
function shareGame(){
  const text = "Joga este Quiz do Uíge e testa o teu conhecimento!";
  const url = window.location.href;
  if(navigator.share){
    navigator.share({title:"Quiz Uíge", text:text, url:url});
  }else{
    alert("Copie este link para partilhar: "+url);
  }
}

/* Suporte do criador */
function support(){
  alert(
    "SUPORTE DO JOGO\n\n"+
    "Se tiver problemas ou sugestões contacte o criador.\n\n"+
    "Criador: Emanuel Da Costa\n"+
    "WhatsApp:929146091\n"+
    "Obrigado por jogar!"
  );
}

showQuestion();
</script>
</body>
</html>
