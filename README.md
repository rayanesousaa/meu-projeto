# meu-projeto 📖

let palavra;

function setup() {
  createCanvas(400, 400);

  palavra = palavraAleatoria();
  
}

function palavraAleatoria() {
  
  let palavras = ["rayane"]
  
  return random(palavras);
}

function inicializaCores() {
  background("rgb(56,128,143)");
  fill("rgb(10,10,10)");
  textSize(64);
  textAlign(CENTER, CENTER);
}

function palavraParcial(minimo, maximo) {
  let quantidade = map(mouseX, minimo, maximo, 1, palavra.length);
  let parcial = palavra.substring(0, quantidade);
  return parcial;
}

function draw() {
  
  inicializaCores();

  let parcial = palavraParcial(0, width);
    
  text(parcial, 200, 200);
  
}
