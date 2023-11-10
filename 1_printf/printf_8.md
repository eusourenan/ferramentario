<p align="center"> <a href="printf_7.md"> << Sem sinalizadores </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="../2_variaveis/variaveis_1.md"> Próximo Tipo >> </a> </p>

# Long
### <center>Superando os limites marcados... (com novos limites)</center>

Como vimos antes, os intervalos dos números são grandes, mas vem a dúvida: e se quisermos números maiores?

A alternativa foi a criação do tipo ``long``.

``Long`` é a mesma coisa que um inteiro, só que cabe mais números.

Em vez de ter o intervalo dos inteiros:
- -2.147.483.648 até 2.147.483.647

Ele tem um intervalo diferente:
- -9.223.372.036.854.775.808 até +9.223.372.036.854.775.807

Isso são nove quintilhões (imagina isso de dinheiro na conta)!

Como isso é possível? É mais simples do que você imagina.

Um inteiro (%d) tem uma memória de 4 bytes no computador. Um ``long`` tem o dobro da memória, 8 bytes.

Separar a memória assim, já permitiu expandir o número e muito. Mas, como dá pra perceber, não é infinito, é apenas um limite beeeeeeem maior para os números que podemos representar.

Como foi dito antes, o long é apenas um inteiro, só que mais longo. Por isso, o printf usa ``%ld`` para representar os números do tipo ``long``. Vamos de exemplo:

```c
#include <stdio.h>

int	main(void)
{
	printf("Printando um número long: %ld\n", 42);
	return (0);
}
```

Uaaaaaaau! Que número gigantesco eu coloquei aqui, não é mesmo?!

Ah! Neste ponto de evolução, você já consegue entender os valores que podem ou não ser colocados ali. Confio em ti no fundo do meu coração. :orange_heart:

Pense em ``%ld`` como abreviação de ``long digit``.

# Double
### <center>É tipo um long, mas pra floats</center>

O subtítulo já explica bem o rolê. Literalmente o ``double`` é um meio de fazer o float, só que mais longo.

O nome ``double`` vem porque ele tem o dobro do tamanho do float. ([Tem um meio mais obscuro que esconde a verdade](https://stackoverflow.com/questions/399114/why-are-c-c-floating-point-types-so-oddly-named)), mas ficarei com a versão mais bonita. É porque ele tem o dobro de memória.

Veja um exemplo de uso:

```c
#include <stdio.h>

int	main(void)
{
	printf("Printando um número double: %lf\n", 42);
	return (0);
}
```
O ``%lf`` pode ser interpretado como ``long float``. O que representa bem o tipo numérico que queremos representar.

# Long Double
### <center>Porque temos que mesclar todas as palavras</center>

Gostaria de fazer uma última apresentação de tipos o ``long double``. Ele tem o dobro do que o double tem de representação. Sim, ele é beeeeeem grande.


Exemplo:
```c
#include <stdio.h>

int	main(void)
{
	printf("É... é um número bem grande: %LF\n", 42);
	return (0);
}
```

O 'L' (maiúsculo) indica pro printf que queremos o maioral dos tipos flutuantes. A letra 'f' pode ser minúscula, ou maiúscula que ele entende.

Tem o intervalo...

# Finalização

O long também tem um jeito de printar ``unsigned``. Para isso, usamos ``%lu``.

O intervalo que alcança vai de 0 até 18.446.744.073.709.551.615 (18 quintilhões). Nesta altura do campeonato, já posso deixar os testes com sua pessoa. :heart:

Números dos tipos ``float``, ``double`` e ``long double`` não podem ser ``unsigned``. Quem construiu a linguagem sabe o porquê disso. Infelizmente, eu não sei. (T.T)

Para compensar esse desconhecimento, passamos para as cenas dos próximos episódios. Neles, irei contar como usar ``variáveis``. Uma coisa que vai te acompanhar e muito nos seus dias de código. 

Vem comigo, se alegre, bora cantar uma música aleatória e aprender mais sobre o que a linguagem C nos proporciona.

Se quiser mais informações de como o printf funciona clique [aqui](https://www.man7.org/linux/man-pages/man3/printf.3.html).

<p align="center"> <a href="printf_7.md"> << Sem sinalizadores </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="../2_variaveis/variaveis_1.md"> Hora das variáveis >> </a> </p>