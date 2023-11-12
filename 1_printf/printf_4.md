<p align="center"> <a href="printf_3.md"> << Char, o camadara </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="printf_5.md"> Próximo Tipo >> </a> </p>

# Strings
### <center>Sequência de letras, também temos!</center>

Nesse ponto da jornada já estamos familiarizados com o nosso amigo printf.

Pode ser que a gente ainda não conheça todos os seus segredos, mas já sabemos melhor como usá-lo.

Agora é uma questão de mostrar o que pode ser impresso. Nesse tópico é a vez das ``strings``. Olha o exemplo:

```c
#include <stdio.h>

int	main(void)
{
	printf("Meu nome é: %s\n", "Pedrinho da Alemanha");
	return (0);
}
```

Você pode mandar textos completos agora! :partying_face::partying_face::partying_face:

Repare que aspas são usadas ao invés de apóstrofos.

A͟p͟ó͟s͟t͟r͟o͟f͟o͟s se usam quando o argumento é apenas um único caractere. A͟s͟p͟a͟s se usam para quando o argumento tem mais de um caractere.

Veja esse exemplo:

<Exemplo anterior com apóstrofos no lugar de aspas>

Ele reclama porque usamos apóstrofos. Isso é como dizer para o programa que você está mandando um único caractere, mas na hora que o progama é compilado, o compilador percebe que tem mais de um caractere ali. Essa contradição gera o erro que pode ser visto.

Nós vemos um erro porque, para a linguagem C, existe um jeito específico de lidar com as strings. Sendo assim, a forma de representar também é diferente.

Por isso, use sempre aspas (``" "``) para o ``%s``, apóstrofos (``' '``) para o ``%c`` e você evitará dores de cabeça.

E sim, você pegou bem a ideia: o 's' vem de ``string``.

Strings são um monte de caracteres individuais em sequência, juntos num único bloco.

Os detalhes maiores [serão vistos depois.]() Por hora, aproveite o fato de você poder enviar vários textos como argumento.

Também aproveite para ver o próximo tipo, os números reais (famosos números com vírgula).

<p align="center"> <a href="printf_3.md"> << Camarada, o Char </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="printf_5.md"> Hora de calcular o troco do pão? >> </a> </p>
