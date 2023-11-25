<p align="center"> <a href="variaveis_3.md"> << Contando inteiro </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_5.md"> Próximo >> </a> </p>

# Char

Continuando nossos exemplos com os tipos, apresentamos o tipo ``signed char``:

```c
#include <stdio.h>

int	main(void)
{
	signed char	variavel;

	variavel = 76;
	printf("A letra da vez é %c\n", variavel);
	return (0);
}
```

[Como foi dito antes](../1_printf/printf_3.md), nos exemplos da printf, o char na verdade é um número convertido para caractere.

Nós vemos letra porque o printf fez a conversão pra gente.

Se pedirmos para ver um inteiro com o valor que existe em um signed char, vemos:

```c
#include <stdio.h>

int	main(void)
{
	signed char	variavel;

	variavel = 76;
	printf("A letra da vez é %d\n", variavel);
	return (0);
}
```

- **Se é assim, por que não deixar apenas as variáveis do tipo int e pronto?**

Em questão de economia de memória, faz toda a diferença você ter uma variável que tem o menor tamanho possível. Esse é o caso do nosso tipo ``signed char``. Ele tem o menor tamanho (1 byte) e é o tipo que cabe menos números nele.

Variáveis de tipo ``signed char`` podem receber valores que vão de -128 até 127.

Serve perfeitamente para imprimir caracteres na tela, pois cada letra individual terá o tamanho de 1 byte.

Lembrando que  as letras serão impressas conforme a tabela ASCII, o ``%c`` do printf respeita isso.

Os números negativos, por exemplo, não serão impressos como algo que nós vamos entender.

Veja o exemplo:

<exemplo de impressão com a variável recebendo o valor -1>

Caso você queira ver uma letra, respeite a tabela ASCII. Caso queira usar apenas os números. O intervalo é o que foi citado antes.

Com a parte de ``signed char`` finalizada, partimos para os tipo ``unsigned``.

<p align="center"> <a href="variaveis_3.md"> << Inteiros! </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_5.md"> Joga o unsigned no peito do pai >> </a> </p>
