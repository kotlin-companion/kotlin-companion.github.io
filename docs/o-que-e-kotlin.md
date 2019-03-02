#O que é Koltin?
##Origem
É a linguagem de programação Open Souce criada pelo JetBrains, que roda em cima da JVM do Java.
#Principais Características
##Concisa
É concisa, pois em relação ao Java temos uma redução significativa na quantidade de código.
Exemplo, imagine uma classe chamada livro com apenas dois atributos, autor e título, em Java ela ficaria assim:
<script src="https://gist.github.com/leoallvez/80581e58a4441069c59649d13a939cdc.js"></script>
Já em Kotlin a mesma a classe seria implementada da seguinte forma:
<script src="https://gist.github.com/leoallvez/444da6496884b0f8c511e2424abd20bb.js"></script>

Num primeiro momento parece que aos métodos getters e setters não existem na classe, quando na verdade eles estão implicitos na mesma.
<script src="https://gist.github.com/leoallvez/e2573f158dbde4b57688ced61434962b.js"></script>

##Interoperável
Além disso ela é  totalmente focada em interoperabilidade com o java. Isso significa que podemos mistura java com Kotlin sem nenhum problema.
Kotlin gera os mesmo bytescodes da JVM Java.