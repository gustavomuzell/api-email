# Microservice de envio de email

##  Lógica
-  Projeto de uma API com 2 microservices que fazem o recebimento de um cadastro e envio de email.
- Através do microservice user ele recebe o novo usuário e com um endpoint ele salva o usuário na base de dados.
- Após isso ele irá criar uma mensagem.
- Irá enviar a mensagem para um Broker(RabbitMQ)
- O microservice Email também está conectado a esse Broker.
- Quando a mensagem chegar no Broker ele irá fazer o respectivo roteamento para o microservice email consumir.
- Receber o email e enviar para o usuário cadastrado com uma mensagem de boas vindas por ter se cadastradado na plataforma.
- irá salvar na base de dados do microserviço de email o cadastro.

##  Tecnologias
- JDK 17
- Maven
- Postman
- PostGreSql
- Rabbit MQ
- STPM Gmail
- Cloud AMQP

##  Para Utililizar a API
- Alterar o email no properties do applilcation.properties do email, com um email válido.
- Alterar o password com uma chave de app.
- Startar os dois microservices.
- Fazer uma requisição do tipo post no postman utilizando o caminho http://localhost:8081/users
- Passar um email válido para receber.
