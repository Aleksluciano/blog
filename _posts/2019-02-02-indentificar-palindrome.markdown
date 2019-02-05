---
layout: post
title:  "Identificar palindrome"
date:   2019-02-02 20:15:48 -0200
categories: javascript
---

Um palindrome é uma frase ou palavra que pode ser lida da esquerda para direita ou da direita para a esquerda, continuando com o mesmo significado. Exemplo: 'ana', 'reviver', 'asacadadacasa'.

Primeira forma de identificar uma palindrome:

{% highlight javascript %}
function identifica_palindrome (palavra) {

  return palavra.split('').every((letra, i) => {
    return letra === palavra[palavra.length - i - 1];
  });

}

{% endhighlight %}

Segunda forma:

{% highlight javascript %}

function identifica_palindrome (palavra) {

const palavra_invertida = palavra
                         .split('')
                         .reverse()
                         .join('');

   return palavra === palavra_invertida;

 }

{% endhighlight %}

{% highlight javascript %}

let palavra_entrada = 'casa';
let palindrome_valida = identifica_palindrome (palavra_entrada);

console.log(palindrome_valida);

// => 'false'

palavra_entrada = 'reviver';
palindrome_valida = identifica_palindrome (palavra_entrada);

console.log(palindrome_valida);

// => 'true'
{% endhighlight %}
