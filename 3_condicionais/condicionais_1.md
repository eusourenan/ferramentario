# O fluxo de um programa
Quando um programa é executado, ele segue "em queda livre, como uma cachoeira". Passa pela linha 1, depois pra linha 2, depois pra 3, e assim por diante.

<Exemplo do fluxo do código>

Mas e se tivermos algum código em que não queiramos que ele passe por todas as linhas?

Por exemplo:
```c
#include <stdio.h>

int	main(void)
{
	int	var;

	var = 6;
	printf("A variável tem valor positivo\n");
	printf("A variável tem valor igual a 5\n");
	return (0);
}
```

<Print do código acima>

Mostrar as duas mensagens, como o código acima faz não traz um sentido lógico.

Apagar ou editar uma das mensagens pode resolver esse problema, mas pode não resolver muitos outros do dia a dia.

A solução para esse problema são as condicionais.

<Código com um if para o segundo print>

Neste exemplo é feita uma verificação antes de printar a mensagem. Se a condiçã resultar numa resposta falsa, não será printado.


# Operadores Relacionais

- <
- <=
- \>
- \>=
- =\=
- !=

Esses são os únicos operadores aritméticos que existem na linguagem C.

TODAS as comparações que você quiser fazer terão que usar algum desses 6.

# Operadores Lógicos

- &&
- ||

Junção de 2 operadores aritméticos.

TODAS as comparações que você quiser fazer com operadores lógicos, terão que usar algum desses 2.