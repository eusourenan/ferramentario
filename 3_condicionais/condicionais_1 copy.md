# Condicionais
## Hora de começar a criar lógica de programação

Até aqui, aprendemos a criar variáveis, colocar valor nelas e fazer a impressão do jeito que queremos. Que progresso! :clap::clap::clap::clap::clap::clap::clap:

Agora chegou o momento de fazer perguntas no nosso código. Vamos fazer com que nosso programa pergunte ao computador e, dependendo da resposta, vamos fazer o programa executar algo, ou não executar algo.

Para entendermos melhor, imagine o seguinte código:

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

Se executarmos ele, termos duas mensagens diferentes. Essas mensagens serão contraditórias e irão bugar o cérebro de quem executar o programa.

Como então dizer para o computador que queremos imprimir a mensagem de número negativo, somente quando o número for negativo?

Com o uso do if! Veja o exemplo:

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

Aqui estamos dizendo que a mensagem "``O número 5 é negativo``" só será impressa se o número 5 for menor que o número zero. Veja a execução:

<Print da execução do código acima>

Como podemos perceber, uma parte do código foi ignorada.

Isso é uma ferramenta poderosa! Ela mostra que nós podemos agora ignorar vários pedaços do código com base em uma única condição!

Parece um tanto bobo com o exemplo de agora, mas essa ferramenta chamada ``if`` aparece nos mais diversos tipos de código. Seja um código simples, ou um código de um programa super complexo. Você agora começa a ditar para a máquina o que ela deve ou não deve fazer!

Vamos entender a fundo como o if funciona nos próximos tópicos.
