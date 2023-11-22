<p align="center"> <a href="variaveis_1.md"> << O início </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_3.md"> Próximo >> </a> </p>

# Explicação Introdutória

[Quando conversamos sobre o tipo unsigned](../1_printf/printf_7.md), foi dito que as variáveis tem duas formas de ser representadas: 

- Com números negativos e positivos. São as variáveis ``signed``;
- Somente com os números positivos. São as variáveis ``unsigned``.

Para fins didáticos, direi que:
- Variáveis com ``signed``, são variáveis que tem um sinalizador;
- Variáveis ``unsigned`` são variáveis que NÃO tem um sinalizador.

Com isso entendido, vêm as dúvidas:

- **E o que é isso? Como funciona? Do que se alimenta?**

Vamos responder isso:

Os números são armazenados em binário pelo computador e depois convertidos em decimal para nós, seres humanos entendermos melhor.

O número 9, por exemplo, em binário é 1001. É em binário que o computador entende o número 9. Mas depois ele converte pra gente e vemos o número 9 na tela.

Cada casa de zeros e uns do número binário 1001 é chamada de ``bit``. Mas, nós usamos frequentemente a unidade ``byte``, que é igual a 8 bits.

Repetindo: 1 byte é igual a 8 bits.

Se esse número 9 estiver numa variável com 1 byte de memória, ele é representado assim: ``00001001``.

Se ele estiver representado numa memória com 2 bytes, ele é representado assim: ``00000000 00001001``.

Se ele estiver representado numa memória com 4 bytes, ele é representado assim: ``00000000 00000000 00000000 00001001``.

Os espaços foram colocados por mim, pra você enxergar melhor. No computador, será tudo juntinho.

Mesmo que o número 9 seja pequeno, se ele estiver numa variável que tem 4 bytes de memória, ele será representado com aquele monte de zeros à esquerda.

Por isso, uma vez definido o tipo da variável, ele terá aquele tamanho e ponto. Mesmo que você não precise de todos os bits daquele número.

## É tudo por uma questão de memória.

Lembremos que a memória do computador é limitada. Por conta disso, os programadores limitaram a quantidade de espaço que uma variável ocupa no sistema.

Daí que quando criamos uma variável do tipo ``signed char``, por exemplo, o computador vai nos dar um espaço de 1 byte (que vale 8 bits).

<Figura com um vetor de 8 bits>

O espaço reservado vai ser bem parecido com a figura.

Se quisermos uma variável do tipo ``unsigned char``, o computador vai nos dar um espaço de 1 byte (que continua valendo 8 bits).

<Mesma figura que foi mostrada antes>

Então como raios ele sabe qual é qual?

Simples! O primeiro bit (da esquerda pra direita) vai ser usado para dizer se o número é positivo ou negativo quando a variável é ``signed`` (por isso é sinalizada).

<Figura com o primeiro bit selecionado e indicado como sinalizador e os outros selecionados indicando que eles serão usados para representar os números>

- Quando o bit sinalizador é 0, o número é positivo.

- Quando o bit sinalizador é 1, o número é negativo.

Quando a variável é ``unsigned`` esse bit não é usado para saber se o número é negativo ou positivo. Todos os espaços são usados para representar o número.

<Figura análoga à de cima, enfatizando que todos os bits são usados para representar o número>

Daí que ele consegue representar diferentes quantidades de números usando a mesma quantidade de memória para quando o número é ``signed`` e quando o número é ``unsigned``.

Se você veio direto do tópico do tipo unsigned, recomendo [voltar](../1_printf/printf_7.md). Existem outras coisas que você tem que ver ainda.

E pra quem fica, vamos falar deles, os famosinhos:

<p align="center"> <a href="variaveis_1.md"> << Volta pro início </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_3.md"> Vamos conhecer os famosinhos >> </a> </p>
