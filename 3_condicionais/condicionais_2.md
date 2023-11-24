# If-else

No tópico anterior, conversamos sobre como o if pode "direcionar" o que vai ser executado, simplesmente indo para uma direção, ou outra.

Como exemplos, tínhamos:

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
	return (0);
}
```

E

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
	if (number != 5)
	{
		printf("As coisas mudaram de figura.\n");
		printf("O número é difente do 5. Como pode?!\n");
	}
	return (0);
}
```

Vendo esses dois exemplos e analisando eles matematicamente, você pode se perguntar: "Tem algum jeito melhor de escrever isso?" A resposta é: sim.

A parte de "escrever melhor" vem como dúvida porque se o número é igual a 5, não tem como ele ser diferente de 5. Se o número é maior ou igual a zero, não tem como ele ser menor que zero. Um if exclui o outro.

Como há esse caso em que ele entra no escopo de um if, ou entra no escopo de outro if, verificar os dois casos sempre, parece meio... "burro demais".

A estrutura if-else ajuda a escrita a ficar melhor, além de ajudar o computador a executar mais rápido em alguns casos.

- **O funcionamento de vários ifs**
	
	Quando você tem um código como os códigos de exemplo acima, o programa SEMPRE irá verificar as duas condições. Se ele entrar no primeiro if, ele ainda assim vai verificar se o segundo é verdadeiro, mesmo que não precise.

	Isso significa que se você cria um código grande com mais de 100 verificações e existe momentos que ele precisaria verificar apenas 5, esse programa faria mais de 95 verificações sem a menor necessidade. E esse comportamento tem um custo no sistema.

- **A Solução**

	A criação da estrutura de if-else resolve o problema, porque o computador junta as duas condições "em um mesmo bloco".

	<Figura pra ilustrar?>

	Vejamos um exemplo:

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

	Basicamente, ele faz apenas uma verificação e executa o bloco de código que precisa ser executado.
	
	- Se a condição for verdadeira, ele executa o bloco que está com o ``if``.
	- Se não for verdadeira, ele executa o bloco de código que está com o ``else``.

Vejamos um outro exemplo com if-else:

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

Ao juntar os dois blocos, apenas uma verificação precisa ser feita, ao invés de duas. 

Ou ele entra no bloco que está com a condição, ou ele entra no outro bloco de código.

Por ele ter esse comportamento, essa estrutura é chamada de "se - senão".
- se for isso, execute isso.
- Senão, execute aquilo.

Simplesmente ter essa estrutura de if-else, corta o tempo de verificação pela metade. ao invés de duas comparações, apenas uma será feita. Pro computador, uma maravilha isso aí.

Lembrando que o if-else também suporta vários comandos em cada bloco.

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

Não há segredos aqui, você está mais apto(a) a fazer códigos com mais complexidade. Criar seus exemplos faz a diferença. Teste e se surpreenda!
