---
layout: post
title:  "Inverter inteiro"
date:   2019-02-02 20:15:48 -0200
categories: javascript
---

Ini

{% highlight javascript %}

function inverte_inteiro (n) {

const inteiro_string =  n
                        .toString()
                        .split('')
                        .reverse()
                        .join('');

  return parseInt(inteiro_string) * Math.sign(n); 
  // Math.sign retorna -1 se o número é negativo e 1 se for positivo

}


let numero_entrada = -534;
let numero_saida  = inverte_inteiro(numero_entrada);

console.log(numero_saida);

// => -435

{% endhighlight %}

