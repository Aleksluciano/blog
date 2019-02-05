---
layout: post
title:  "Contar letras"
date:   2019-02-02 20:15:48 -0200
categories: javascript
---

Vamos contar o número de vezes que uma letra existe em uma palavra ou sentença. A letra que for mais utilizada, será retornada pela função.

{% highlight javascript %}
function letra_mais_utilizada(frase) {
  
  const letraMap = {};
  let mais_vezes = 0;
  let letra_mais_utilizada = '';

  for (let letra of frase) {

    if (letraMap[letra]) {
      letraMap[letra]++;
    } else {
      letraMap[letra] = 1;
    }

  }

  for (let letra in letraMap) {

    if (letraMap[letra] > mais_vezes) {
      mais_vezes = letraMap[letra];
      letra_mais_utilizada = letra;
    }
    
  }

  return letra_mais_utilizada;
}

let frase_entrada = 'o bebe baba no boi';
let letra  = letra_mais_utilizada(frase_entrada);

console.log(letra);

// => b
{% endhighlight %}

 No fim da função letraMap ficará assim:

      { o: 3, 
       ' ': 4, 
       b: 5, 
       e: 2, 
       a: 2, 
       n: 1, 
       i: 1 }

 b será retornado porque occorre mais vezes

