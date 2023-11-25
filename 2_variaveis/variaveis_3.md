<p align="center"> <a href="variaveis_2.md"> << Me fala sobre os bits </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_4.md"> Próximo >> </a> </p>

# Inteiros

Com os tipos explicados nos tópicos anteriores, resta apenas ver como usá-los. Para os inteiros, veja o exemplo:

```c
#include <stdio.h>

int	main(void)
{
	signed int	variavel;

	variavel = 42;
	printf("A resposta é %d.\n", variavel);
	return (0);
}
```

Variáveis do tipo ``signed int`` podem receber números que vão de -2147483648 até 2147483647.

Esse número está na casa dos bilhões, veja com os pontos: 2.147.483.647. Imagina isso de motivos pra dar risada!

Assim como nos exemplos da printf, nós podemos usar várias vezes o ``%d`` e a variável.

<exemplo com a variável replicada várias vezes>

<exemplo com mais de uma variável>

Operações com os valores armazenados nas variáveis também são válidas.

<Exemplo com operações matemáticas>

<Exemplo com operações matemáticas com mais de uma variável>

Quando se usa variável, basta imaginar que o valor que está ná variável será o valor que será entendido pelo programa em C.

Desse modo, podemos calcular uma fórmula inteira e guardar na variável.

```c
#include <stdio.h>

int	main(void)
{
	signed int	idade_pedro;

	idade_pedro = ((37 * 5) / 8) + 19;
	printf("Pedro tem %d anos\n", idade_pedro);
	printf("O dobro da idade de Pedro é %d\n", idade_pedro * 2);
	return (0);
}
```

Não precisamos nos preocupar com o código ser escrito errado em muitas partes.

Podemos guardar os valores e o resultado de fórmulas mais trabalhosas numa variável e pegar os valores que estão armazenados nela.

```c
#include <stdio.h>

int	main(void)
{
	signed int	idade_pedro;
	signed int	idade_ana;

	idade_pedro = 21;
	idade_ana = ((idade_pedro * 2) / 4) * 5;
	printf("Pedro tem %d anos\n", idade_pedro);
	printf("Ana tem %d anos\n", idade_ana);
	printf("Ana é %d anos mais velha que Pedro\n", idade_ana - idade_pedro);
	return (0);
}
```

Se não tivesse variáveis, o código seria assim:

```c
#include <stdio.h>

int	main(void)
{
	printf("Pedro tem %d anos\n", 21);
	printf("Ana tem %d anos\n", ((21 * 2) / 4) * 5);
	printf("Ana é %d anos mais velha que Pedro\n", ((21 * 2) / 4) * 5 - 21);
	return (0);
}
```

Usar variáveis facilita muito.

Armazenamos um valor na variável, e chamamos ela onde quisermos no código.

Se inserirmos o resultado de uma fórmula numa variável, usarmos essa variável várias vezes e algo estiver errado na fórmula, consertando em apenas um lugar, consertamos para todos.

Todos os outros tipos de variáveis seguirão o mesmo padrão.

O que elas vão ter de diferente será:
- O tamanho que a variável ocupa na memória;
- O intervalo de números que é possível representar.

### Mas, e se eu quiser um número maior que um int?

A solução são as variáveis do tipo long.

# Long

Variáveis do tipo ``signed long`` são idênticas às variáveis do tipo ``signed int`` com pequenas diferenças. Veja:

```c
#include <stdio.h>

int	main(void)
{
	signed long	variavel;

	variavel = 42;
	printf("A resposta é %ld\n", variavel);
	return (0);
}
```

- Usamos ``%ld`` ao invés de ter apenas a letra 'd'.
- Os números long tem o intervalo que vai de -9223372036854775807 até 9223372036854775807.

Se antes 2 bilhões estava bom, imagina ter 9 quintilhões de motivos pra dar risada (além de ter tudo na conta bancária)! Veja com os pontos: 9.223.372.036.854.775.807. Eita número grande!

## Observações
Nessa altura do campeonato, você deve ter percebido que esse conteúdo está muito relacionado com o que foi visto no tópico do printf. Até os intervalos dos números são os mesmos! E sim, você acertou.

A forma de escrever e os exemplos estão colocados apenas para você ter um exemplo de como usar os tipos. Depois daqui, recomendo você criar seus próprios exemplos e se sentir cada vez mais confortável com a criação de variáveis. Porque você mesmo(a) vai perceber que o padrão é o mesmo para todos os tipos.

<p align="center"> <a href="variaveis_2.md"> << Solta o 'bits' </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_4.md"> Quero ver letra na tela >> </a> </p>
