# Porquê Kotlin?

## A linguagem

Kotlin é uma linguagem de programação [Open Souce](https://github.com/JetBrains/kotlin), multiplataforma desenvolvida pela [JetBrains](https://www.jetbrains.com) famosa por suas IDEs, e assim como o Java é compilada para bytecodes que são interpretados pela JVM (Java Virtual Machine). 

Kotlin combina os paradigmas de orientação a objetos e de programação funcional. Pode ser 
[compilada para javascript](https://kotlinlang.org/docs/tutorials/javascript/kotlin-to-javascript/kotlin-to-javascript.html), assim com também existe o [Kotlin/Native](https://kotlinlang.org/docs/reference/native-overview.html) que permite criar binários nativos para o sistema operaciona alvo que são execultados sem o uso de maquina virtual.
## Um breve histórico

| Ano      | Acontecimentos                                                                |
| ---------| :-----------------------------------------------------------------------------|
| **2010** | JetBrains inicia o projeto Kotlin                                             |
| **2011** | Durante a JVM Language Submit a JetBrains revela a implenetação do Kotlin     |
| **2012** | Kotlin foi colocado sob a licença Apache de código aberto.                    |
| **2016** | Foi lançada a versão 1.0 a primeira estável da linguagem.                     |
| **2017** | No Google I/O foi anunciada como linguagem oficial de desenvolvimento Android.|

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
    Num primeiro momento parece que aos métodos getters e setters não existem na classe, quando na verdade eles estão implicitos na mesma..

<script src="https://gist.github.com/leoallvez/e2573f158dbde4b57688ced61434962b.js"></script>

###Segura

###Interoperável
Além disso ela é  totalmente focada em interoperabilidade com o java. Isso significa que podemos mistura java com Kotlin sem nenhum problema.
Kotlin gera os mesmo bytescodes da JVM Java.