# Seu Barriga!

[![Github Badge](https://img.shields.io/badge/-Github-000?style=flat-square&logo=Github&logoColor=white&link=https://github.com/elidiojunior/Demoday---QAlegria)](https://github.com/elidiojunior/Demoday---QAlegria)

O [Sr. Barriga](https://seubarriga.wcaquino.me/login), um app revolucionário que vai ajudá-lo a manter suas finanças em dia.

## Introdução

A equipe da BigBelly Tech deseja incrementar sua capacidade de controle de qualidade a fim de evitar que bugs atinjam seus clientes.

A fim de salvar capacidade de seus QA’s para que atuem em cenários de maior complexidade, BBT decidiu implementar Automação de Testes End to End em sua plataforma web e agora precisa da sua ajuda para desenvolver.

## Descrição do Projeto
O Seu Barriga é um app que ajuda no gerenciamento de finanças. Nele você pode criar contas, excluir e listar contas. Você vai gerenciar as finanças a partir da criação de movimentações, podendo escolher a conta que terá a movimentação e informar o interessado. Pode ser realizado o acompanhamento das movimentações criadas através do resumo mensal, onde também é possível realizar exclusões de movimentações.

## Funcionalidade a serem testadas
Realizamos os testes das seguintes funcionalidades: 
- Realizar Cadastro de Usuário
- Realizar Login de Usuário
- Adicionar Contas
- Criar movimentação
- Resumo mensal
- Realizar Reset

## Definição de Prioridade

Definição da prioridade dos cenários, avaliando a severidade (Probabilidade x Impacto) de um bug ocorrer. 

Foi utilizado a **matriz de riscos** como ferramenta para nos auxiliar na visualização da probabilidade de um determinado bug ocorrer no cenário testado e o impacto que poderia causar.

	     	   _________________________________________
              |              PROBABILIDADE              |
              |_________________________________________|____
              |  * BAIXA *  |  * MÉDIA *  |   * ALTA *  | I  |
     _________|_____________|_____________|_____________| M  |
     * ALTO * |    Média    |    Alta     |     Alta    | P  |
     _________|_____________|_____________|_____________| A  |
    * MÉDIO * |    Baixa    |    Média    |     Alta    | C  |
     _________|_____________|_____________|_____________| T  |
    * BAIXO * |    Baixa    |    Baixa    |    Média    | O  |
     _________|_____________|_____________|_____________|____|

## Casos de Teste (Planejamento)

 ### 1 - Realizar Cadastro de Usuário
 #### Cenário - Criar um novo usuário com sucesso
 **Objetivo:** Cadastrar com sucesso um novo usuário
 **Prioridade:** Alta
 **Resultado Esperado:** O sistema deve mostrar ao agora, usuário, a seguinte mensagem: "Usuário inserido com sucesso" e direcionar o usuário para a tela de login
 
 #### Cenário - Tentar criar um usuário já cadastrado
 **Objetivo:** Não realizar cadastro com email já cadastrado
 **Prioridade:** Média
 **Resultado Esperado:** Sistema deve mostrar um mensagem de erro, "Endereço de email já utilizado e não deve permitir a criação de um novo usuário
 
### 2 - Realizar Login de Usuário
 #### Cenário - Login com sucesso
**Objetivo:** Acessar o sistema
**Prioridade:** Alta
**Resultado Esperado:** O usuário deve conseguir realizar o login, visualizar na tela uma mensagem de boas vindas e ver a tela principal da ferramenta.

 #### Cenário - Usuário tentar realizar login sem está cadastrado
 **Objetivo:** Acessar o sistema sem está cadastrado
 **Prioridade:** Alta
 **Resultado Esperado:** Sistema não deve permitir o login do usuário caso não esteja cadastrado.
 
### 3 - Adicionar Contas
 #### Cenário - Adicionar conta
 **Objetivo:** Realizar a criação de uma conta com sucesso
 **Prioridade:** Baixa
 **Resultado Esperado:** Sistema deve criar uma conta para movimentações.
 
 #### Cenário - Adicionar conta sem sucesso
 **Objetivo:** Realizar a criação de uma conta com o mesmo nome de uma conta anterior
 **Prioridade:** Média
 **Resultado Esperado:** Sistema não deve permitir a criação de uma conta com o mesmo nome já cadastrado anteriormente.
  
 ### 4 - Excluir Contas
 #### Cenário - Excluir conta
 **Objetivo:** Realizar a exclusão de uma conta
 **Prioridade:** Baixa
 **Resultado Esperado:** Sistema deve permitir a exclusão da conta com sucesso.
 
 ### 5 - Criar Movimentação
 #### Cenário - Criar Movimentação
 **Objetivo:** Realizar a criação de uma movimentação atrelada a uma conta criada anteriormente.
 **Prioridade:** Baixa
 **Resultado Esperado:** Sistema deve realizar a criação de uma movimentação que irá aparecer no Resumo Mensal.
 
 ### 6 - Resumo mensal
 #### Cenário - Excluir movimentação
 **Objetivo:** Realizar a exclusão de movimentação
 **Prioridade:** Alta
 **Resultado Esperado:** Sistema deve realizar a exclusão da movimentação escolhida.
 
 ### 7 - Realizar Reset
 #### Cenário - Reset com sucesso
 **Objetivo:** Realizar o reset dos dados das contas
 **Prioridade:** Alta
 **Resultado Esperado:** Apresenta falha na aplicação, pois ao clicar no botão do reset, espera-se que os dados das contas da tela do home sejam zerados ao serem resetados com sucesso, porém os dados permanecem os mesmos sem nenhuma alteração apesar de apresentar o alerta de sucesso "Dados resetados com sucesso!"

## Instalação
Para que seja possível iniciar o projeto, precisa ser realizada a preparação do ambiente no Windows para a execução do código.

#### 1. Instalação do Python e pip
-   Baixe o [Python](https://www.python.org/downloads/);
-   Instale via executável o Python. OBS.: Defina a variável de ambiente durante a instalação ou, edite manualmente as variáveis e adicione: 

<h5>
    <p align="center">C:\Python27\;C:\Python27\Scripts</p>
</h5>

- Para verificar se a instalação deu certo, no prompt de comando (cmd) execute: 
	``python --version``  
	``pip -- version`` 
			
#### 2. Instalando o Robot Framework
-   Execute no prompt de comando (cmd) o seguinte comando para a instalação do robot framework:  
    ``pip install robotframework`` 
-   Para verificar se a instalação deu tudo certo no prompt de comando (cmd) execute:  
    ``robot --version``

Leia o [manual](https://code.google.com/archive/p/robotframework/wikis/Installation.wiki) para mais informações sobre a instalação e configuração do ambiente que você irá precisar.

#### 3. Editores e Plugins
Depois de realizada toda a instalação e configuração do Python, Pip e Robot framework, você precisará de um editor ou plugin para a escrita do código. 
Os editores mais conhecidos que têm plugins para o Robot Framework:

-   PyCharm
-   Eclipse
-   Atom
-   Visual Studio Code
-   Sublime

Para saber saber mais sobre os plugins que não estão nessa lista confira a sessão **Editors** do site oficial do [Robot Framework](https://robotframework.org/#tools) 🇺🇦

## Cenários de Testes (Código)
Abaixo encontra-se os test cases referente aos casos citados no planejamento. As keywords e os page objects estão localizados em um arquivo separadamente.

#### 1 - Login com sucesso
```
*** Test Cases *** 
Realizar login com sucesso
    Quando preenche o Email
    E preenche a Senha
    E clica em Entrar
    Então aprenseta a mensagem Bem vindo, "Usuário"!
 ```

#### 2 - Usuário tentar realizar login sem está cadastrado
```
*** Test Cases ***
Realizar login com credenciais invalidas
    Quando preenche o Email invalido
    E preenche a Senha invalida
    E clica em Entrar
    Então aprenseta a mensagem de erro Problemas com o login o usuário
 ```

#### 3 - Criar um novo usuário com sucesso
```
*** Test Cases ***
Realizar cadastro de um novo usuário
    Quando preenche o Nome
    E preenche o Email
    keywords.E preenche a Senha
    E clica em Cadastrar
    Então apresenta a mensagem Usuário inserido com sucesso
 ```

#### 4 - Tentar criar um usuário já cadastrado
``` 
*** Test Cases ***
Realizar cadastro com email já existente
    Quando preenche o Nome
    E preenche com um email já cadastrado
    keywords.E preenche a Senha
    E clica em Cadastrar
    Então apresenta a mensagem Endereço de email já utilizado
 ```

#### 5 - Adicionar conta
```
*** Test Cases ***
Adicionar multiplas contas
    Dado que acesse a pagina de Adicionar Contas
    Quando preencho o nome da conta
    E clico em salvar
    E adicione mais 4 contas
    Então apresenta a mensagem Conta adicionada com sucesso!
 ```

#### 6 - Adicionar conta sem sucesso
```
*** Test Cases ***
Adicionar conta com nome já exsitente
    Dado que acesse a pagina de Adicionar Contas
    Quando preencho o nome da conta
    E clico em salvar
    Então apresenta a mensagem Já existe uma conta com esse nome!
 ```
 
#### 7 - Excluir conta
```
*** Test Cases ***
Excluir contas criadas
    Dado que acesse a pagina de Listar Contas
    Quando clico no botão remover de cada conta
    Então apresenta mensagem Conta removida com sucesso!
 ```

#### 8 - Criar Movimentação de Receita
```
*** Test Cases ***
Criar movimentações de receita para cada conta
    Dado que acesso a pagina de Criar Movimentação
    Quando crio uma negociação de receita paga para cada conta
    Então apresenta a mensagem Movimentação adicionada com sucesso!
 ```

#### 9 - Criar Movimentação de Despesa
 ```
 *** Test Cases ***
 Criar movimentações de despesa para cada conta
    Dado que acesso a pagina de Criar Movimentação
    Quando crio uma negociação de despesa paga para cada conta
    Então apresenta a mensagem Movimentação adicionada com sucesso!
 ```

#### 10 - Excluir movimentação
```
*** Test Cases ***
Excluir Movimentações realizadas
    Dado que acesse a pagina de Resumo Mensal
    Quando clico no botão remover movimentação
    Então apresenta mensagem Movimentação removida com sucesso!
 ``` 
 
#### 11 - Reset com sucesso
```
*** Test Cases ***
Realizar reset dos dados cadastrados
    Dado que acesse a pagina Home
    Quando clicar no botão Reset 
    Então apresenta mensagem Dados resetados com sucesso!
    E limpa todos os dados das contas
 ```

## Contribuintes
Este projeto foi realizado através graças a contribuição das seguintes pessoas: 

![Linkedin Ana Clara](https://media-exp1.licdn.com/dms/image/C5103AQEp1zSam0NJOw/profile-displayphoto-shrink_200_200/0/1517008701546?e=1674691200&v=beta&t=HdKj636g7y-U_0GAI2Xc2kOGl1TCOq5_VC0Mr4pqytc)
[![Linkedin Badge Ana](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/anaclaraor/)](https://www.linkedin.com/in/anaclaraor/)

![Linkedin Anderson](https://media-exp1.licdn.com/dms/image/C4E03AQEKqiI_gf5GWQ/profile-displayphoto-shrink_200_200/0/1639246689251?e=1674691200&v=beta&t=ScWRThIhrlJMklZFbW1ZnCw2dxIkDOJtxYQooc3MVGo)
[![Linkedin Badge Ana](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/andersonncostta/)](https://www.linkedin.com/in/andersonncostta/)

![Linkedin Elídio](https://media-exp1.licdn.com/dms/image/C5103AQGteC0KO_GhZQ/profile-displayphoto-shrink_200_200/0/1542375216422?e=1674691200&v=beta&t=jHDnfra0bxrXhQnKeHM5N8KvYyIrl1AIeJgoT33FE90)
[![Linkedin Badge Ana](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/el%C3%ADdio-j%C3%BAnior-0405a8107/)](https://www.linkedin.com/in/el%C3%ADdio-j%C3%BAnior-0405a8107/)

![Linkedin Jefferson](https://media-exp1.licdn.com/dms/image/C4D03AQG4EandgNVq7Q/profile-displayphoto-shrink_200_200/0/1647708575910?e=1674691200&v=beta&t=111r5uqXcIXwgHNBBci78-tsT9pFeRVQozDDYXwnwyQ)
[![Linkedin Badge Ana](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/jefferson-barbosa-640855209/)](https://www.linkedin.com/in/jefferson-barbosa-640855209/)