# Implementação de tarefas

## Informações gerais

- Capítulo: [Implementação de tarefas](https://wiki.inf.ufpr.br/maziero/lib/exe/fetch.php?media=socm:socm-05.pdf)
- Disciplina: *sistemas operacionais*
- Livro: [Sistemas Operacionais: Conceitos e Mecanismos](https://wiki.inf.ufpr.br/maziero/doku.php?id=socm:start)

## Aluno

- nome: Larissa Samara Xavier Pedro de Lima
- matrícula: 20211014040070

## Respostas dos exercícios

1.Um TCB (Task Control Block), ou Bloco de Controle de Tarefa em português, é uma estrutura de dados fundamental em sistemas operacionais. Ele serve como um repositório de informações sobre um processo ou thread em execução. Imagine o TCB como um dossiê completo de um processo, contendo todos os detalhes necessários para que o sistema operacional possa gerenciá-lo de forma eficiente.

2.Diagrama de Tempo (simplificado):

![image](https://github.com/user-attachments/assets/664f677a-9fbf-4f45-8ff2-ab34fe98c61b)


A saída do programa será:

Valor de x: 2

3.Impressão de 'X': Cada processo, incluindo o pai e todos os filhos, imprime uma letra 'X'. Quando o programa é executado com a linha de comando a.out 4 3 2 1, serão impressas 15 letras 'X' na tela.

4.Threads, ou fios de execução, são como subprogramas dentro de um processo. Imagine um processo como uma tarefa complexa, como cozinhar um jantar. Cada etapa da receita, como preparar o arroz, refogar a carne e fazer a salada, pode ser vista como uma thread dentro do processo de cozinhar.

Concorrência: Permitem que múltiplas tarefas sejam executadas "simultaneamente" dentro de um mesmo processo, aumentando a eficiência e responsividade de um programa. Compartilhamento de recursos: Threads dentro de um mesmo processo compartilham a mesma memória e outros recursos, o que facilita a comunicação entre elas. Melhor aproveitamento de múltiplos núcleos: Em sistemas com múltiplos núcleos de processador, as threads podem ser distribuídas por diferentes núcleos, aumentando o desempenho.

5.Melhor desempenho: Threads compartilham o mesmo espaço de endereço, o que reduz a sobrecarga de criação e gerenciamento em comparação com processos. Isso permite que tarefas sejam executadas em paralelo dentro de um mesmo processo, aproveitando melhor os recursos do sistema. Responsividade: Threads podem tornar um programa mais responsivo, permitindo que uma parte do programa continue a executar enquanto outra está bloqueada, por exemplo, esperando por uma entrada do usuário. Economia de recursos: A criação de threads é geralmente mais leve que a criação de processos, o que economiza memória e outros recursos do sistema. Facilidade de comunicação: Threads dentro de um mesmo processo podem se comunicar de forma mais fácil, utilizando variáveis compartilhadas e outras técnicas de sincronização.

6.Tarefas altamente sequenciais: Se uma tarefa depende fortemente de resultados anteriores, a criação de múltiplas threads pode não trazer ganhos significativos em desempenho, pois as threads terão que esperar pela conclusão de etapas anteriores. Problemas com alto overhead de sincronização: Se a comunicação e sincronização entre as threads forem muito frequentes, o custo dessas operações pode anular os benefícios do paralelismo.

7.(a) Tem a implementação mais simples, leve e eficiente: Many-to-one (N:1) (b) Multiplexa os threads de usuário em um pool de threads de núcleo: Many-to-many (N:M) (c) Pode impor uma carga muito pesada ao núcleo: One-to-one (1:1) (d) Não permite explorar a presença de várias CPUs pelo mesmo processo: Many-to-one (N:1) (e) Permite uma maior concorrência sem impor muita carga ao núcleo: Many-to-many (N:M) (f) Geralmente implementado por bibliotecas: Many-to-one (N:1) e Many-to-many (N:M) (g) É o modelo implementado no Windows NT e seus sucessores: One-to-one (1:1) (h) Se um thread bloquear, todos os demais têm de esperar por ele: Many-to-one (N:1) (i) Cada thread no nível do usuário tem sua correspondente dentro do núcleo: One-to-one (1:1) (j) É o modelo com implementação mais complexa: Many-to-many (N:M)

8.
