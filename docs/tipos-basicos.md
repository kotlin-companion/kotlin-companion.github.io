Em Kotlin, tudo é objeto no sentido de que qualquer variável possui propriedades e métodos. 
Nesta seção, descrevemos os tipos básicos usados ​​no Kotlin: números, caracteres, booleanos, matrizes e strings.
###Números
Kotlin manipula os números de maneira muito semelhante a do Java, e possuem tamanhos limitados, esses limites dependem da quantidade de bits que cada tipo númerico oculpa em memória.
O Kotlin fornece os seguintes tipos que representam números:

|Tipo    |Bit|Valor Mínimo        |Valor Máximo        |
| -------|:--|:-------------------|:-------------------|
| Long   |64 |-9223372036854775808|9223372036854775807 |
| Int    |32 |-2147483648         |2147483647          |
| Short  |16 |-32768              |32767               |
| Byte   |8  |-128                |127                 |

Os números de ponto flutuante vêm em dois tipos, dependendo de quantos dígitos você precisa. Se você precisar de maior precisão ou trabalhar com quantias monetárias (ou outras situações em que você deve ter resultados exatos), use o tipo não primitivo BigDecimal.

|Tipo    |Bit| Quantidade de dígitos         |
| -------|:--|:------------------------------|
| Double |64 | 16-17                         |
| Float  |32 | 6-7                           |


####Underline
Podemos usar _underline_ para tornar os valores numéricos mais legíveis.
<script src="https://gist.github.com/leoallvez/4d84fe66d410e68837efc59788580599.js"></script>

####Conversões
Tipos menores não são subtipos de maiores. Se eles fossem, teríamos o seguinte problema.
<script src="https://gist.github.com/leoallvez/9b7da06626f26ab07fa9bd9a67451888.js"></script>
Tipo menores **não** são implicitamente convertidos em tipos maiores. Isso significa que não podemos atribuir um valor do tipo Byte a uma variável Int sem uma conversão explícita.
<script src="https://gist.github.com/leoallvez/27f10bf96729fa931c9385dc15b4f165.js"></script>
Podemos usar conversões explícitas para ampliar os números
<script src="https://gist.github.com/leoallvez/4a11f3e3f1e16e4dc0a25136cd157f32.js"></script>

Cada tipo de númerico suporta os seguintes os metódos conversão.

- toByte (): Byte
- toShort (): Short
- toInt (): Int
- toLong (): Long
- toFloat (): Float
- toDouble (): Double
- toChar (): Char

###Char
Char não podem ser tratados diretamente como números.
<script src="https://gist.github.com/leoallvez/d99b56c8cffc250e7d6bc756c0f35375.js"></script>
Porém, podemos converter explicitamente um char em um número inteiro.
<script src="https://gist.github.com/leoallvez/1fc5e1bd9587752f31ea7400d494d673.js"></script>
<!--
Em Kotlin, o sistema de tipos distingue entre referências que podem conter nulas ou não. Uma variável ou propriedade não podem conter valor nulo por default.
<script src="https://gist.github.com/leoallvez/c52359fabad8c240a9a1f9c836b150c3.js"></script>
Para permitir valores nulos, nós devemos declarar a variável como _nullable_ explicitamente.
<script src="https://gist.github.com/leoallvez/ee132bc32f439d665c27e48e987dfe18.js"></script>
-->
###Booleans
Tipos booleanos são definidos como Boolean, e podem ter apenas dois valores true (verdadeiro) ou false(falso) da qual podemos execultar as seguintes operações lógicas.

####Operações lógicas

|Operação|Operador|
| -------|:-------|
| E      | &&     |
| OU     | II     |
| Não    | !      |

####Métodos da classe Boolean.
A classe Boolean possui métodos para essas operações, o que tornam a sintax mais legível.
<script src="https://gist.github.com/leoallvez/ca7aa4a97250c8d1a141d58ccd0da68e.js"></script>

###Arrays

###Strings
Strings são comparadas com o operador **==** que verificar a sua igualdade estrutural.
<script src="https://gist.github.com/leoallvez/fa6ac27dccd28c0ae83fc9bbd35620c3.js"></script>
Já o operador **===** verifica igualdade referencial e **!==** é a sua contra parte de negação.

!!! note "Nota"
    Somente se a **===** b só será avaliado como **true** somente se **a** e **b** apontarem para o mesmo objeto em memória.

<script src="https://gist.github.com/leoallvez/5c3586b5a45e6e03c117250133a80f1e.js"></script>

!!! note "Nota"
    Para valores que são representados como tipos primitivos no tempo de execução (por exemplo, o tipo Int), a verificação da igualdade **===** é equivalente à verificação **==** de verificação.

Strings são um conjutos de caracteres que podem ser acessados ​​por index.
<script src="https://gist.github.com/leoallvez/0667ee05a395e270e3698d58ba36398c.js"></script>
Os elementos de uma string podem ser iterados em um loop.
<script src="https://gist.github.com/leoallvez/a931f839e7c191d1540bd3817d0918ac.js"></script>
Template é um pedaço de código que é avaliado e seu resultado é concatenado em uma string. 
Começa com um sinal de dólar **$** e consiste em um nome variável.
<script src="https://gist.github.com/leoallvez/ec02fabc2f4b5012fa6c0bdb629d9a47.js"></script> 
Para acessar valores de propriedade ou métodos de objetos devemos usar chaves.
<script src="https://gist.github.com/leoallvez/2b37c9facb9a705f8a4fa51b6db16af8.js"></script>


