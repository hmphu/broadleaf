# broadleaf
broadleafCommerce docker


Aplicação Broadleaf Commerce aplicada em docker.

Introdução:

Procedimento para subir a aplicação:

1 -  É necessário para subir a aplicação, a instalação do docker e o docker compose, de acordo com a documentação oficial.
https://docs.docker.com/engine/install/ubuntu/
https://docs.docker.com/compose/install/
 
2 - Realizar o clone do repositório do Github.
No shell do sistema operacional, digitar o comando git clone https://github.com/prointegradorsecv/broadleaf.git



3 - Após o clone do repositório, será criado uma pasta chamada “broadleaf”, contendo o código necessário para subir a aplicação. É necessário entrar no diretório e verificar  a existência dos subdiretórios: deploy, docker, jdbc.
Comando:
cd broadleaf	//Entrar no diretório da aplicação
ls -la
deploy	// “deploy”  será utilizado para o volume do arquivo em        
  produção devopsnapratica.war.

docker // “docker” será utilizado para o volume do banco de dados Mysql.

docker-compose.yaml //Arquivo de configuração.

jdbc  // “jdbc” será utilizado como volume, contendo o arquivo          
 de configuração database “context.xml”.

4 - Realizar a criação da variável de ambiente .env, contendo as informações dos volumes nos containers docker.
Comandos:

vi mkdir
CATALINA_DEPLOY=/opt/backup/deploy
JDBC_DEPLOY=/opt/backup/jdbc
