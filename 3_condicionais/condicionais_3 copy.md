# If-else

Como agora sabemos criar ifs com maior facilidade e entendemos que é uma pergunta com duas respostas possíveis: ``sim ou não``, podemos ver agora formas diferentes de escrever os ifs, para situações específicas.

Para entendermos melhor, veja um exemplo:

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

Para este caso, temos duas opções de perguntas:

```c
#include <stdio.h>

int	main(void)
{
	int	numero = 5;
	if (numero >= 0)
	{
		printf ("O número %d é positivo.", numero);
	}
	if (numero < 0)
	{
		printf ("O número %d é negativo.", numero);
	}
}
```

Como podemos perceber, uma condição automaticamente exclui a outra. Afinal, ou o número é positivo, ou o número é negativo, não tem como ele ser os dois ao mesmo tempo. A não ser que você seja um matemático quântico. 

Mesmo que o programa seja simples e tenha essas duas condições; mesmo que essas duas condições sejam excludentes (ou acontece uma, ou acontece outra). O computador comparar cada if para ter certeza do que acontece.

Neste nosso programa com apenas dois ifs comparar os dois nem faz tanta diferença. Mas em programas mais completos e complexos, fazer a comparação de todas as possibilidades, encontrar o que você quis e continuar verificando pode ser muito custoso para o sistema. Seu programa pecaria em performace.

Nosso foco então está em buscar uma forma de escrever melhor as condições, além fazer o programa parar de ficar perguntando se a condição é verdadeira quando ele já achou a resposta. O ``else`` foi a palavra-chave que os criadores do C deixaram como opção para nós.

## **A Solução**

Sei que seria melhor uma introdução, mas vamos colocar o exemplo no começo e explicar os detalhes em seguida:

```c
#include <stdio.h>

int	main(void)
{
	int	numero = 5;

	if (numero >= 0)
	{
		printf ("O número %d é positivo.", numero);
	}
	else
	{
		printf ("O número %d é negativo.", numero);
	}
	return (0);
}
```

Como foi comentado antes quando estávamos com 2 ifs, as condições eram excludentes, somente uma das duas é que seriam verdadeira.

Com isso em mente, os criadores criaram o que chamamos de "estrutura if-else" (em português, poderíamos traduzir por "se-senão").

A vantagem para a execução é que o computador junta esse conjunto "if-else" como se fosse uma coisa só. O sistema processa mais rápido e fazemos menos comparações.

Um exemplo em português pode deixar um pouco mais claro:

```
se (numero >= 0)
{
	...
}
senão
{
	...
}
```

Apenas para retomar:

- Se a condição for verdadeira, ele executa o bloco que está com o ``if``.
- Se não for verdadeira, ele executa o bloco de código que está com o ``else``.

Com esse conhecimento, podemos fazer códigos ainda melhores e que consomem menos tempo de sistema. Agora estamos evoluindo nos passos de programação para construir códigos com maior complexidade! :clap::clap::clap::clap::clap::clap::clap:


Para uma melhor fixação do que foi ensinado, vamos ver mais exemplos com if-else:

```c
#include <stdio.h>

int	main(void)
{
	int	temperatura = 25;

	if (temperatura > 30)
	{
		printf ("Está muito quente hoje\n");
	}
	else
	{
		printf ("Hoje está com um clima agradável\n");
	}
	return (0);
}
```

```c
#include <stdio.h>

int	main(void)
{
	int number = 5;

	if (number == 5)
	{
		printf("Tenho uma mensagem escrita.\n");
		printf("Ela diz que o número é um número primo e é o número 5.\n");
		printf("Tudo isso ao mesmo tempo.\n");
	}
	else
	{
		printf("As coisas mudaram de figura.\n");
		printf("O número é difente do 5. Como pode?!\n");
	}
	return (0);
}
```

Com esse conhecimento, podemos controlar muito do que o sistema consegue executar com uma única pergunta. Mas, e se precisarmos trabalhar com algo que não tenha apenas duas possibilidades?

A estrutura "if/ else if/ else" tem a resposta que queremos.
