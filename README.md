# Azure Challenge 20200921

Por favor, complete o seguinte desafio para a sua entrevista online. Terá de documentar o seu processo e apresentá-lo na entrevista (utilizando um PowerPoint ou apresentação semelhante), bem como demonstrar o resultado das tarefas no servidor durante a entrevista técnica.

Os resultados destas tarefas são menos importantes do que o seu processo de pensamento e decisões à medida que as completa, por isso tente documentar e apresentar os seus hipóteses e decisões na medida do possível.


## **Parte 1 - Configuração do Servidor**

A sua tarefa consiste em configurar um servidor baseado na nuvem e instalar e configurar alguns componentes básicos.


1. Configurar um servidor na Azure (recomenda-se o freetier) executando uma versão Ubuntu LTS.
2. Instalar e configurar qualquer software que você recomendaria em uma configuração de servidor padrão sob as perspectivas de segurança, desempenho, backup e monitorização.
3. Instalar e configurar o nginx para servir uma página web HTML estática.
4. Utilizar ferramentas de automatização como Ansible e/ou Terraform.


## **Part 2 – Scripting**

Utilizando uma linguagem de script à sua escolha, construa um projeto (servido através do nginx) que possa relatar estatísticas operacionais básicas sob a forma de um objeto JSON.

As estatísticas devem incluir (como mínimo):



1. Carga actual da CPU, tempo de espera e utilização de memória (opcionalmente reportado como slab, cache, RSS, etc.)
2. Se existem actualizações pendentes (opcionalmente, reportando actualizações de segurança independentemente)
3. Utilização actual do disco e desempenho de leitura/escrita

O resultado final pode incluir quaisquer outras estatísticas que considere importantes para efeitos de monitorização do servidor. Você pode considerar a possibilidade de construir o script em cima do projeto [dstat](https://github.com/dagwieers/dstat).

O seu código deve ser entregue a um repositório Git que demonstram uma compreensão de conceitos tais como ramificação de branchs e merges requests.


## **Part 3 – Continuous Delivery**

- Desenhar e construir uma pipeline para apoiar a entrega contínua da aplicação de monitorização construída na Parte 2 no servidor configurado na Parte 1. 
- Descrever a pipeline utilizando um diagrama de fluxo e explicar o objetivo e o processo de seleção usado em cada uma das ferramentas e técnicas específicas que compõem a sua pipeline. 
- Utilizar tecnologías de CI/CD como Gitlab, Github Actions ou Azure Pipelines;

## Extras

- Configurar Tests Unitários durante o processo de CI;
- Criar uma imagem do Docker com as configurações do Server;

## Instruções para a Apresentação: 

1. Será necessário compartilhar a tela durante a vídeo chamada;
2. Deixe todos os projetos de solução previamente abertos em seu computador antes de iniciar a chamada;
3. Deixe os ambientes configurados e prontos para rodar; 
4. Prepara-se pois você será questionado sobre cada etapa e decisão do Challenge;
5. Prepare uma lista de perguntas, dúvidas, sugestões de melhorias e feedbacks (caso tenha).

## Suporte

Use o nosso canal no slack: http://bit.ly/32CuOMy para tirar dúvidas sobre o processo ou envie um e-mail para contato@coodesh.com. 

