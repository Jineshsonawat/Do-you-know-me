# Quiz

var score = 0;
var readlineSync = require("readline-sync");
var hostWel = readlineSync.question("what is your name? ");
console.log("welcome " + hostWel)
var userName = readlineSync.question("Do you know jinesh?(yes or no) ")
console.log(userName)
if(userName==="yes"){
console.log("let's play the game")
}else{
  console.log("ok. no worries, Play the game atleast.")
}
function play(question, answer){
var userAnswer = readlineSync.question(question);
console.log(userAnswer)
if(userAnswer === answer){
console.log("you are right")
score=score+1;
}else{
  console.log("you are wrong")
}
console.log("your score is",score)
}

var questions = [{
  question: "Is jinesh an Engineer? ",
  answer: "yes"
},
{
question: "Jinesh's age? ",
answer: "21"
},
{
  question: "jinesh's favourite food? ",
  answer: "pizza"
}]
for(var i=0;i<questions.length; i++){
var gameOn = questions[i];
play(gameOn.question,gameOn.answer)
}
if(score === 3){
  console.log("you know jinesh")
}else{
  console.log("you don't know jinesh properly.")
}

