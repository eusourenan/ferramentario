<p align="center"> <a href="printf_4.md"> << Stringona </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="printf_6.md"> Próximo Tipo >> </a> </p>

# Float Numbers
### <center>Números que flutuam?</center>

Os nossos chamados números reais tem um paralelo na programação, chamamos eles de n͟ú͟m͟e͟r͟o͟s f͟l͟u͟t͟u͟a͟n͟t͟e͟s.

Eles são chamados de flutuantes por "flutuarem" entre o número que você digitou e o que é possível representar no sistema.

Como assim ``"o que é possível representar no sistema"``? Simples, o computador não tem memória infinita e não consegue representar infinitos números.

Quando você enviar um número com muita precisão, por exemplo, ele arredonda pro mais próximo que ele consegue representar. Por isso, ele "flutua".


Caso queira ver os pormenores disso, te mostro esses links:
https://en.wikipedia.org/wiki/Floating-point_arithmetic

https://en.wikibooks.org/wiki/Data_Science:_An_Introduction/Definitions_of_Data#Data_Types_in_Computer_Science

Partindo para a parte de printar, ``floats`` tome o exemplo:

```c
#include <stdio.h>

int	main(void)
{
	printf("Número real qualquer: %f\n", 42.1234);
	return (0);
}
```

<Print do exemplo acima>

Como pode ser visto, o número é representado lindamente da forma que foi enviado no argumento. Esses são os números flutuantes.

Mas o rolê de "flutuar", vou ver como? Taí um exemplo:

<Exemplo do que foi dito sobre o número 'flutuar'>


# Observações

- O padrão em países de língua inglesa é diferenciado.

	Nós escrevemos um milhão de dinheiros assim: 1.000.000,00.\
Eles preferem escrever o mesmo milhão assim: 1,000,000.00.

	Como a linguagem segue o padrão dos americanos (e eles falam inglês), temos que usar o ponto pra fazer um número real. Se usarmos vírgula, ele vai reclamar com a gente.

<print de erro>

- Apesar de não ser possível representar infinitos números, a variedade de números é bem alta e pode ser que você nem sinta tanto a falta de precisão numérica. Principalmente agora que estamos em fase de aprendizado.

Sobre os floats, encerro por aqui.

Existem outros meios de modificar os números e outras bases de números que podem ser printadas com o printf! Vamos conhecê-las!

<p align="center"> <a href="printf_4.md"> << Quero printar strings </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="printf_6.md"> Show me more! >> </a> </p>