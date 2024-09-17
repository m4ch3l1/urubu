# urubu
function setup() {
   createCanvas(400, 400);
}
let xBolinha = 200;
 let yBolinha = 200;
 let diametro = 10;
 let velocidadeXBolinha = 5;
 let velocidadeYBolinha = 3;

 function draw() {
   background(0);
  circle(xBolinha, yBolinha, diametro);
   xBolinha += velocidadeXBolinha;
   yBolinha += velocidadeYBolinha;
 } 
let xBolinha = 300;
let yBolinha = 200;
let diametro = 15;
let raio = diametro /2;
if (xBolinha + raio > width || xBolinha - raio < 0) {
    velocidadeXBolinha *= -1;
}
if (yBolinha + raio > height || yBolinha - raio < 0) {
    velocidadeYBolinha *= -1;
}
function draw() {
    background(0);
    mostraBolinha();
    movimentaBolinha();
    verificaColisaoBorda();
}

function mostraBolinha() {
    circle(xBolinha, yBolinha, diametro)
}

function movimentaBolinha() {
    xBolinha += velocidadeXBolinha;
    yBolinha += velocidadeYBolinha;
}

function verificaColisaoBorda() {
    if (xBolinha + raio > width || xBolinha - raio < 0) {
        velocidadeXBolinha *= -1;
    }
    if (yBolinha + raio > height || yBolinha - raio < 0) {
        velocidadeYBolinha *= -1;
    }
}
//variáveis da bolinha
let xBolinha = 300;
let yBolinha = 200;
let diametro = 15;
let raio = diametro / 2;

//velocidade da bolinha
let velocidadeXBolinha = 6;
let velocidadeYBolinha = 6;
function draw() {
  background(0); //1 - Desenha o background 
  mostraBolinha(); // 2 - Desenha a bolinha
  movimentaBolinha(); // 3 - Movimenta a Bolinha
  verificaColisaoBorda(); // 4 - Verifica Colisão da bolinha
 
 // 5- Volta para o início da função draw()
}
