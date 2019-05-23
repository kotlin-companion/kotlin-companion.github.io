# Porquê Kotlin?

## A linguagem

[Kotlin](https://github.com/JetBrains/kotlin) é uma linguagem de programação open souce, multiplataforma desenvolvida pela [JetBrains](https://www.jetbrains.com) famosa por suas IDEs, ela assim como o Java é compilada para bytecodes que são interpretados pela JVM (Java Virtual Machine). 

Kotlin combina os paradigmas de orientação a objetos e programação funcional. E pode ser 
[compilada para javascript](https://kotlinlang.org/docs/tutorials/javascript/kotlin-to-javascript/kotlin-to-javascript.html), assim como existe também o [Kotlin/Native](https://kotlinlang.org/docs/reference/native-overview.html) da qual permite a criação de binários nativos para sistemas operacionais como: iOS, MacOS, Windows e Linux. E esses binários são execultados sem o uso da JVM.
## Um breve histórico
- **2010**  JetBrains inicia o projeto Kotlin                                             
- **2011**  Durante a JVM Language Submit a JetBrains revela a implementação do Kotlin     
- **2012**  Kotlin foi colocado sob a licença Apache de código aberto.                    
- **2016**  Foi lançada a versão 1.0 a primeira estável da linguagem.                     
- **2017**  No Google I/O foi anunciada como linguagem oficial de desenvolvimento Android.

!!! note " Anuncio de Kotlin como liguagem oficial para Android"

    <iframe width="560" height="315" src="https://www.youtube.com/embed/X1RVYt2QKQE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Características

### Concisa
Pois em relação ao Java temos uma redução significativa na quantidade e legibilidade de código.
Kotlin tem muito menos _boilerplate code_ do que o Java. 

!!! info "Boilerplate code"
    _Boilerplate_ é um termo muito utilizado para se referir a trechos de documentos (por exemplo jurídicos) que são sempre os mesmos, de documento pra documento, de modo que não acrescentam muita coisa mas mesmo assim não podem ser omitidos. Você já deve ter visto em licenças de software, por exemplo, a parte que diz que "NÃO HÁ NENHUMA GARANTIA PARA O PROGRAMA, NO LIMITE PERMITIDO PELA LEI APLICÁVEL. EXCETO QUANDO..." etc. Todo mundo já conhece, ninguém nem lê porque já sabe de cor o que está escrito, mas o documento não estaria completo sem ela.

Exemplo, imagine uma classe chamada livro com apenas dois atributos, autor e título, em Java ela ficaria assim:

<script src="https://gist.github.com/leoallvez/80581e58a4441069c59649d13a939cdc.js"></script>
Já em Kotlin a mesma a classe seria implementada da seguinte forma:
<script src="https://gist.github.com/leoallvez/444da6496884b0f8c511e2424abd20bb.js"></script>


!!! info "Observação"
    Em um primeiro momento, pode parecer que os métodos getters e setters não existem na classe livro, mas na verdade eles estão implícito na mesma.

###Segura de referência nulas

Em Kotlin por default todo objeto e variável **não pode** ter valor nulo.
<script src="https://gist.github.com/leoallvez/2e319fee0eda4570550aa4951785ccf6.js"></script>

Kotlin protege você de operar incorretamente em tipos nullable.
<script src="https://gist.github.com/leoallvez/3e4a97359c2f6a1e0bab37c183c4378e.js"></script>

Podemos usar uma chamada segura (safe call) que impede o um erro de referência nula(NullPointerException).
<script src="https://gist.github.com/leoallvez/46a2e6e41b764eed1898742bd53b0683.js"></script>
Apesar de a váriavel **sobreNome** ser nula, não havera um erro ao chamar a propriedade **lenght**.

!!! note "Nota"
    Um NullPointerException é uma exceção lançada quando um programa tenta acessar uma variável ou objeto de memória que não foi instanciado (ou melhor, inicializado) até o momento de sua chamada. Ou seja, o objeto ainda está nulo e não tem um valor definido.	

###Interoperável
Kotlin é 100% interoperável com o Java. Isso significa que podemos usar qualquer classe ou API que foi implementada em Java sem o menor problema.
Isso é graças ao fato do Kotlin gerar os mesmos bytescodes da JVM Java.

<script src="https://gist.github.com/leoallvez/247eacc9965a72e10c359b1e7e5d85b5.js"></script>

Podemos então ter uma instância da classe **Carro.java** no código Kotin.
<script src="https://gist.github.com/leoallvez/851e201fc6f7fe0ea308f9aba86d6839.js"></script>
![Suprise](images/suprise.jpg)
**Mágia pura!**