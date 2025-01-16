# functional-programming

# **Programação Funcional**
Este repositório possui um resumo sobre os principais métodos e conceitos relacionados à Programação Funcional em JavaScript. Esses métodos são amplamente utilizados para manipulação de arrays e representam abordagens declarativas que tornam o código mais limpo, legível e eficiente.

A programação funcional é um paradigma que trata funções como "cidadãos de primeira classe", promovendo a utilização de funções puras, imutabilidade de dados e operações baseadas em composição. Aqui, destacamos métodos essenciais que exemplificam esses princípios, como .map(), .filter(), .reduce(), entre outros.

Explore o conteúdo e veja como esses métodos podem simplificar e transformar seu código! 🚀


## **.indexOf()**

Verifica se o elemento buscado está presente no array.
- Caso encontrar: retorna a posição do elemento
- Caso não encontrar: retorna **-1**

```javascript
let frutas = ["banana", "maca", "uva"];

console.log(frutas.indexOf(("uva"))
//output = 2

console.log(frutas.indexOf(("goiaba"))
//output = -1
```

## **.map()**
Aplica uma função a cada elemento da coleção, retornando uma nova coleção com os elementos alterados

```javascript
let list = [1, 2, 3, 4];
let m3 = list.map(x => 2 * x);
console.log(m3)
// output: 2, 4, 6, 8
```


## **.sort()**
Ordena a coleção conforme a função de comparação informada como parâmetro

```javascript
let nomes = ['MARIA', 'JOAO', 'ANABELA'];

function comparacaoPorTamanho(s1 ,s2) {
   return s1.length - s2.length;
}

let s1 = nomes.sort(comparacaoPorTamanho);
console.log(s1);
// output: [ 'JOAO', 'MARIA', 'ANABELA' ]

let s2 = nomes.sort();
console.log(s2);
// output: [ 'ANABELA', 'JOAO', 'MARIA' ]
```


## **.filter()**
Retorna uma nova coleção, contendo apenas os elementos que satisfazem uma restrição
```javascript
let users = [
  { name: "clóvis", id: 1, active: true },
  { name: "silva", id: 2, active: false },
  { name: "neto", id: 3, active: true },
]

let t = users.filter(x => x.active == true)
console.log(t)
//output = [
//  { name: 'clóvis', id: 1, active: true },
//  { name: 'neto', id: 3, active: true }
//]
```

## **.reduce()**
Aplica uma função cumulativa aos elementos de uma coleção, retornando o resultado final.

```javascript
function produto(x : number, y : number) : number {
    return x * y;
}
let r1 = list1.reduce(soma);
let r2 = list1.reduce(produto);
```


Ex2: - Exiba no console quantos números abaixo de 501 o array abaixo possui.
```javascript
const crazyNumbers = [937, 5, 395, 402, 501, 333, 502, 781, 3]
let t = crazyNumbers.reduce((counter, crazyNumber)=>{
    return crazyNumber < 501 ? counter+1: counter
},0)
console.log(t)
```

Obs: o segundo argumento da função callback do reduce (0) é o valor inicial do acumulador.


