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

Repare que aspas são usadas ao invés de apóstrofos.

A͟p͟ó͟s͟t͟r͟o͟f͟o͟s se usam quando o argumento é apenas um caracter. A͟s͟p͟a͟s se usam para quando o argumento tem mais de um caracter.

Strings são um monte de caracteres em sequência juntos num único bloco. Explicações virão num futuro próximo.
