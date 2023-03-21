# alura-spring-boot-3
Spring Boot 3 desenvolva uma api rest java

--> O comando para rodar o projeto é composto pelo comando java, pelo parâmetro -jar, e pelo caminho do arquivo:

java -jar target/api-0.0.1-SNAPSHOT.jar

--> Vou parar a aplicação e pressionar seta para cima para listar o último comando. Agora, antes do parâmetro -jar, vamos passar outro parâmetro: -Dspring.profiles.active=prod.

java -Dspring.profiles.active=prod -jar target/api-0.0.1-SNAPSHOT.jar

--> Dito isso, como passar as variáveis de ambiente? Da mesma forma que passamos o parâmetro do profile! Com o projeto parado, pressionamos seta para cima e digitaremos o seguinte comando:

-DDATASOURCE_URL=jdbc:mysql://localhost/vollmed_api`

--> Para simular, utilizei o "localhost", pois o banco está no meu próprio computador.

java -Dspring.profiles.active=prod -DDATASOURCE_URL=jdbc:mysql://localhost/vollmed_api -jar target/api-0.0.1-SNAPSHOT.jar

--> Passamos então a variável da URL. Faremos o mesmo processo para as variáveis USERNAME e PASSWORD. Trata-se das mesmas variáveis configuradas no arquivo application-prod.properties.

java -Dspring.profiles.active=prod -DDATASOURCE_URL=jdbc:mysql://localhost/vollmed_api -DDATASOURCE_USERNAME=root -DDATASOURCE_PASSWORD=root -jar target/api-0.0.1-SNAPSHOT.jar

--> No navegador, entraremos na documentação do Swagger:

http://localhost:8080/swagger-ui.html