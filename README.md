# Projeto "AMOR ÀS CEGAS"

Realizado por mim e [João Meneses](https://github.com/JGMeneses).

<h2> Em geral </h2>

- O Projeto *"Amor Às Cegas"* foi um trabalho de conclusão da disciplina de Programação Orientada a Objetos, ofertada no segundo semestre do TADS, realizado em dupla.
- O projeto em si é uma aplicação de um aplicativo de relacionamentos que busca aproximar as pessoas a partir das suas preferências e hobbies.
- Esse trabalho foi realizado em conjunto com a disciplina de Banco de Dados, onde trabalhamos com o PostgreSQL.


<h2> Detalhes do Projeto </h2>

Um dos primeiros questionamentos quando iniciamos o projeto era: ***como relacionar duas pessoas?*** Como não tinhamos contato com o precessamento digital de imagens, precisavamos de um fator comum, algo que aproximasse os usuários. Logo, chegamos aos **HOBBIES** e assim, nasceu o "Amor às Cegas", onde as pessoas se relacionam através dos seus gostos e preferências.

Para a criação do projeto, foi necessário estabalecer quais as entidade necessárias para gerar o banco de dados, como cada entidade iria se relacionar e quais seriam seus atributos. Nós já sabiamos de duas entidades: **Usuario** e **Hobbies**. Porém era requisito do projeto que tivessem quatro entidades, portanto, criamos também **PagamentoVip**, onde o usuario que tivesse o pagamento vip, teria alguns benefios dentro da aplicação; e **Usuario_Hobbies**, que é justamente a tabela gerada a partir do relacionamento N para N entre os usuários e os seus hobbies.

#### Modelagem do Banco de Dados:

- Usuario (**nickname**, _nome, login, senha, idade, genero, orientacao_sexual_)
- Hobbies (**cod_hobbie**, _descricao_)
- PagamentoVIP (**cpf**, _cod_pagamento, senha_cartao, numero_cartao, pg, **fk_usuario**_)
- Usuario_Hobbies (**id**, **_fk_usuario, fk_hobbies_**)

<sub> OBS.: O texto em **negrito** é uma chave primária e aquele em **_negrito e itálico_** é uma chave estrangeira.</sub>

A partir disso, foi possivel criar o projeto e suas classes para então detalhá-las com seus atributos e métodos. Ao ver o arquivo 'src', percebe-se a classe **_Match_**, essa classe foi criada com o próposito de facilitar a visualização do auto-relacionamento da tabela Usuario, pois um usuario se relaciona com vários outros a partir da quantidade de hobbies compatíveis.

#### Diagrama de Entidade Relacionamento: 

![DER 1](https://user-images.githubusercontent.com/128005290/226071582-53a93be3-7205-4dd2-9d55-e9fa18c452c8.png)

<h2>Status do projeto: Não finalizado</h2>

#### Motivos: 

- Ao excluir um usuário, deveria sair do "MENU USUARIO", gera um erro na aplicação.
- 
