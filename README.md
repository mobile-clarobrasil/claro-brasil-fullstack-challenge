# claro-brasil-fullstack-challenge

O objetivo deste desafio é avaliar as competências técnicas para uma vaga fullstack, pontos que serão avaliados:

* Organização;
* Estilo e boas praticas de código;
* Designer e criação das APIs REST;
* Conhecimento nas libs e frameworks utilizados;
* API executando em alguma plataforma de cloud (Heroku é grátis) para apresentação;
* Demonstração do aplicativo;


## Instruções

* O código deve ficar disponivel em um repositório público no github;
* Inclua um arquivo chamado COMMENTS.md com:
  * Explicação rápida da decisão da arquitetura utilizada e o porquê
  * O que você melhoraria se tivesse mais tempo
* Informe ao recrutador quando concluir o desafio junto com o link do repositório;

## Requisitos

### Contextualização

A empresa possui uma solução de vídeo que os usuários utilizam através de um aplicativo nas plataformas Android e iOS. Os usuários têm à disposição um catálogo de filmes e séries que eles podem assistir em seus tablets/smartphones. Para assistir ao conteúdo do catálogo, o usuário precisa primeiro cadastrar o seu dispositivo no backend.

O desafio consiste em criar um **aplicativo movel** e **APIs** que permitam visualizar, cadastrar, alterar ou remover os dispositivos dos usuários. Não é necessário implementar o cadastro dos usuários, eles podem ser representados por ids.

Mas existem algumas restrições para o controle de devices:

* Um usuário poderá ter, no máximo, três dispositivos cadastrados.
* O usuário poderá fazer a troca de um dispositivo cadastrado no período de 30 dias, ou seja, o usuário deverá remover um dispositivo e cadastrar um novo. Após efetuar a troca de dispositivo, uma nova troca para o novo dispositivo só será possível 30 dias depois.
* As APIs de controle de devices deverão respeitar estas restrições e retornar os erros correspondentes, informando para o client o motivo do erro.
  * O client deve tratar os errors e exibir uma mensagem que explique ao cliente o que está acontecendo.
  * Exemplo de mensagens:
    * ooops! Sua conta atingiu o limite máximo de dispositivos cadastrados.
    * Deseja remover o dispositivo?  

Exemplos de uso:

* O usuário 123 cadastra seu primeiro device e visualiza uma mensagem de sucesso. 
* O usuário 456 já possui três devices cadastrados, tem direito a uma troca, e tenta cadastrar o quarto device. Mas visualiza uma mensagem de error.
* O usuário 789 possui dois devices cadastrados, já efetuou uma troca nos últimos 30 dias, tenta remover um device e visualiza uma mensagem de sucesso.
* O usuário 789 agora possui apenas um device cadastrado, já efetuou uma troca nos últimos 30 dias, tenta realizar uma nova troca. Mas visualiza uma mensagem de error.

### Requisitos funcionais:

* Adicionar um dispositivo, informando:
  * ID do usuário
  * ID do dispositivo
  * Nome do dispositivo
  * Modelo do dispositivo (Android, iOS)
* Alterar o nome de um dispositivo através do ID
* Remover um dispositivo através do ID
* Trocar dispositivo.

### Requisitos desejáveis:

* Testes unitários;
* Uso de animações para apresentação do conteúdo;
* Implementar autenticação;
