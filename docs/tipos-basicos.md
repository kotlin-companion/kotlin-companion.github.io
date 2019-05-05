Em Kotlin, o sistema de tipos distingue entre referências que podem conter nulas e as que não podem. Uma variável ou propriedade não podem conter valor nulo por default:
<script src="https://gist.github.com/leoallvez/c52359fabad8c240a9a1f9c836b150c3.js"></script>
Para permitir valores nulos, devemos declarar uma variável como **nullable** de forma explicita:
<script src="https://gist.github.com/leoallvez/ee132bc32f439d665c27e48e987dfe18.js"></script>

###Strings
Em Kotlin strings são comparadas com o operador **==** que verificar a sua igualdade estrutural.
<script src="https://gist.github.com/leoallvez/fa6ac27dccd28c0ae83fc9bbd35620c3.js"></script>
Já o operador **===** verifica igualdade referencial e **!==** é a sua contra parte de negação.

!!! note "Nota"
    Somente se a **===** b só será avaliado como **true** somente se **a** e **b** apontarem para o mesmo objeto.

<script src="https://gist.github.com/leoallvez/5c3586b5a45e6e03c117250133a80f1e.js"></script>

!!! note "Nota"
    Para valores que são representados como tipos primitivos no tempo de execução (por exemplo, o tipo Int), a verificação da igualdade **===** é equivalente à verificação **==** de verificação.

 Assim como em outras linguagens strings são um conjutos de caracteres que podem ser acessados ​​por index.
<script src="https://gist.github.com/leoallvez/0667ee05a395e270e3698d58ba36398c.js"></script>
Os elementos de uma string podem ser iterados com um loop.
<script src="https://gist.github.com/leoallvez/a931f839e7c191d1540bd3817d0918ac.js"></script>
Template é um pedaço de código que é avaliado e seu resultado é concatenado em uma string. 
Começa com um sinal de dólar **$** e consiste em um nome variável:
<script src="https://gist.github.com/leoallvez/ec02fabc2f4b5012fa6c0bdb629d9a47.js"></script> 
Para acessar valores de propriedade ou métodos de objetos devemos usar chaves:
<script src="https://gist.github.com/leoallvez/2b37c9facb9a705f8a4fa51b6db16af8.js"></script>

| Ano      | Acontecimentos                                                                |
| ---------| :-----------------------------------------------------------------------------|
| **2010** | JetBrains inicia o projeto Kotlin                                             |
| **2011** | Durante a JVM Language Submit a JetBrains revela a implenetação do Kotlin     |
| **2012** | Kotlin foi colocado sob a licença Apache de código aberto.                    |
| **2016** | Foi lançada a versão 1.0 a primeira estável da linguagem.                     |
| **2017** | No Google I/O foi anunciada como linguagem oficial de desenvolvimento Android.|
