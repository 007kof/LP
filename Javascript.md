











<img src = "https://upload.wikimedia.org/wikipedia/commons/9/99/Unofficial_JavaScript_logo_2.svg" alt = "image1" width = "400" />












#### Junjie Ji Chen
#### LP 2018-19 Q2







# Índex

1. Introducció i història

2. Característiques

3. Principals aplicacions

4. Llenguatges similars

5. Exemples de codi

6. Bibliografia




















































# Introducció i història

A causa de la necessitat de crear pàgines web amb contingut dinàmic, va sorgir LiveScript, que va ser creat l'any 1995 pel programador Brendan Eich. Posteriorment LiveScript va adoptar el nom de  JavaScript per motius de màrqueting (ja que en aquella època la paraula Java estava de moda en el món informàtic).  
Actualment JavaScript és un llenguatge molt popular pel desenvolupament de pàgines web, la seva funcionalitat principal és la de poder controlar arxius de multimèdia, imatges, animacions, etc.

# Característiques

**Multiparadigma**  
JavaScript és un llenguatge que combina diferents paradigmes: Imperatiu, funcional i orientat a objectes.

**Interpretat i amb compilació just-in-time**  
JavaScript és un llenguatge interpretat, és a dir, no cal fer el procediment de traduir el codi font a llenguatge màquina (procés de compilació), els navegadors poden llegir directament del codi font. Hi ha navegadors més moderns que tenen la capacitat de fer la compilació just-in-time.

**Sistema de tipus**  
JavaScript és un llenguatge de tipat feble, és a dir, es pot barrejar valors de diferents tipus, per exemple:  
```
let a = 1;
let b = "hello";

writeln(a+b);	// Escriurà "hello1"
```
Com que JavaScript és un llenguatge interpretat, no té gaire sentit parlar si és de type safe, ja que no hi ha una fase de compilació prèvia.

La comprovació de tipus és dinàmica, és a dir, en temps d'execució, i té 6 tipus primitius que son els següents:
```
let num1 = 123;
let num2 = 12.34; // num1 i num2 són de tipus Number
let str1 = "Hola";
let str2 = 'Adeu';
let str3 = `Bon dia`; // str1, str2 i str3 són de tipus String
let bool = true; // bool és de tipus Boolean
let x = null; // x és de tipus Null (No és un punter, null significa un valor buit)
let y; // y és de tipus Undefined (Semblant a Null)
let z1 = Symbol();
let z2 = Symbol("string") // z1 i z2 són de tipus Symbol
let z3 = Symbol() == Symbol(); // Un símbol és un tipus que fa d'identificador, per tant cada símbol és únic, és a dir, z3 sera fals.
```
# Principals aplicacions



# Bibliografia

[Brendan Eich]: https://en.wikipedia.org/wiki/Brendan_Eich
[JavaScript1]: https://es.wikipedia.org/wiki/JavaScript#Caracter%C3%ADsticas
[JavaScript2]: https://developer.mozilla.org/es/docs/Web/JavaScript
[JavaScript3]: https://javascript.info/types
[JavaScript4]: http://www.maestrosdelweb.com/que-es-javascript/
