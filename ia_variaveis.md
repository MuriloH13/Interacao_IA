• Quais as boas práticas em dart declarando variáveis?

1. Use final e const sempre que possível
Evite var e dynamic quando o valor não muda.

final: para valores que são definidos apenas uma vez (tempo de execução).

const: para valores que nunca mudam (tempo de compilação).

2. Prefira tipos explícitos quando possível
Usar tipos explícitos melhora a legibilidade e ajuda a evitar erros.
Ainda assim, var pode ser usado quando o tipo é óbvio pelo valor atribuído.

3. Evite dynamic quando possível
O tipo dynamic desativa a verificação de tipo, o que pode levar a erros difíceis de depurar.
Prefira usar tipos específicos ou Object? se precisar armazenar qualquer valor.

4. Use late apenas quando necessário
late pode ser útil para inicialização tardia, mas evite seu uso excessivo.

• O que evitar na hora de declarar variáveis em dart?

1. Usar var ou dynamic sem necessidade
O uso excessivo de var pode tornar o código menos claro, enquanto dynamic desativa a verificação de tipo, podendo causar erros em tempo de execução.

2. Declarar variáveis sem necessidade
Evite criar variáveis que não são usadas ou que poderiam ser substituídas diretamente por expressões.

3. Não usar final e const para valores imutáveis
Se o valor não precisa mudar, use final ou const para melhorar a eficiência.

4. Nomes de variáveis pouco descritivos
Usar nomes genéricos ou abreviados dificulta a leitura do código.

5. Declarar variáveis late sem necessidade
O modificador late só deve ser usado quando realmente precisar de inicialização tardia.

6. Não usar ? para valores nulos quando necessário
Se uma variável pode ser null, deve ser declarada corretamente com ? para evitar erros.

7. Usar listas e mapas mutáveis quando não precisa
Se a coleção não deve ser alterada, declare-a como const para evitar modificações acidentais.

• Quais cuidados tomar quando crio variáveis com valor nulo trabalhando com dart? 

1. Use ? para permitir valores nulos
Em Dart, uma variável pode ser nullable (aceita null) ou non-nullable (não aceita null). Para permitir null, use ? ao declarar a variável.

2. Verifique se a variável não é null antes de usá-la
Se uma variável pode ser null, você deve tratá-la antes de acessá-la para evitar erros.

Use if antes de acessar:
Use o operador ?. para evitar erros:
Use ?? para definir um valor padrão:

3. Evite late sem necessidade
O modificador late permite adiar a inicialização de uma variável, mas se ela não for inicializada antes do uso, causará erro.
Use late apenas quando souber que a variável será inicializada antes do uso:

4. Converta null para um valor padrão com ??
O operador ?? permite definir um valor caso a variável seja nula.

5. Utilize ! apenas quando tiver certeza de que não é null
O operador ! força Dart a tratar a variável como não nula, mas se a variável for realmente null, o programa quebrará.

 6. Inicialize variáveis nullable com valores padrão sempre que possível
Evite null desnecessário atribuindo um valor padrão na inicialização.

7. Use required para parâmetros que não podem ser nulos
Quando criar funções ou classes, use required para obrigar que certos valores sejam passados.