# Arquiteturas de Sistemas Operacionais

## Informações gerais

- Capítulo: [Arquitetura de SO](https://wiki.inf.ufpr.br/maziero/lib/exe/fetch.php?media=socm:socm-03.pdf)
- Disciplina: *sistemas operacionais*
- Livro: [Sistemas Operacionais: Conceitos e Mecanismos](https://wiki.inf.ufpr.br/maziero/doku.php?id=socm:start)

## Aluno

- nome: Larissa Samara X. P. de Lima
- matrícula: 20211014040070

## Respostas dos exercícios

  1.
Fornecer uma interface simplificada para os recursos de hardware, ocultando a complexidade do hardware subjacente.Gerenciar e alocar recursos do sistema (CPU, memória, dispositivos de entrada/saída) de forma eficiente entre múltiplas aplicações.

  2.
Para desenvolvedores de aplicações: A abstração simplifica o desenvolvimento de aplicações ao fornecer uma interface de alto nível para o hardware, facilitando a escrita de código portável e manutenível.
Para desenvolvedores de sistemas operacionais: A abstração ajuda a modularizar o sistema operacional, tornando mais fácil adicionar novos dispositivos de hardware ou modificar os existentes sem afetar o sistema como um todo.
	
  3. 
Vantagens:
Melhor utilização do sistema: Aumenta a eficiência do uso dos recursos do computador.
Maior capacidade de resposta: Permite que o sistema responda mais rapidamente às solicitações do usuário.
Execução simultânea de múltiplas aplicações: Possibilita a execução de várias tarefas ao mesmo tempo.
Desafios:
Algoritmos de escalonamento: Desenvolver algoritmos eficientes para distribuir o tempo de processador entre as tarefas.
Sobrecarga de troca de contexto: Minimizar o tempo gasto para alternar entre diferentes processos.
Garantia de justiça entre processos concorrentes: Assegurar que todos os processos recebam uma quantidade justa de tempo de processador.

  4.
Características:
Tempos de resposta previsíveis e comportamento determinístico.
Classificações:
Tempo real rígido (hard real-time): Perder prazos pode ter consequências catastróficas (por exemplo, sistemas de controle de voo).
Tempo real flexível (soft real-time): Perder prazos degrada o desempenho, mas não causa falhas catastróficas (por exemplo, aplicações multimídia).

  5.
[T] Deve ter um comportamento temporal previsível, com prazos de resposta claramente definidos.

[S] Sistema operacional usado por uma empresa para executar seu banco de dados corporativo.

[E] São tipicamente usados em telefones celulares e sistemas eletrônicos dedicados. 

[D] Neste tipo de sistema, a localização física dos recursos do sistema computacional é transparente para os usuários. 

[M] Todos os recursos do sistema têm proprietários e existem regras controlando o acesso aos mesmos pelos usuários. 

[E] A gerência de energia é muito importante neste tipo de sistema. 

[K] Sistema que prioriza a gerência da interface gráfica e a interação com o usuário. 

[S] Construído para gerenciar de forma eficiente grandes volumes de recursos. 

[K] O MacOS X é um exemplo típico deste tipo de sistema. 

[E] São sistemas operacionais compactos, construídos para executar aplicações específicas sobre plataformas com poucos recursos. 

  6.
(d) Incorreta. Sistemas de tempo real priorizam tarefas com base em prazos, não em interação com o usuário.


