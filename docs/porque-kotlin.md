# Porquê Kotlin?

## A linguagem

Kotlin é uma linguagem de programação [Open Souce](https://github.com/JetBrains/kotlin), multiplataforma desenvolvida pela [JetBrains](https://www.jetbrains.com) famosa por suas IDEs, assim como o Java é compilada para bytecodes que são interpretados pela JVM (Java Virtual Machine). 

Kotlin combina os paradigmas de orientação a objetos e de programação funcional. Pode ser 
[compilada para javascript](https://kotlinlang.org/docs/tutorials/javascript/kotlin-to-javascript/kotlin-to-javascript.html), assim com também existe o [Kotlin/Native](https://kotlinlang.org/docs/reference/native-overview.html) que permite criar binários nativos para o sistema operaciona alvo que são execultados sem o uso de maquina virtual.
## Um breve histórico


- **2010**  JetBrains inicia o projeto Kotlin                                             
- **2011**  Durante a JVM Language Submit a JetBrains revela a implenetação do Kotlin     
- **2012**  Kotlin foi colocado sob a licença Apache de código aberto.                    
- **2016**  Foi lançada a versão 1.0 a primeira estável da linguagem.                     
- **2017**  No Google I/O foi anunciada como linguagem oficial de desenvolvimento Android.

!!! note " Anuncio de Kotlin como liguagem oficial para Android"

    <iframe width="560" height="315" src="https://www.youtube.com/embed/X1RVYt2QKQE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Características

### Concisa
É concisa, pois em relação ao Java temos uma redução significativa na quantidade de código.
Exemplo, imagine uma classe chamada livro com apenas dois atributos, autor e título, em Java ela ficaria assim:

<script src="https://gist.github.com/leoallvez/80581e58a4441069c59649d13a939cdc.js"></script>
Já em Kotlin a mesma a classe seria implementada da seguinte forma:
<script src="https://gist.github.com/leoallvez/444da6496884b0f8c511e2424abd20bb.js"></script>


!!! info "Observação"
    Num primeiro momento parece que aos métodos getters e setters não existem na classe, quando na verdade eles estão implicitos na mesma.

###Segura de referência nulas

Em Kotlin por default todo objeto e variável **não pode** ter valor nulo.
<script src="https://gist.github.com/leoallvez/2e319fee0eda4570550aa4951785ccf6.js"></script>

Kotlin protege você de operar incorretamente em tipos nullable.
<script src="https://gist.github.com/leoallvez/3e4a97359c2f6a1e0bab37c183c4378e.js"></script>

Podemos usar uma chamada segura (safe call) que impede o um erro de referência nula(NullPointerException).
<script src="https://gist.github.com/leoallvez/46a2e6e41b764eed1898742bd53b0683.js"></script>
Apesar de a váriavel **sobreNome** ser nula, não havera um erro ao chamar a propriedade **lenght**.

!!! note "Nota"
    Um NullPointerException é uma exceção lançada quando um programa tenta acessar uma variável ou objeto de memória que não foi instanciado (ou melhor, inicializado) até o momento de sua chamada. Ou seja o objeto ainda está nulo e não tem um valor definido.

###Interoperável
Kotlin é 100% interoperal com o java. Isso significa que podemos usar qualquer Classe ou API implementada em Java sem nenhum problema.
Isso é graças ao fato do Kotlin gerar os mesmo bytescodes da JVM Java.

<script src="https://gist.github.com/leoallvez/247eacc9965a72e10c359b1e7e5d85b5.js"></script>

Podemos então ter uma instância da classe **Carro.java** no código Kotin.
<script src="https://gist.github.com/leoallvez/851e201fc6f7fe0ea308f9aba86d6839.js"></script>
![Suprise](images/suprise.jpg)
**Mágia pura!**