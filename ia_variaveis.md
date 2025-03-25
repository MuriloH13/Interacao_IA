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