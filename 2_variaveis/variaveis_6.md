<p align="center"> <a href="variaveis_5.md"> << Unsigned </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_7.md"> Próximo >> </a> </p>

# Float

Em relação à declaração de variáveis, o padrão é o mesmo que já vimos várias vezes:
```
tipo_da_variável nome_da_variável
```
Eis que agora vamos ver o tipo ``signed float``, mas esse vem com um diferencial. Dá uma olhada:

```c
#include <stdio.h>

int	main(void)
{
	float	variavel;

	variavel = 12.3456;
	printf("Quero dinheiro, mas só tenho R$ %f\n", variavel);
	return (0);
}
```

Sim, você viu direito, não tem a palavra ``signed``.

<Mostar erro usando signed float>

A palavra ``signed`` só pode ser explicitada nos tipos int, char e long.

- **Mas, por quê isso acontece?**

A resposta mais sincera é: Não sei.

Acredito que por não ser possível usar o tipo float como variável ``unsigned`` os programadores já restringiram o uso das palavras ``signed`` e ``unsigned`` de uma vez.

Assim, facilita o uso para quem vai criar o programa, basta criar com o tipo ``float`` e pronto!

O mesmo exemplo serve para as variáveis do tipo ``double`` e ``long double``.

Veja os exemplos abaixo:
<Algum gráfico para efeito visual da frase acima?>

# Double

```c
#include <stdio.h>

int	main(void)
{
	double	variavel;

	variavel = 12.3456;
	printf("Quero dinheiro, mas só tenho R$ %lf\n", variavel);
	return (0);
}
```

# Long Double

```c
#include <stdio.h>

int	main(void)
{
	long double	preco_pastel;

	preco_pastel = 9.50;
	printf("Pastel de flango tá custando R$ %LF\n", preco_pastel);
	return (0);
}
```

# Observações

Talvez venha a dúvida na mente: **Mas, não teria um jeito de simplificar então os tipos ``char``, ``int`` e ``long`` para não ter que ficar usando 2 palavras toda hora?**

E tem! Caso as variáveis sejam signed (``signed char``, ``signed int``, ``signed long``) você não precisa colocar a palavra signed, a linguagem C entende.

Caso você queira que as variáveis sejam ``unsigned`` você precisa colocar a palavra. Exemplo:

```c
// Variável do tipo signed (não precisa usar a palavra "signed", caso você não queira)
int var;
char var;
long var;

// Variável do tipo unsigned (você DEVE usar a palavra "unsigned" na hora de declarar)
unsigned int var;
unsigned char var;
unsigned long var;
```

Falta apenas as explicações de valores em octal, hexadecinal e variáveis so tipo string.

<p align="center"> <a href="variaveis_5.md"> << Os independentes de sinais </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_7.md"> Os números diferentões >> </a> </p>
