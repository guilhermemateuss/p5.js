// variaveis da bolinha
let xBolinha = 300;
let yBolinha = 200;
let diametro = 20;
let raio = 10

// velocidade da bolinha
let velocidadex = 5
let velocidadey = 5

// variaveis da  raquete
let xraquete = 5
let yraquete = 200
let raquetecomprimento = 10
let raquetealtura = 90

//variaveis oponente
let xoponente = 590
let yoponente= 200
let velocidadeoponente ;
let colidiu

//placar do jogo
let meuspontos =0
let pontosoponente= 0

// sons do jogo
let raquetada
let ponto
let trilha 

function preload(){
  trilha = loadSound("trilha.mp3")
  ponto = loadSound( "ponto.mp3")
  raquetada = loadSound("raquetada.mp3")
}
function setup() {
    createCanvas(600, 400);
  trilha.loop();
}

function draw(){
    background(0);
    Bolinha();
  velocidade();
  colisaocombordas();
   raquete(xraquete, yraquete);
  movimentoraquete()
  //colisaocomraquete(xraquete , yraquete) 
colisaoraquete(xraquete, yraquete)
  oponente(xoponente, yoponente)
 // movimentooponente()
  colisaoraquete(xoponente, yoponente)
  placar()
  marcaponto()
  multiplay()
  sembug()
}
function Bolinha(){circle(xBolinha, yBolinha, diametro);}

function velocidade(){xBolinha += velocidadex
                     yBolinha += velocidadey }

function colisaocombordas(){  if(xBolinha + raio > width || xBolinha -raio < 0){velocidadex *= -1}
   if(yBolinha + raio > height || yBolinha -raio < 0){velocidadey *= -1}}

function raquete(x, y){rect(x, y, raquetecomprimento, raquetealtura)}

function movimentoraquete(){if(keyIsDown(UP_ARROW)){yraquete += -10}
                          if(keyIsDown(DOWN_ARROW)){yraquete += 10}}
function colisaocomraquete(x, y){
 if(xBolinha - raio < x + raquetecomprimento && yBolinha- raio < y + raquetealtura && yBolinha - + raio > y ) 
  { 
velocidadex *= -1
  }                  
}
function colisaoraquete(x ,y){ colidiu = collideRectCircle(x, y, raquetecomprimento, raquetealtura, xBolinha, yBolinha, raio); if(colidiu)
{velocidadex *= -1}
              raquetada.play()
                                      }
function oponente(x, y){rect(x, y, raquetecomprimento, raquetealtura) }

function movimentooponente(){velocidadeoponente = yBolinha - yoponente - raquetecomprimento/2 - 30;
                            yoponente += velocidadeoponente
                            }

function multiplay(){if(keyIsDown(87)){yoponente += -10}
                         
                    if(keyIsDown(83)){yoponente += 10}}

function placar(){
  stroke(255)
  textSize(16);
  textAlign(CENTER);
  fill(color(255, 140, 0))
  rect(150, 10, 40, 20)
  fill(225)
  text(meuspontos,170, 26)
    fill(color(255, 140, 0))
  rect(450, 10, 40, 20)
    fill(255)
  text(pontosoponente, 470, 26)
}
function marcaponto(){
  if(xBolinha> 590){
    meuspontos += 1
    ponto.play()
  }
  if(xBolinha< 10){
    pontosoponente+=1
    ponto.play()
  }
}
         
function sembug(){
    if (xBolinha - raio < 0){
    XBolinha = 23
    }
}
                              
