# Conjugador.js

> Um conjugador de verbos da língua portuguesa.

## Características

* Aceita verbos irregulares.
* Não requer conexão com a *internet*.

Um utilitário para conjugar qualquer verbo da língua portuguesa, regular ou irregular, nos seis tempos modo indicativo (presente, pretérito imperfeito, pretérito perfeito, pretérito mais que perfeito, futuro do presente e futuro do pretérito).

## Instalação

Com [`npm`](https://npmjs.com/):

```
npm install --save conjugador
```

## Uso

Importe-o com:

```js
var conjugar = require("conjugador");
```

### Sintaxe

```js
conjugar([verbbo])
```

#### Parâmetros

- `verbo` ― Um verbo qualquer (regular ou irregular).

#### Retorno

Retorna um objeto com as conjugações do verbo onde o valor de cada propriedade é uma *array* com a conjugação em todas as pessoas do singular e do plural.

As propriedades retornadas são:

* `presente` ― Presente.
* `preteritoImperfeito` ―  Pretérito Imperfeito.
* `preteritoPerfeito` ―  Pretérito Perfeito.
* `preteritoMaisQuePerfeito` ― Pretérito Mais-que-perfeito.
* `futuroDoPresente` ― Futuro do Presente.
* `futuroDoPreterito` ― Futuro do Pretérito.

## Exemplo

Um exemplo para obter a conjugação do verbo *amar* no presente.

```js
var conjugar = require("conjugador");

conjugar("amar").presente;
// [ "amo",
//   "amas",
//   "ama",
//   "amamos",
//   "amais",
//   "amam" ]
```

## Como Funciona?

Os verbos regulares são conjugados a partir de um algoritmo, enquanto os irregulares com ajuda de uma lista pronta com mais de 163 verbos mais conhecidos. Não é exigido que o verbo seja "oficial", bastando ser conjugável, portanto também é possível conjugar verbos como *twittar*, *forkar*, *photoshopar*, etc.

## Licença

MIT
