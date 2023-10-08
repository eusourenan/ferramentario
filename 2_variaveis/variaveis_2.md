# Inteiros

Tal como no exemplo anterior, o tipo inteiro é o mais rápido de ser entendido.

```c
#include <stdio.h>

int	main(void)
{
	signed int	variavel;

	variavel = 42;
	printf("A resposta é %d\n", variavel);
	return (0);
}
```

Variáveis do tipo int podem receber números que vão de -2147483648 até 2147483647.

Esse número está na casa dos bilhões, veja com os pontos: 2.147.483.647. Imagina isso de dinheiro!

Assim como nos exemplos da printf, nós podemos usar várias vezes o ``%d`` e a variável.

<exemplo com a variável replicada várias vezes>

Operações também são válidas.

<Exemplo com operações matemáticas>

### Mas, e se eu quiser um número maior?

A solução são as variáveis do tipo long.

# Long

Variáveis do tipo ``long`` são idênticas às variáveis do tipo ``int`` com pequenas diferenças. Veja:

```c
#include <stdio.h>

int	main(void)
{
	signed long	variavel;

	variavel = 42;
	printf("A resposta é %ld\n", variavel);
	return (0);
}
```

- Usamos ``%ld`` ao invés de ter apenas a letra 'd'.
- Os números long tem o intervalo que vai de -9223372036854775807 até 9223372036854775807.

Se antes 2 bilhões estava bom, imagina ter 9 quintilhões na conta bancária! Veja com os pontos: 9.223.372.036.854.775.807. Eita número grande!