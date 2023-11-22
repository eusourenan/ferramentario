<p align="center"> <a href="variaveis_4.md"> << Letrinhas </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_6.md"> Próximo >> </a> </p>

# Unsigned

Como foi mostrado na [tabela](variaveis_1_copy.md#mas-quais-são-os-tipos-que-existem) de tipos de variáveis, os tipos ``int``, ``long`` e ``char`` podem ser tanto ``signed`` quanto ``unsigned``.

Vejamos alguns exemplos:

```c
#include <stdio.h>

int	main(void)
{
	unsigned int	numero;

	numero = 76;
	printf("Vejamos um número inteiro sem sinal: %u\n", numero);
	return (0);
}
```

```c
#include <stdio.h>

int	main(void)
{
	unsigned long	outro_numero;

	outro_numero = 76;
	printf("Vejamos um número do tipo unsigned long: %lu\n", outro_numero);
	return (0);
}
```

O tipo char não tem nenhuma flag para unsigned. Caso você queira ver a letra correspondente, use o ``%c``, se for o número que te interessa, basta usar ``%u``, ou ``%d``, ou outra flag para ver números.

```c
#include <stdio.h>

int	main(void)
{
	unsigned char	letra;

	letra = 76;
	printf("Vejamos a letra misteriosa: %c\n", letra);
	return (0);
}
```

Vendo o valor -1 nos 3 casos:

```c
#include <stdio.h>

int	main(void)
{
	unsigned int	numero;

	numero = -1;
	printf("Olha o unsigned -1: %u\n", numero);
	return (0);
}
```

```c
#include <stdio.h>

int	main(void)
{
	unsigned long	outro_numero;

	outro_numero = -1;
	printf("Olha o unsigned long -1: %lu\n", outro_numero);
	return (0);
}
```

```c
#include <stdio.h>

int	main(void)
{
	unsigned char	letra;

	letra = -1;
	printf("Qual a letra que é -1?\nR: %c\n", letra);
	printf("E o número que tem ali?\nR: %d\n", letra);
	return (0);
}
```

Unsigned continua sendo os números positivos seguindo o que foi [explicado anteriormente](variaveis_2_copy.md).

<p align="center"> <a href="variaveis_4.md"> << Cadê o char? </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_6.md"> Variáveis pra contar o troco >> </a> </p>
