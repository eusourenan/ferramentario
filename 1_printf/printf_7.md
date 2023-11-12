<p align="center"> <a href="printf_6.md"> << Número do xizinho </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="printf_8.md"> Próximo Tipo >> </a> </p>

# Unsigned
### <center>Quero somente números positivos!</center>

Nesse ponto da jornada, já sabemos que o computador não representa números infinitamente, ele para em algum momento.

A memória pode ser limitada, mas a criatividade humana supera essas barreiras de modos bem inteligentes.

Uma dessas barreiras foi: ``"Como representar vários números com uma mesma quantidade de memória?"``. 

Para dar um super resumo, eles fizeram a linguagem C entender o número de formas diferentes.
- Se eles quiserem os números positivos e negativos, existe um jeito certo de lidar com o número.
- Se eles quiserem APENAS números positivos, existe uma outra forma de lidar com o número.
- Não existe um tratamento para números apenas negativos.

Daí que em inglês chamamos os números de ``signed`` quando tem diferenças de negativos e positivos.

E chamamos de ``unsigned`` quando os números são apenas positivos.

Todos os exemplos anteriores lidaram com números ``signed``. Esse tópico vai lidar com números ``unsigned``.

[Num momento futuro](../2_variaveis/variaveis_2_copy.md) veremos com mais detalhes como isso está acontecendo.

Para testarmos, segue o exemplo:
```c
#include <stdio.h>

int	main(void)
{
	printf("Veja um número unsigned: %u\n", 42);
	return (0);
}
```

No momento que esse código é executado, o que é printado é exatamente o que estamos acostumados a ver.

Mas, e se mandarmos um número negativo?

```c
#include <stdio.h>

int	main(void)
{
	printf("Veja uma mágica estranha: %u\n", -1);
	return (0);
}
```

Se mandarmos printar...:

<print do código acima>

Mas o que foi isso?! Como assim -1 virou esse número?!

Para entender o que aconteceu, devo relembrar: A linguagem C ``N͟Ã͟O͟``  consegue representar todos os números, a memória do computador é LIMITADA. Sendo assim, existe um jeito de representar os números e de tratar eles. 

# Números Limitados

Quando a gente manda um número maior do que é possível, a linguagem C dá um jeito de representar esse número dentro do intervalo dos números que existem na memória.

Para um exemplo visual, imagine um relógio.

- Se o ponteiro estiver marcando 12 horas e a gente somar mais uma hora, o ponteiro muda para 1 hora.

<Exemplificar o que foi dito>

- Se o ponteiro estiver marcando 1 hora e a gente diminuir uma hora, ele volta para as 12 horas.

<Exemplo de novo>

Não importa o quanto a gente avance ou diminua o valor das horas. Sempre será um número entre 1 e 12. Não vai aparecer um 37 do nada num relógio. (Só se você tiver um relógio diferenciado).

<Fazer um relógio que vai de zero até 12?>

Com os números aqui na linguagem C, acontece da mesma forma.

- Se avançarmos demais o número, ele volta para zero.
- Se diminuirmos demais o número, ele vai até o número máximo.

O número máximo e o número mínimo é definido pela linguagem e depende o tipo do número. [Os intervalos de cada tipo podem ser vistos nesta tabela aqui]().

Colocando -1 como no exemplo, pedimos pra ele voltar 1 número, começando do zero.

Se colocar -2 ele volta dois números, começando do zero. Se colocar -3, volta 3 números, e assim por diante.

O mesmo efeito ocorre com números ``signed``. Veja um exemplo:

```c
#include <stdio.h>

int	main(void)
{
	printf("Zero: %d\nSomando 1: %d\nSubtraindo 1: %d\n", 0, 0 + 1, 0 - 1);
	printf("\n\nInteiro máximo: %d\nSuperando o limite do inteiro: %d\n", 2147484347, 2147483647 + 1);
	printf("\n\nInteiro Mínimo: %d\nQuerendo printar um número menor que o mínimo: %d\n", -2147483648, -2147483648 - 1);
	return (0);
}
```

Esses efeitos de "voltar para os limites dos números do relógio" tem nomes.

- Quando estamos em um número gigante e ele vai para um número menor (ou para um número negativo), chamamos isso de ``overflow``.
- Quando estamos em um número bem pequeno (ou negativo) e ele vai para um número gigante, chamamos isso de ``underflow``.

## Finalizando

Octal ``(%o)`` e hexadecimal ``(%x)`` são tratados como números ``unsigned``. Caso você tenha testado antes e estranhado o resultado grandão, agora você entende melhor o que acontece.

Os números ``unsigned`` vieram como uma alternativa para printar números maiores usando uma memória limitada, porque os computadores tinham muitas limitações de memória.

O tempo passou e os computadores evoluíram. Conseguimos mais memória e processamento. Os programadores não pensaram em aumentar os intervalos disponíveis?

Não só pensaram, como fizeram! Para mais detalhes, vamos para o próximo tópico.

<p align="center"> <a href="printf_6.md"> << Número com letra junto </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="printf_8.md"> EVOLUÇÃO! >> </a> </p>