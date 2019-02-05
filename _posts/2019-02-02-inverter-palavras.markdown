---
layout: post
title:  "Inverter palavras"
date:   2019-02-02 20:15:48 -0200
categories: javascript
---
Primeira forma de inverter uma palavra:

{% highlight javascript %}
function inverte_palavra (palavra) {

  return palavra
         .split('')  // transforma a string str em uma array ['c','a','s','a']
         .reverse()  // inverte a array ['a','s','a','c']
         .join('');  // transforma a array em uma string 'asac'


}


{% endhighlight %}

Segunda forma:

{% highlight javascript %}

 function inverte_palavra (palavra) {

   let palavra_invertida = '';

   for (let letra of palavra) {
     palavra_invertida = letra + palavra_invertida;
   }

   return palavra_invertida;

 }

{% endhighlight %}

Terceira forma:

{% highlight javascript %}

function inverte_palavra (palavra) {

  return palavra
         .split('')
         .reduce((palavra_invertida, letra) => letra + palavra_invertida, '');

}

{% endhighlight %}

{% highlight javascript %}

let palavra_entrada = 'casa';
let palavra_saida  = inverte_palavra(palavra_entrada);

console.log(palavra_saida);

// => 'asac'
{% endhighlight %}

