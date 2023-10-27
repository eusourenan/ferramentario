# Hexadecimal
### <center>Os números que são representados com números e letras </center>

Pensando de forma matemática, existem diferentes formas de representar os números. O número 12, por exemplo, é representado como ``C`` em hexadecimal, é representado como ``14`` em base octal e é representado como ``1100`` em base binária.

Infelizmente, o printf não mostra números em binário. :face_holding_back_tears:

Porém, ele mostra números na base hexadecimal e na base octal! :partying_face::partying_face::partying_face:

Essas duas bases foram MUITO usadas por programadores, principalmente no início da programação. Faz todo o sentido o printf ter uma impressão rápida para esses tipos.

- Base decimal usa os caracteres ``0 1 2 3 4 5 6 7 8 9`` para representar os números.

- A base hexadecimal usa os caracteres ``0 1 2 3 4 5 6 7 8 9 A B C D E F`` para representar os números.

O que é feito no printf é simplesmente mostrar qual o valor em hexadecimal que representa o número enviado como argumento.

Como fazer?! Tome um exemplo:

```c
#include <stdio.h>

int	main(void)
{
	printf("Eis um número na base hexadecimal: %x\n", 12);
	return (0);
}
```

Como dito no exemplo no início desse tópico, a letra 'C' é a letra que representa o número 12 na base hexadecimal.

Caso você queira ver o 'C' como letra maiúscula, basta trocar o 'x' (minúsculo) por 'X' (maiúsculo). Assim, o printf entende a forma que você quer que seja printado o número. Troque o 'x' e veja a mágica acontecendo.

## E se eu quiser enviar um número em hexadecimal como argumento?

Você pode! :v:

Para fazer isso, faça o número começar com ``0x``. Isso faz o compilador entender que um número será enviado, mas que ele está com o formato hexadecimal.

Vamos fazer um teste:

<Exemplo usando o 0xC>

Como pode ser visto, ele imprime a letra C novamente. Pois ela é o número 12.

Se você pedir para printar um inteiro e enviar o número ``0xC``, irá ver que ele imprime o número 12 (basta trocar ``%x`` por ``%d``).

<Exemplo do parágrafo acima>

E mais, você pode escrever o ``0x`` e o número que vem depois, tanto com letras minúsculas ou com letras maiúsculas que ele entende! Sinta-se à vontade para testar.

# Octal

Assim como o exemplo acima mostrou que números podem ser convertidos em hexadecimal. Essa parte mostrará que eles podem ser convertidos para octal também.

- Decimais são representados com os caracteres ``0 1 2 3 4 5 6 7 8 9``.
- Octais são representados com os caracteres ``0 1 2 3 4 5 6 7``.

De forma bem parecida, usaremos o printf para saber os valores convertidos:

```c
#include <stdio.h>

int	main(void)
{
	printf("Eis um número na base octal: %o\n", 12);
	return (0);
}
```

O número 14 foi impresso, assim como dito no início de tudo. Pois, 14 em octal é igual a 12 em decimal.

Dá pra fazer o número em octal e pedir pra mostar em decimal? Dá sim! :v:

Pra isso, o número tem que começar com ``0``. Apenas isso.

Lembre-se dos caracteres que existem em octal ``8 e 9`` não estão incluídos. Pode testar o que vier à cabeça e ver como o programa se comporta.

<Erro de octal e hexadecimal?>

Entender a conversão de bases é uma coisa bem interessante. Mas deixo essa parte para a sua pesquisa, seja com o buscador de internet ou com os amiguinhos.

Partimos agora para nosso fechamento.