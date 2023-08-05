# Instruções:

Faça um código, utilizando o Google Blockly, que execute a contagem regressiva de uma bomba, informando o número de segundos para explodir. Ele deverá mostrar a mensagem “iniciando contagem regressiva”, os segundos passados e, no final, a mensagem “BUM!”.

# Resolução:

<img src='bum.png'>

- Link para acessar ao blockly - https://blockly-demo.appspot.com/static/demos/code/index.html?lang=pt-br

# Código em javascript:

```
var inicio, contador;

function mathRandomInt(a, b) {
  if (a > b) {
    // Swap a and b to ensure a is smaller.
    var c = a;
    a = b;
    b = c;
  }
  return Math.floor(Math.random() * (b - a + 1) + a);
}


inicio = mathRandomInt(5, 20);
contador = inicio;
window.alert('Iniciando a contagem regressiva: ');
for (var count = 0; count < inicio; count++) {
  window.alert(['A bomba vai exploidir em:',contador,'Segundos...'].join(''));
  contador = contador - 1;
}
window.alert('Bum...');



```