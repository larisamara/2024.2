# Conceito de tarefas

## Informações gerais

- Capítulo: [Conceito de tarefas](https://wiki.inf.ufpr.br/maziero/lib/exe/fetch.php?media=socm:socm-04.pdf)
- Disciplina: *sistemas operacionais*
- Livro: [Sistemas Operacionais: Conceitos e Mecanismos](https://wiki.inf.ufpr.br/maziero/doku.php?id=socm:start)

## Aluno

- nome: Larissa Samara XAvier Pedro de Lima
- matrícula: 20211014040070

## Respostas dos exercícios
 
1.Time sharing (compartilhamento de tempo) é uma técnica que permite a execução de múltiplas tarefas em um único processador. A ideia é dividir o tempo do processador em pequenos intervalos (quanta) e alocar cada quantum a uma tarefa diferente. Isso cria a ilusão de que as tarefas estão sendo executadas simultaneamente, mesmo que o processador esteja executando apenas uma delas em cada momento.

A importância do time sharing reside na capacidade de aumentar a utilização do processador, permitindo que diversos usuários ou processos compartilhem um único computador de forma eficiente. Além disso, essa técnica torna os sistemas operacionais mais responsivos, pois as tarefas interativas recebem pequenas porções de tempo de processamento com frequência, evitando que o usuário precise esperar longos períodos por uma resposta.


2.A duração do quantum é um parâmetro importante em sistemas de tempo compartilhado, pois afeta diretamente o desempenho e a responsividade do sistema. A escolha do tamanho do quantum envolve um trade-off:

Quanta curtos: Permitem maior interatividade, pois as tarefas trocam de contexto com mais frequência. No entanto, podem gerar uma sobrecarga excessiva devido ao grande número de trocas de contexto.
Quanta longos: Reduzem a sobrecarga de trocas de contexto, mas podem prejudicar a responsividade, especialmente para tarefas com alta prioridade ou que exigem respostas rápidas.
A escolha do tamanho do quantum depende de diversos fatores, como:

Número de tarefas: Quanto maior o número de tarefas, menores devem ser os quanta para garantir que todas as tarefas recebam uma fatia de tempo razoável.
Tipo de tarefas: Tarefas interativas geralmente requerem quanta menores para garantir uma boa resposta.
Características do hardware: A velocidade do processador e a latência de memória influenciam a escolha do tamanho do quantum.
Política de escalonamento: Diferentes políticas de escalonamento podem exigir tamanhos de quantum diferentes.


3.Estado faltante (t6): A transição t6 representa a passagem de um estado suspenso para o estado pronto. Isso ocorre quando a condição que estava bloqueando a tarefa é satisfeita (por exemplo, um recurso se torna disponível, um evento ocorre).

Significado dos estados e transições:

N (Nova): A tarefa está sendo criada e inicializada.

P (Pronta): A tarefa está pronta para ser executada e aguarda na fila de prontos.

E (Executando): A tarefa está sendo executada pelo processador.

S (Suspensa): A tarefa está bloqueada aguardando algum evento ou recurso.

T (Terminada): A tarefa concluiu sua execução ou foi abortada.

t1: A tarefa é criada e entra no estado pronto.

t2: A tarefa sai da fila de prontos e começa a executar.

t3: A tarefa é preemptada (interrompida) e retorna à fila de prontos.

t4: A tarefa é bloqueada aguardando um evento ou recurso.

t5: A tarefa é desbloqueada e retorna à fila de prontos.

t6: A tarefa sai do estado suspenso e vai para a fila de prontos.

e1: Criação de uma nova tarefa.

e2: Início da execução de uma tarefa.

e3: Preempção de uma tarefa.

e4: Bloqueio de uma tarefa.

e5: Desbloqueio de uma tarefa.

4.
E → P: Possível. Ocorre quando a tarefa é preemptada ou quando atinge o fim do seu quantum.
E → S: Possível. Ocorre quando a tarefa precisa de um recurso que não está disponível no momento.
S → E: Possível. Ocorre quando o recurso aguardado pela tarefa se torna disponível e ela é colocada na fila de prontos.
P → N: Impossível. Uma tarefa não pode voltar ao estado de nova após ter sido criada.
S → T: Possível. Uma tarefa pode ser terminada enquanto está suspensa (por exemplo, se o processo pai for encerrado).
E → T: Possível. Ocorre quando a tarefa completa sua execução ou é abortada.
N → S: Impossível. Uma tarefa recém-criada normalmente entra no estado pronto.
P → S: Possível. Uma tarefa pronta pode ser bloqueada se tentar acessar um recurso indisponível.
Há uma tarefa neste estado para cada processador do sistema: Não se aplica a nenhum estado específico. O número de tarefas em execução depende da carga do sistema e da política de escalonamento.
A tarefa aguarda a ocorrência de um evento externo: Estado Suspenso (S).

5.
O código da tarefa está sendo carregado: N (Nova)
As tarefas são ordenadas por prioridades: P (Pronta)
A tarefa sai deste estado ao solicitar uma operação de entrada/saída: E (Executando)
Os recursos usados pela tarefa são devolvidos ao sistema: T (Terminada)
A tarefa vai a este estado ao terminar seu quantum: P (Pronta)
A tarefa só precisa do processador para poder executar: P (Pronta)
O acesso a um semáforo em uso pode levar a tarefa a este estado: S (Suspensa)
A tarefa pode criar novas tarefas: E (Executando)
Há uma tarefa neste estado para cada processador do sistema: Nenhum estado específico.
A tarefa aguarda a ocorrência de um evento externo: S (Suspensa)
