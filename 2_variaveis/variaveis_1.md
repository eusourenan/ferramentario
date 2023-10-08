# Os tipos de variáveis

Imagine o caso de você não ter o valor em mente, mas sabe a conta que resolve seu problema:

```c
#include <stdio.h>

int	main(void)
{
	printf("Pedro tem %d anos\n", 37);
	printf("O dobro da idade de Pedro é %d\n", 37 * 2);
	return (0);
}
```

<print da resposta>

Como dá pra ver, você pode digitar a fórmula. O resultado vai ser calculado.

O resultado da fórmula é que será enviado como argumento para o printf.

No final, terá apenas um único resultado, independente da fórmula que você mandar.

<print com alguma fórmula que vier à cabeça e que seja bem grande e/ou complexa>

**E se a gente precisasse usar essa fórmula em mais prints?**

Dá pra fazer um simples ``Ctrl + C, Ctrl + V``.

<print pra confirmar a frase acima>

E se eu precisasse mudar algo na fórmula porque está errado?

Como você está imaginando, você teria que mudar em todos os printf que você tivesse usado aquela fórmula.

Tem algum jeito mais fácil? Sim! Podemos criar variáveis:

<Substituir a fórmula problema pela variável que recebe o valor que queremos>

Vamos falar do que aconteceu. Primeiro, uma variável foi criada. Chamamos isso de ``declaração`` de variável:

<Parte da declaração da variável>

Depois, inserimos um valor nessa variável. Essa parte é chamada de ``atribuição`` da variável:

<Atribuição>

E por fim, usamos a variável:

<Os printfs>

Toma um exemplo simplificado:

<Exemplo simplificado e comentado>

A vantagem é que agora, basta a gente mudar o valor na linha da atribuição que ele será alterado em todos os lugares nos quais usamos a variável.

Não tem mais re-escrita de código, nem duplicação de uma parte difícil de modificar.

Sendo assim, variável é só um meio de usar um valor que já foi definido antes em outro lugar do código, sem precisar definir o valor de novo.

## Regras de Declaração de Variáveis

- Primeiro devemos especificar o tipo da váriavel, depois o nome da variável.

  - Nesse exemplo: ``signed int`` (inteiro com sinal) é o tipo e ```` é o nome da variável.

-  Variáveis não podem ter acento, não podem começar com número e não podem ter caracteres especiais além do ``_`` (underline).

   - Exemplos de nomes de variáveis válidas:
     - variavel
     - _teste
     - _teste2
	  - mesclando_t3xt0_c0m_num3r02

	- Exemplos errados:
	  - 1teste
	  - $com(cara@
	  - um-teste-qualquer
	  - 1234

Os próximos tópicos tratam dos tipos de variáveis que temos em C.

<p align="center"> <a href="../1_printf/printf_5.md"> << Anterior </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_2.md"> Próximo >> </a> </p>