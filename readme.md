# SPOCK-ROCK game
Juego de piedra, papel o tijera, pero como lo defició Sheldon Cooper: añadiendo dos posibilidades más, lagarto y Spock.
El aprendizaje añadido en este desarrollo es el **uso de módulos**.
Lo que haremos es que cada vez que ganemos, activaremos una animación de "caída de confetti".
El módulo que se encarga de la caida de confetti está en:
[Confetti.js Library](https://www.cssscript.com/confetti-falling-animation/)

##Uso de módulos
[Mozilla - ES Modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
Lecturas adicionales:
[JS Modules History Article](https://www.sitepoint.com/understanding-es6-modules-via-their-history/)

[JS Modules History Github](https://gist.github.com/branneman/558ef3a37ffd58ea004e00db5b201677)

## A tener en cuenta
Usar módulos implica **export** en el módulo e **import** en el fichero .js que lo utiliza.
También implica modificar el elemento script del html añadiendo **type="module"**

<script src="script.js" type="module"></script>

Al hacer esto, el ámbito del script se vuelve local y al utilizar sus funciones dará un error (Por ejemplo, en **onclick="resetAll()"**)

Para solucionarlo, después de la definición de la función, pondremos: 
**window.resetAll = resetAll;**
