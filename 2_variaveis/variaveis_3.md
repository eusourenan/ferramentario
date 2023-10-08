# Char

Segue o mesmo padrão de declaração: tipo da váriável, nome da variável.

```c
#include <stdio.h>

int	main(void)
{
	signed char	variavel;

	variavel = 'L';
	printf("A letra da vez é %c\n", variavel);
	return (0);
}
```

Como foi dito antes, nos exemplos da printf, o char é um número convertido para caractere.

Variáveis de tipo ``signed char`` podem receber valores que vão de -128 até 127.

Lembrando que ele respeita a tabela ASCII. Se a tabela não tem o valor -1, ele vai simplesmente imprimir um caracter indefinido.

<exemplo de impressão com a variável recebendo o valor -1>

