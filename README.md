# DevOps Azure Challenge

Este é um desafio para testar seus conhecimentos de DevOps na Azure;

O objetivo é avaliar a sua forma de estruturação e autonomia em decisões para construir algo escalável utilizando o Infra as Code.

[SPOILER] As instruções de entrega e apresentação do challenge estão no final deste Readme (=

### Antes de começar
 
- Considere como deadline da avaliação a partir do início do teste. Caso tenha sido convidado a realizar o teste e não seja possível concluir dentro deste período, avise a pessoa que o convidou para receber instruções sobre o que fazer.
- Documentar todo o processo de investigação para o desenvolvimento da atividade (README.md no seu repositório); os resultados destas tarefas são tão importantes do que o seu processo de pensamento e decisões à medida que as completa, por isso tente documentar e apresentar os seus hipóteses e decisões na medida do possível.


## **Parte 1 - Configuração do Servidor**

A sua tarefa consiste em configurar um servidor baseado na nuvem e instalar e configurar alguns componentes básicos.


1. Configurar um servidor na Azure, executando uma versão Ubuntu LTS.
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

## Readme do Repositório

- Deve conter o título do projeto
- Uma descrição sobre o projeto em frase
- Deve conter uma lista com linguagem, framework e/ou tecnologias usadas
- Como instalar e usar o projeto (instruções)
- Não esqueça o [.gitignore](https://www.toptal.com/developers/gitignore)
- Se está usando github pessoal, referencie que é um challenge by coodesh:  

>  This is a challenge by [Coodesh](https://coodesh.com/)

## Finalização e Instruções para a Apresentação

1. Adicione o link do repositório com a sua solução no teste
2. Adicione o link da apresentação do seu projeto no README.md.
3. Verifique se o Readme está bom e faça o commit final em seu repositório;
4. Envie e aguarde as instruções para seguir. Sucesso e boa sorte. =)

## Suporte

Use a [nossa comunidade](https://discord.gg/rdXbEvjsWu) para tirar dúvidas sobre o processo ou envie uma mensagem diretamente a um especialista no chat da plataforma. 


