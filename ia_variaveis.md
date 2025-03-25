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