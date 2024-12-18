# Arquiteturas de Sistemas Operacionais

## Informações gerais

- Capítulo: [Arquitetura de SO](https://wiki.inf.ufpr.br/maziero/lib/exe/fetch.php?media=socm:socm-03.pdf)
- Disciplina: *sistemas operacionais*
- Livro: [Sistemas Operacionais: Conceitos e Mecanismos](https://wiki.inf.ufpr.br/maziero/doku.php?id=socm:start)

## Aluno

- nome: Larissa Samara Xavier Pedro de Lima
- matrícula: 20211014040070

## Respostas dos exercícios

# Arquiteturas de Sistemas Operacionais

## Informações gerais

- Capítulo: [Arquitetura de SO](https://wiki.inf.ufpr.br/maziero/lib/exe/fetch.php?media=socm:socm-03.pdf)
- Disciplina: *sistemas operacionais*
- Livro: [Sistemas Operacionais: Conceitos e Mecanismos](https://wiki.inf.ufpr.br/maziero/doku.php?id=socm:start)

## Aluno

- nome: Larissa Samara
- matrícula: 20211014040070

## Respostas dos exercícios

Exercício 
1. 

|**Arquitetura**| **Vantagens**| **Desvantagens**|
| :-----------------: | :-----------------: | :-----------------: | 
|Monolítico |Alto desempenho, simplicidade|Baixa robustez, dificuldade de manutenção, menor modularidade|
|Micronúcleo  | Alta modularidade, flexibilidade, robustez |	Baixo desempenho, complexidade de implementação|
|Camadas | Modularidade, hierarquia clara	|Desempenho pode ser afetado por múltiplas camadas, dificuldade em definir limites entre camadas|
| Híbrido       |      Combinação de vantagens de monolítico e micronúcleo	| Complexidade na escolha de quais componentes colocar em cada parte|
|Máquinas virtuais	|  Isolamento, consolidação de servidores, portabilidade	|Sobrecarga de desempenho, complexidade de gerenciamento|
|Contêineres  |   Isolamento, leveza, agilidade	|Compartilham o mesmo kernel, menor isolamento que máquinas virtuais|
|Exokernels |Alto desempenho, flexibilidade	|Complexidade de desenvolvimento, menor abstração para o programador|
|Unikernels |Alto desempenho, leveza	|Dificuldade de desenvolvimento, menor flexibilidade|

2. O núcleo do Linux é monolítico com características híbridas. Embora a maior parte do código seja executada em modo kernel e tenha acesso direto a hardware, o Linux introduziu módulos carregáveis que permitem adicionar ou remover funcionalidades sem recompilar todo o núcleo. Essa modularidade é uma característica dos sistemas micronúcleo, mas a base do Linux ainda é monolítica.

3. 
(a) Incorreta: Uma máquina virtual de sistema é construída para suportar um sistema operacional completo, não apenas uma aplicação específica.

(b) Um hipervisor convidado executa dentro de outro sistema operacional, como uma aplicação.

(c) Em um sistema operacional micronúcleo, a maioria dos componentes executa como processos no espaço do usuário, não dentro do núcleo.

(d) Núcleos monolíticos são menos robustos e mais difíceis de manter devido ao alto acoplamento entre seus componentes.

(e) Em um sistema operacional micronúcleo, a comunicação entre componentes se dá através de trocas de mensagens.
