# String

Strings serão aprofundadas no tópico sobre ponteiros. 

Por hora, vamos ver a declaração:

```c
#include <stdio.h>

int	main(void)
{
	signed char	*variavel;

	variavel = "Tem uma string na variável";
	printf("Qual a mensagem? '%s'\n", variavel);
	return (0);
}
```

Por que não ser ``signed string`` ou ``signed str``? 

Sendo bem sincero, foi uma escolha das pessoas que fizeram a liguagem. 

Mas, tem uma lógica, ``string é uma sequência de caracteres``. Isso facilita para a montagem dos ponteiros (que explicarei mais tarde).

Tem 2 valores que a string pode receber:
- NULL
- A frase que você deseja

Ela é bem direta ao ponto.