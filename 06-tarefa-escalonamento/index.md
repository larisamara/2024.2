# Escalonamento de tarefas

## Informações gerais

- Capítulo: [Escalonamento de tarefas](https://wiki.inf.ufpr.br/maziero/lib/exe/fetch.php?media=socm:socm-06.pdf)
- Disciplina: *sistemas operacionais*
- Livro: [Sistemas Operacionais: Conceitos e Mecanismos](https://wiki.inf.ufpr.br/maziero/doku.php?id=socm:start)

## Aluno

- nome: Larissa Smamara Xavier Pedro de Lima
- matrícula: 20211014040070

## Respostas dos exercícios

1. Escalonamento Round-Robin
Escalonamento Round-Robin é um algoritmo de escalonamento de processos que distribui o tempo de CPU de forma equitativa entre todos os processos prontos para execução. Imagine uma fila circular onde os processos aguardam sua vez. Cada processo recebe um "fatia de tempo" (quantum) para executar. Se o processo não terminar dentro desse tempo, ele é interrompido e colocado no final da fila, e o próximo processo da fila tem sua vez.

Exemplo: Pense em uma impressora compartilhada por várias pessoas. Cada pessoa envia um documento para imprimir e espera sua vez. O sistema operacional utiliza o Round-Robin para garantir que todos os documentos sejam impressos em um tempo razoável, sem que um documento específico demore muito para ser processado.

2. Eficiência do Sistema Round-Robin
A eficiência (E) de um sistema Round-Robin é influenciada por vários fatores, como o quantum (tq), o tempo de troca de contexto (ttc) e a porcentagem de tempo que um processo gasta em E/S (p). A eficiência pode ser definida como a proporção de tempo que a CPU está efetivamente executando processos.

Fórmula da Eficiência:

E = (tq - ttc) / tq * (1 - p)
tq - ttc: Representa o tempo útil de processamento por quantum, após descontar o tempo gasto na troca de contexto.
(1 - p): Representa a proporção de tempo que o processo está efetivamente executando instruções, considerando o tempo gasto em E/S.
Análise da Fórmula:

Aumentando tq: Aumenta a eficiência, pois permite que os processos executem por mais tempo antes de serem interrompidos.
Diminuindo ttc: Aumenta a eficiência, pois diminui o tempo perdido com trocas de contexto.
Diminuindo p: Aumenta a eficiência, pois os processos passam menos tempo esperando por E/S.
3. Técnica de Aging
Aging é uma técnica utilizada em sistemas operacionais para evitar que processos com baixa prioridade permaneçam indefinidamente na fila de espera, sofrendo de starvation. A ideia é aumentar gradualmente a prioridade de um processo ao longo do tempo que ele permanece na fila, fazendo com que ele seja eventualmente escolhido para execução.

Para que serve:

Evita o starvation: Garante que todos os processos sejam executados, mesmo aqueles com prioridades mais baixas.
Melhora a responsividade do sistema: Ao evitar que processos permaneçam por muito tempo na fila, o sistema responde mais rapidamente às novas requisições.
Como funciona:

A cada intervalo de tempo, a prioridade de todos os processos na fila é incrementada em uma quantidade pequena. Dessa forma, processos que estão há mais tempo na fila tendem a ter prioridades mais altas e são escolhidos para execução antes dos processos que chegaram mais recentemente.

4. Modificações para Escalas de Prioridades Negativas
Para suportar uma escala de prioridades negativas no algoritmo de envelhecimento descrito na Seção 6.4.6, seria necessário adaptar a lógica de atualização da prioridade. Uma possível abordagem:

Limite inferior para a prioridade: Definir um valor mínimo para a prioridade, abaixo do qual ela não pode ser reduzida.
Taxa de envelhecimento diferenciada: Utilizar uma taxa de envelhecimento maior para processos com prioridades negativas, de forma que eles "envelheçam" mais rapidamente e tenham suas prioridades aumentadas mais rapidamente.
Prioridade baseada em um valor absoluto: Converter as prioridades negativas em valores absolutos antes de aplicar o algoritmo de envelhecimento.

5. 
FCFS (First-Come, First-Served): A primeira tarefa a chegar é a primeira a ser executada.
SJF (Shortest Job First): A tarefa com menor tempo de execução é executada primeiro.
SRTF (Shortest Remaining Time First): Uma variação do SJF, onde a tarefa com menor tempo de execução restante é sempre escolhida para ser executada.
PRIO: A tarefa com maior prioridade é executada primeiro.
RR (Round Robin): Cada tarefa recebe um quantum de tempo para executar. Se a tarefa não terminar nesse tempo, ela é interrompida e colocada no final da fila.


Exemplo (FCFS):
   
|**Tempo**| **Tarefa em Execução**| 
| :-----------------: | :-----------------: | 
|0-5|t1|
|5-9|t2|
|9-15|t3|
|14-20|t4|
|20-24|t5|

Cálculo dos Tempos (FCFS):

|**Tarefa**| **Tempo de Carga**| **Tempo de Término**| **Tempo de Vida**| **Tempo de Espera**|
| :-----------------: | :-----------------: | :-----------------: | :-----------------: | :-----------------: | 
|t1|0|5|5|0|
|t2|0|9|9|5|
|t3|3|14|11|8|
|t4|5|20|15|15|
|t5|7|24|17|17|

6.
FCFS
|**Tempo**| **Tarefa em Execução**| 
| :-----------------: | :-----------------: | 
|0-5|t1|
|5-11|t2|
|11-13|t3|
|13-19|t4|
|19-23|t5|

SJF
|**Tempo**| **Tarefa em Execução**| 
| :-----------------: | :-----------------: | 
|0-2|t3|
|2-8|t2|
|8-14|t1|
|14-20|t4|
|20-24|t5|

SRTF
|**Tempo**| **Tarefa em Execução**| 
| :-----------------: | :-----------------: | 
|0-2|t3|
|2-8|t2|
|8-13|t1|
|13-19|t4|
|19-23|t5|

PRIO
|**Tempo**| **Tarefa em Execução**| 
| :-----------------: | :-----------------: | 
|0-6|t2|
|6-8|t3|
|8-14|t1|
|14-20|t4|
|20-24|t5|

RR(TQ = 2)
|**Tempo**| **Tarefa em Execução**| 
| :-----------------: | :-----------------: | 
|0-2|t1|
|2-4|t2|
|4-6|t3|
|6-8|t4|
|8-10|t1|
|...|...|
