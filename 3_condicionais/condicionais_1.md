# Condicionais
## Hora de começar a criar lógica de programação

Até aqui, aprendemos a criar variáveis, colocar valor nelas e fazer a impressão do jeito que queremos. Que progresso! :clap::clap::clap::clap::clap::clap::clap:

O que faremos agora é dar os primeiros passos para a lógica de programação.

Para fazer esses primeiros passos, vamos fazer nosso programa decidir entre duas mensagens e printar apenas uma.

Veja o exemplo:

```c
#include <stdio.h>

int	main(void)
{
	int	numero = 5;

	printf ("O número %d é positivo.", numero);
	printf ("O número %d é negativo.", numero);
	return (0);
}
```

Se executarmos esse código, vamos ter o seguinte resultado:

<print do código acima>

Como dá pra peceber, o código foi executado com sucesso. MAS, as mensagens são contraditórias e não fazem sentido para quem vai ler.

Isso acontece porque o computador é "um tanto robótico".

Se você mandar ele imprimir, ele imprime e ponto final. Se a mensagem não faz sentido, é apenas porque pedimos para imprimir algo que não deveria ser printado.

Daí, que podemos "dizer para o computador" que se algo ocorre ele imprime, ou não imprime a mensagem. Veja o exemplo:

```c
#include <stdio.h>

int	main(void)
{
	int	numero = 5;

	printf ("O número %d é positivo.", numero);
	if (numero < 0)
	{
		printf ("O número %d é negativo.", numero);
	}
	return (0);
}
```

Executando esse código temos:

<Print da execução do código acima>

A mensagem dizendo que 5 é número negativo não foi printada. O poder das condicionais está aí: em fazer ser executado o que queremos e ignorar o que não queremos.

Mais detalhes nas páginas que se seguem.