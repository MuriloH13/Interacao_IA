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

<!--

Nesta questão a IA disponibilizou dicas para uma melhor manipulação do programa ao ser executado,
pois ela da dicas de como evitar utilidades de certo modo desnecessárias na execução do programa.

-->

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

<!--

Nesta questão a IA disponibiliza algumas dicas em relação a boas práticas na programação como a
não declarar variáveis com nomes genéricos, não usar var ou dynamic sem necessidade ou até a não
utilização de final e const quando os valores não são mutáveis no programa. Essas dicas são exce-
lentes principalmente para melhorar tanto a legibilidade do código quanto sua execução.


-->

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

<!--

Nesta questão a IA da dicas de como fazer a utilização correta de variáveis nulas e também
disponibiliza dicas de como saber se a variável em questão realmente tem que ser nula ou
talvez, possa ser uma variável com um valor base onde em um problema específico isso possa
ser considerado um valor nulo, como setar um valor 0.00 em uma variável de um programa que
faz a soma de algo com essa variável por exemplo.

-->

• No dart quando usar variáveis nulas e quando usar o modificador late? 

Quando usar variáveis nulas (?)
Use ? quando o valor pode realmente ser null em algum momento do código. Isso ajuda a evitar erros e tornar o código mais seguro.

Use ? quando:
A variável pode não ter um valor inicial válido.
O valor pode ser alterado para null mais tarde.
Você pode lidar com null usando if, ??, ?., etc.

Quando usar late?
Use late quando a variável será inicializada mais tarde, mas sempre antes de ser usada.

Use late quando:
A variável não pode ser null, mas será inicializada depois.
Você tem certeza de que o valor será definido antes do uso.
Evita tornar a variável null desnecessariamente (?).

<!--

Nesta questão a IA mostra um pouco do modificador late e variáveis nulas, onde as variá-
veis nulas geralmente são variáveis com valores não obrigatoriamente informados/opcionais
e o modificador late é dito como uma variável que se assemelha ao null por ser inicialmente
nula e que embora esse fator ainda deve ser informada em algum momento.

-->

• Gostaria de entender quais os benefícios de utilização do modificador "late" no Dart. 

1. Evita valores nulos (null) sem precisar de ?
Em Dart, sem late, se uma variável não for inicializada imediatamente, ela precisa ser nullable (?). Isso pode ser um problema se você quer garantir que ela terá um valor, mas só será inicializada depois.

2. Inicialização eficiente e mais rápida
Se uma variável contém um valor que só será usado mais tarde, late adianta a inicialização e melhora o desempenho.

3. Permite variáveis obrigatórias em classes sem null
Se um valor será sempre definido antes do uso, mas não pode ser inicializado no construtor, late ajuda a manter o código seguro.

4. Ideal para injeção de dependência e variáveis que dependem de lógica
Em frameworks como Flutter, late permite inicializar variáveis depois de carregar dados da API ou banco de dados, sem que precisem ser null.

5. Evita inicializações desnecessárias
Se uma variável não for usada imediatamente, late adiará sua criação, evitando desperdício de memória e processamento.

<!--

Nesta questão a IA demonstra que o modificador late serve basicamente para delimitar
variáveis que não são declaradas pré-inicialização do código e que recebem valores somente
durante o período de execução do código, o que potencializa o desempenho do código e des-
carta a utilização de um valor inicial para a variável em questão.

-->

• Quais as diferenças entre final e const em dart?

1. final: Valor fixo, mas pode ser atribuído em tempo de execução
final significa que a variável pode ser atribuída apenas uma vez, mas o valor pode ser definido durante a execução do programa.

Usado quando o valor é conhecido apenas em tempo de execução.

Pode receber valores dinâmicos vindos de APIs, banco de dados, cálculos, etc.

2. const: Valor fixo e conhecido em tempo de compilação
const significa que o valor é imutável e precisa ser conhecido no momento da compilação.

Usado quando o valor nunca muda e pode ser definido antes da execução.

Objetos const são armazenados no tempo de compilação e otimizados pelo Dart.

3. const pode ser usado para criar objetos constantes
Diferente de final, const pode ser usado para criar objetos imutáveis.

Quando usar final e const?
Use final quando o valor será definido em tempo de execução
Exemplo: Dados de uma API, tempo atual, entrada do usuário.

Use const quando o valor é fixo e conhecido na compilação
Exemplo: Pi, tamanhos fixos, strings constantes.

Se precisar de imutabilidade máxima e otimização de memória, prefira const sempre que possível.

<!--

Nesta questão a IA demonstra as diferenças entre os modificadores final e const demonstrando
algumas de suas regras específicas como valores imutáveis em const e valores mutáveis em
tempo de execução como em final, assim destacando também a questão da otimização onde em
variáveis constantes o programa tem mais facilidade no acesso devido as mesmas serem imutáveis
e descartarem a necessidade de verificação da alteração da variável.

-->

• Por que no dart usar variáveis final e const ao invés de usar somente seus valores padrão? 

1. Evita valores mágicos e melhora a legibilidade do código
Se você espalha valores fixos pelo código, ele pode se tornar difícil de entender e manter. Usar final ou const dá nomes significativos aos valores, tornando o código mais claro e fácil de ler.

2. Evita repetições e facilita a manutenção
Se você precisar mudar um valor fixo, mudar apenas uma variável final ou const atualiza todo o código automaticamente.

3. Melhora o desempenho e reduz o consumo de memória
Quando usamos const, o Dart otimiza o uso da memória armazenando valores fixos uma única vez e reaproveitando-os.

4. Garante imutabilidade e segurança no código
Usar final e const impede que valores sejam alterados acidentalmente, evitando bugs difíceis de encontrar.

<!--

Nesta questão a IA demonstra que basicamente o motivo da utilização das variáveis final e const
está na otimização de código e também segurança de código pois por estas serem variáveis "constantes"
seu acesso para alteração ou remoção tornam-se mais difíceis do que em variáveis var por exemplo.

-->

• Quais métodos possuem as variáveis strings no dart? 

1. Métodos de Manipulação de Texto

🔹 toUpperCase() – Converte para maiúsculas

🔹 toLowerCase() – Converte para minúsculas

🔹 trim() – Remove espaços extras no início e no fim

🔹 replaceAll(String antiga, String nova) – Substitui todas as ocorrências

🔹 replaceFirst(String antiga, String nova) – Substitui a primeira ocorrência

🔹 replaceRange(int start, int end, String nova) – Substitui um trecho

2. Métodos de Busca

🔹 contains(String substring) – Verifica se contém um texto

🔹 indexOf(String substring) – Retorna a posição da primeira ocorrência

🔹 lastIndexOf(String substring) – Retorna a posição da última ocorrência

3. Métodos de Extração e Divisão

🔹 substring(int inicio, [int fim]) – Retorna parte da string

🔹 split(String delimitador) – Divide uma string em uma lista

🔹 characters – Divide a string em caracteres

4. Métodos de Verificação

🔹 startsWith(String prefixo) – Verifica se começa com um texto

🔹 endsWith(String sufixo) – Verifica se termina com um texto

🔹 isEmpty – Verifica se a string está vazia

🔹 isNotEmpty – Verifica se a string não está vazia

5. Métodos de Formatação

🔹 padLeft(int comprimento, [String preenchimento]) – Preenche à esquerda

🔹 padRight(int comprimento, [String preenchimento]) – Preenche à direita

6. Métodos de Conversão

🔹 toString() – Converte qualquer valor para string

🔹 parse() – Converte uma string para número

🔹 toInt() e toDouble() – Converte para número

<!--

Nesta questão a IA demonstra os métodos de variáveis String dispostos na linguagem Dart
que facilitam bastante o gerenciamento de Strings em Dart como a procura, leitura, conversão
e demais processos em Dart.

-->

• Traga a documentação dos métodos de variáveis inteiras.

• Métodos da classe int

🔹 abs(): Retorna o valor absoluto do número.​

🔹 ceil(): Arredonda o número para cima, retornando o menor inteiro maior ou igual a ele.

🔹 floor(): Arredonda o número para baixo, retornando o maior inteiro menor ou igual a ele.

🔹 round(): Arredonda o número para o inteiro mais próximo.

🔹 toDouble(): Converte o inteiro para um número de ponto flutuante (double)

🔹 toString(): Converte o inteiro para uma representação em string.

🔹 isEven: Retorna true se o número for par.

🔹 isOdd: Retorna true se o número for ímpar.

🔹 gcd(int other): Calcula o maior divisor comum (MDC) entre o número e outro fornecido.

🔹 modInverse(int modulus): Retorna o inverso modular deste número em relação ao módulo especificado.​

🔹 modPow(int exponent, int modulus): Calcula a exponenciação modular deste número elevado ao expoente especificado, módulo o valor fornecido.​

🔹 toRadixString(int radix): Converte o número para uma string na base especificada (entre 2 e 36).

🔹 bitLength: Retorna o número de bits necessários para representar o valor em binário, excluindo o sinal.

🔹 toUnsigned(int width): Trunca o número para um valor não assinado com o número de bits especificado.

🔹 toSigned(int width): Trunca o número para um valor assinado com o número de bits especificado.

<!--

Nesta questão a IA demonstra os métodos das variáveis Int dispostos na linguagem Dart
que facilitam a conversão, arredondamento, exponenciação e entre outros processos.

-->