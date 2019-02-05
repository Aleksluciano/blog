---
layout: post
title:  "Notas em Javascript"
date:   2019-02-01 20:15:48 -0200
categories: javascript
---

*for of => array, for in => objeto*
{% highlight javascript %}

let letrasArray = ['a', 'b', 'c'];

//iteração em array
for ( let elemento of letrasArray ){
      console.log(elemento) //=> a
                            //   b
                            //   c
    }

let letrasMap = { a:1, b:2, c:3 };

//iteração em objeto
for ( let elemento in letrasMap ){

      console.log(elemento) //=> a
                            //   b
                            //   c

    }

 for ( let elemento in letrasMap ){

      console.log(letrasMap[elemento]) //=> 1
                                       //   2
                                       //   3
    }   
   




{% endhighlight %}

*reduce*
{% highlight javascript %}
let numeros = [1,2,3,4,5];
let total = numeros.reduce((soma,elemento) => soma + elemento)
console.log(total) //=> 15
{% endhighlight %}

*every* => testa se todas as condições são verdadeiras
{% highlight javascript %}
let numeros = [1,2,3,4,5];
let todos_igual_3 = numeros.every((elemento) => elemento == 3)
console.log(todos_igual_3) //=> false

numeros = [3,3,3,3,3];
todos_igual_3 = numeros.every((elemento) => elemento == 3)
console.log(todos_igual_3) //=> true
{% endhighlight %}

*some* => testa se alguma condição é verdadeira
{% highlight javascript %}
let numeros = [1,2,3,4,5];
let algum_igual_3 = numeros.some((elemento) => elemento == 3)
console.log(algum_igual_3) //=> true

numeros = [1,2,2,4,5];
algum_igual_3 = numeros.some((elemento) => elemento == 3)
console.log(algum_igual_3) //=> false
{% endhighlight %}

