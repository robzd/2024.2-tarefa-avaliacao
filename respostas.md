# 2024.2 Avaliação do 1o período de Sistemas Operacionais

## Informações gerais
- **Objetivo do repositório**: Avaliação do 1o bimestre da Disciplina de sistemas operacionais do curso de TADS do IFRN-CNAT
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- disciplina: **SO** Sistemas Operacionais
- professor: [Leonardo A. Minora](https://github.com/leonardo-minora)
- aluno: Robson Douglas Fernandes de Araújo - 20231014040036

# Questão 1. Introdução a sistemas operacionais

Considere as funções e objetivos principais de um sistema operacional conforme discutido no texto. Explique como um sistema operacional gerencia os recursos de hardware e software de um computador para garantir eficiência e segurança. Em sua resposta, aborde os seguintes pontos:

- Gerenciamento de processos
- Gerenciamento de memória
- Gerenciamento de dispositivos de entrada e saída
- Gerenciamento de arquivos

## Resposta:
Inicialmente, considerando processos, que se referem às tarefas que estão sendo executadas ou em qualquer outro estado dentro da máquina,
quando se abre um programa, como um navegador qualquer por exemplo, o SO utiliza a CPU para definir um escalonamento, que determina
a ordem de prioridade e o tempo que cada processo vai utilizar o processador.  
Quanto ao gerenciamento de memória, é aqui onde é definida a memória necessária para ser utilizada pelos processos, o SO muitas vezes
usa métodos como memória virtual, que permite o uso de mais memória do que o que é fisicamente suportado normalmente, parte dessa memória
extra é normalmente armazenada em dispositivos como HD ou SSD, um programa pesado de abrir, por exemplo, é um processo pesado e portanto
necessita do alocamento de mais memória para realizá-lo.  
Considerando dispositivos de entrada e saída, o SO se comunica com eles através da utilização de drivers, que basicamente são programas
instalados no sistema que traduzem as informações passadas pelos dispositivos e vice-versa, um mouse, por exemplo, tem suas direções
analisadas e repassadas através de um driver, definindo para onde o cursor vai. Por fim, o gerenciamento de arquivos é feito através de
diretórios e pastas dentro de um programa que os organiza, como o explorador de arquivos, ele define quem tem acesso a determinadas pastas
ou arquivos por questão de segurança e, por exemplo, quando você salva um arquivo novo na máquina, é também nesse momento onde é definida
a pasta na qual o arquivo vai ser salvo e a atualiza.

# Questão 2. Estrutura de sistemas operacionais
### Estrutura de Sistemas Operacionais: Custo de Desenvolvimento e Segurança da Informação

A estrutura de um sistema operacional (SO) é fundamental para determinar tanto o custo de desenvolvimento e manutenção quanto a segurança da informação. Existem várias arquiteturas de SO, como monolítica, microkernel e em camadas, cada uma com suas próprias implicações em termos de custo e segurança.

#### Custo de Desenvolvimento e Manutenção

1. **Arquitetura Monolítica**:
   - **Desenvolvimento**: Geralmente, mais rápida de desenvolver inicialmente, pois todos os componentes do SO são integrados em um único bloco de código.
   - **Manutenção**: Pode ser mais complexa e cara, pois qualquer alteração em um componente pode afetar todo o sistema, exigindo testes extensivos e cuidadosos.

2. **Arquitetura Microkernel**:
   - **Desenvolvimento**: Pode ser mais demorada e cara inicialmente, pois envolve a criação de um núcleo mínimo e a implementação de serviços adicionais como processos separados.
   - **Manutenção**: Mais fácil e menos custosa, já que os componentes são isolados. Atualizações e correções podem ser feitas em módulos específicos sem impactar o núcleo do sistema.

3. **Arquitetura em Camadas**:
   - **Desenvolvimento**: Moderadamente complexa, pois cada camada deve ser bem definida e interagir corretamente com as outras.
   - **Manutenção**: Relativamente fácil, pois problemas podem ser isolados e corrigidos em camadas específicas sem afetar o restante do sistema.

#### Segurança da Informação

1. **Arquitetura Monolítica**:
   - **Segurança**: Pode ser mais vulnerável, pois uma falha em qualquer parte do sistema pode comprometer todo o SO. A integração de todos os componentes em um único bloco de código pode dificultar a implementação de medidas de segurança robustas.

2. **Arquitetura Microkernel**:
   - **Segurança**: Geralmente mais segura, pois isola os serviços em processos separados. Isso limita o impacto de uma falha ou ataque a um único componente, protegendo o núcleo do sistema e outros serviços.

3. **Arquitetura em Camadas**:
   - **Segurança**: Oferece um bom equilíbrio, pois cada camada pode implementar suas próprias medidas de segurança. No entanto, a comunicação entre camadas deve ser cuidadosamente gerenciada para evitar vulnerabilidades.

### Conclusão

A escolha da arquitetura de um sistema operacional tem um impacto significativo tanto no custo de desenvolvimento e manutenção quanto na segurança da informação. Arquiteturas monolíticas podem ser mais rápidas e baratas de desenvolver inicialmente, mas podem acarretar custos de manutenção mais altos e maiores riscos de segurança. Por outro lado, arquiteturas microkernel e em camadas podem exigir um investimento inicial maior, mas oferecem vantagens em termos de manutenção e segurança.

## Questão
Com base no texto sobre a estrutura de sistemas operacionais, analise como as diferentes arquiteturas (monolítica, microkernel e camadas) impactam o custo com a equipe de desenvolvimento e a segurança do sistema operacional. Em sua resposta, considere os seguintes pontos:
- Complexidade de implementação e manutenção
- Necessidade de especialização da equipe
- Potenciais vulnerabilidades de segurança
- Facilidade de atualização e correção de falhas

## Resposta:
Arquitetura Monolítica: a implementação é inicialmente simples, mas a manutenção é complexa conforme o sistema cresce,
isso porque qualquer mudança feita pode comprometer o núcleo inteiro, então é necessário a realização de muitos testes para
garantir um bom funcionamento. Por isso, a equipe precisa estar atenta nas alterações do código, sendo necessário um
conhecimento vasto sobre o sistema. A segurança desse sistema é de certa forma vulnerável por causa da integração de todos
os componentes em um único bloco de código. Sendo assim, correções de falhas são complexas, bem como sua manutenção. Um
exemplo de SO monolítico é o próprio Linux.  
Arquitetura Microkernel: a implementação é complexa porque o núcleo é construído de forma que o máximo de funcionalidades
possíveis ocorram fora dele, já a manutenção é facilitada devido a isso, porque alterações acontecem de forma que não
impacte o núcleo, reduzindo o risco de falhas no sistema inteiro. A equipe precisa ser especializada não apenas no
entendimento do núcleo, mas também nas interfaces e processos que acontecem alheio a ele. A segurança dessa arquitetura
é bastante alta por ser possível isolar os processos, fazendo com que o sistema não seja inteiramente comprometido quando
algum deles sofre um tipo de falha. A correção de falhas também se torna facilitada por meio da separação desses processos.
Um exemplo de SO que utiliza a arquitetura microkernel é o Minix.  
Arquitetura em Camadas: possui uma complexidade intermediária porque como é um SO dividido em camadas, cada uma delas possui
um papel específico, cada uma com sua dificuldade de implementação e manutenção, mas, nesse tipo de sistema, os problemas
também podem ser isolados e resolvidos sem que isso afete o sistema como um todo. A especialização da equipe precisa ser
muito bem distribuida entre várias áreas diferentes, porque cada camada é tratada de uma forma diferente das demais.
A segurança desse tipo de arquitetura é também muito boa porque cada camada é capaz de apresentar um recurso de segurança
específico para suas especialidades. A atualização e correção de falhas nesse sistema também é facilitada pela separação
de responsabilidades entre as camadas. Um exemplo de SO que utiliza a arquitetura em camadas é o Windows NT.

# Questão 3. Introdução à Segurança de Sistemas Operacionais

## Texto informativo

A segurança de um sistema operacional é um aspecto crucial que visa proteger os recursos do sistema contra acessos não autorizados, ataques maliciosos e falhas. Um sistema operacional seguro deve garantir a integridade, confidencialidade e disponibilidade dos dados e serviços. Para alcançar esses objetivos, várias técnicas e mecanismos são implementados, incluindo:

1. **Controle de Acesso**: Define quem pode acessar o sistema e quais recursos podem ser utilizados. Isso é feito através de autenticação (verificação de identidade) e autorização (permissão de acesso).

2. **Criptografia**: Utilizada para proteger dados em trânsito e em repouso, garantindo que apenas usuários autorizados possam acessar informações sensíveis.

3. **Auditoria e Monitoramento**: Registra atividades do sistema para detectar e responder a comportamentos suspeitos ou anômalos.

4. **Isolamento de Processos**: Garante que os processos sejam executados em ambientes isolados, evitando que um processo comprometa a segurança de outro.

5. **Atualizações e Patches**: Manter o sistema operacional atualizado é essencial para corrigir vulnerabilidades conhecidas e proteger contra novas ameaças.


## Questão

Considerando os mecanismos de segurança discutidos, analise como a implementação de controles de acesso e criptografia pode impactar a performance e a usabilidade de um sistema operacional. Em sua resposta, aborde os seguintes pontos:
- Benefícios e desafios de cada mecanismo
- Impacto na experiência do usuário
- Exemplos de situações onde esses mecanismos são críticos

## Resposta:
Controle de Acesso: Possui uma função fundamental que define quem possui acesso a determinados recursos do sistema, mas a 
implementação e configuração pode se dar de forma complexa. O usuário pode ter dificuldade para manusear os recursos
disponíveis, principalmente se for necessário muitos passos para se autenticar. Esse tipo de controle é crítico por exemplo
em uma empresa que faz uso de informações pessoais como dados dados financeiros ou documentos de identidade, por exemplo
em sistemas bancários ou hospitais.  
Criptografia: Garante que dados não consigam ser legíveis ou usados sem que haja uma ferramenta de descriptografia, mas o
sistema pode ficar sobrecarregado devido a funcionalidade de criptografia caso os recursos da máquina sejam limitados. 
O usuário pode perceber atrasos ou lentidão em certas tarefas, mas se o processo de critpografia acontecer de forma
transparente, a experiência do usuário pode não ser afetada a não ser que ele seja o responsável pela própria criptografia
manualmente. Um exmeplo crítico de necessidade dessa segurança também é a presença em sistemas que envolvam transações
financeiras.  
Auditoria e Monitoramento: Auxilia na identificação de sistemas suspeitos, falhas como acessos não autorizados, mas esse
tipo de segurança pode exigir muitos recursos como capacidade de armazenamento e processamento para possíveis registros de 
falhas ou coisas relacionadas. O usuário normalmente não irá ter sua experiência afetada por essa segurança. Ambientes 
corporativos são exemplos de situações onde a necessidade dessa segurança é crítica.  
Isolamento de Processos: Beneficia no funcionamento de que cada processo funcione utilizando seu espaço de memória, não
interferindo nos outros, sendo assim uma possível falha não afeta o sistema completamente, porém a criação de sistemas
isolados acaba exigindo mais recursos de hardware do que o convencional. O usuário terá uma experiência estável e com menos
propenção à falhas por causa dessa segurança. Um exemplo crítico são servidores em nuvem, que utilizam VMs (máquinas 
virtuais) para realizar esse isolamento de processos.
Atualizações e Patches: Mantém o sistema atualizado de forma que falhas e vulnerabilidades sejam conhecidas, consertadas ou
evitadas, mas existem riscos de atualizações que sejam acompanhadas por bugs ou outros problemas inesperados, além de que
diversas tarefas precisam ser suspensas para a realização de uma atualização. Isso pode afetar a experiência do usuário, 
principalmente se for uma atualização demorada. Entretanto, as atualizações trazem muitos benefícios de performance, 
segurança e outras coisas. Um exemplo crítico de utilização é a aplicação de atualizações em programas ou aplicativos.  

# Questão 4. Custo de Processamento versus Algoritmo Ótimo de Escalonamento

## Texto informativo

O escalonamento de processos é uma função crítica de um sistema operacional, responsável por determinar a ordem em que os processos são executados pelo processador. O objetivo é maximizar a eficiência do sistema, garantindo que os recursos sejam utilizados de maneira justa e eficaz. No entanto, encontrar o algoritmo de escalonamento ótimo envolve um equilíbrio delicado entre o custo de processamento e a eficiência do escalonamento.

### Custo de Processamento

O custo de processamento refere-se ao tempo e aos recursos necessários para executar um algoritmo de escalonamento. Algoritmos mais complexos podem oferecer melhores resultados em termos de tempo de resposta e utilização do processador, mas também podem exigir mais recursos computacionais para tomar decisões de escalonamento. Isso pode incluir tempo de CPU, memória e outras operações de sistema.

### Algoritmo Ótimo de Escalonamento

Um algoritmo ótimo de escalonamento é aquele que maximiza a eficiência do sistema operacional, minimizando o tempo de espera dos processos, o tempo de resposta e o tempo de retorno. Alguns dos algoritmos de escalonamento mais comuns incluem:

- **First-Come, First-Served (FCFS)**: Simples e fácil de implementar, mas pode levar a longos tempos de espera para processos curtos.
- **Shortest Job Next (SJN)**: Minimiza o tempo médio de espera, mas pode ser difícil de implementar devido à necessidade de prever o tempo de execução dos processos.
- **Round Robin (RR)**: Oferece uma abordagem justa, atribuindo fatias de tempo iguais a todos os processos, mas pode resultar em maior sobrecarga de contexto.
- **Priority Scheduling**: Processos com maior prioridade são executados primeiro, mas pode levar à inanição de processos de baixa prioridade.

## Questão

Considerando os conceitos de custo de processamento e algoritmo ótimo de escalonamento, analise como diferentes algoritmos de escalonamento podem impactar a performance de um sistema operacional em termos de tempo de resposta, tempo de espera e utilização do processador. Em sua resposta, aborde os seguintes pontos:
- Vantagens e desvantagens de pelo menos dois algoritmos de escalonamento
- Impacto do custo de processamento na escolha do algoritmo
- Exemplos de situações onde um algoritmo pode ser preferível a outro

## Resposta:
First-Come, First-Served (FCFS): É baseado na ordem de chegada de processos, o que faz com que sua implementação seja fácil
de entender e implementar, mas o problema ocorre quando, por causa dessa ordem, certos processos curtos ficam na espera
pela conclusão de processos longos, fazendo com que haja atraso em processos mais básicos.  
Round Robin (RR): Todos os processos recebem o mesmo tempo de execução, o que é benéfico para sistemas onde o tempo de
resposta é crucial, mas isso pode acabar sobrecarregando o processador, fazendo com que processos sejam frequentemente
interrompidos ou alternados. Isso acaba sendo um problema em sistemas que possuem processos com tempos de execução
desiguais.  
Esses dois tipos de algoritmos são consideravelmente baratos no quesito de custo de processamento, porque neles não há
cálculos muito complexos. Porém, eles podem não ser os ideais para a melhor execução por parte do processador ou por 
questões de otimização de tempo em certos cenários, o que justificaria a escolha de algoritmos mais caros, porém mais
sofisticados, como por exemplo o SJN ou o Priority Scheduling, que consegue determinar qual processo deve ser executado
em sequência, principalmente quando a previsão de tempo requerido ou gestão de prioridades necessitam de operações extas.  
Em situações de sistemas em tempo real, por exemplo, o Priority Scheduling é geralmente o escolhido porque nesses casos a 
prioridade e o tempo de resposta são requisitos críticos. Entretanto, em servidores web, onde o objetivo é a garantia de 
tempos de resposta rápidos para uma grande carga de solicitações, o Round Robbin (RR) pode ser uma escolha melhor, porque
ele oferece uma distribuição de tempo sem a necessidade priorização de processos. Sendo assim, a escolha do algoritmo de
escalonamento depende do sistema referido, ou seja, das necessidades dele, do custo de processamento, etc.

# Questão 5. Aplicativo em python vs aplicativos em c

## Questão

Explique o caminho que as instruções seguem desde um aplicativo escrito em Python e um aplicativo escrito em linguagem C até serem executadas pelo hardware. Em sua resposta, considere os seguintes pontos:
- O papel do interpretador no caso do Python
- O processo de compilação no caso do C
- A interação entre o kernel do sistema operacional e os drivers de dispositivo
- A tradução final das instruções para o formato binário (0 e 1) executado pelo hardware

## Resposta:
Python: por ser uma linguagem interpretada, o interpretador primeiramente lê o código-fonte do arquivo .py, depois o código
é compilado em bytecode, não sendo diretamente executado pelo processador, mas podendo ser interpretada pela PVM, que é a
máquina virtual od Python. Dessa forma, o código não é traduzido diretamente para o código de máquina do processador. Depois, o kernel do sistema operacional e os drivers dos dispositivos gerenciam as interações, fazendo a comunicação entre o código em questão e o hardware, podendo usar os drivers para acesso de disco rígido ou placa de vídeo, por exemplo. No caso, o interpretador pode precisar interagir com o SO através de chamadas de sistema para a realização de tarefas como abrir arquivos ou se comunicar com a rede. Por fim, a tradução final das instruções ocorre antes da execução pelo processador, aqui no caso o interpretador traduz o código para bytecode e este código é interpretado pela PVM. Sendo sasim, o código final é produzido dinamicamente durante a execução do programa.  
C: por ser uma linguagem compilada, o código-fonte do tipo .c é passado para um compilador, por exemplo o gcc, e depois é convertido para código de máquina específico do SO ou do tipo de processador onde o programa será executado. Depois disso, o compilador gera um arquivo do tipo .o que contém o código de máquina, esse arquivo é linkado com possíveis bilbiotecas ou dependências necessárias e acaba virando um arquivo executável. Por fim, o  SO carrega o binário na memória e o processador executa o arquivo diretamente, interpretando as instruções do código de máquina. O kernel do SO e os drivers funcionam de forma semelhante com o Python, diferentemente de que em C, as interações são feitas diretamente através de chamadas de sistema ou APIs. Por fim, a tradução final ocorre quando o arquivo binário contendo o código de máquina é carregado na memória e executado pelo processador.  
Comparando as duas linguagens, percebe-se que o código C é mais rápido de se executar que o código Python, por não precisar de uma camada adicional de interpretação, que no caso seria a PVM. Entretanto, o código Python tende a ser mais flexível e interativo, por não necessitar de compilação, isso faz com que testes e desenvolvimento dinâmico sejam mais possibilitados.
