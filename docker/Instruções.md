# Instruções para rodar infraestrutura Docker

1. Organizando as pastas do seu projeto

Copie todos os arquivos e pastas que há nesta pasta /docker para a raiz do seu projeto. Em seguida, cria uma pasta chamada "services" na raiz do projeto.

2.  Clonar o repositório do Laravel

Clone o [repositório do Laravel](https://github.com/laravel/laravel) dentro da pasta /services que você acabou de criar. Em seguida, renomeie a pasta clonada para "app".

A estrutura do projeto deve ficar da seguinte forma:

```
/
+ docker-compose.yml
+ mysql/
+ services/
++ app/
```

3. Copie o conteúdo do arquivo .env.example para um arquivo .env na raiz do projeto

```
	cp .env.example .env
```

4.  Instale as dependências do composer.json

Inicialize seus containers na raiz do diretório /docker:

```
	docker-compose up -d
```

Você não precisa ter o Composer instalado na sua máquina para este passo, utilizaremos um container efêmero Docker. Bastando rodar o seguinte comando no terminal, na raiz da pasta app:

```
	docker-compose exec app composer install
```

Este comando instala todos os pacotes usando o Composer no container Docker e consequentemente na sua pasta local (por conta do [volume bind](https://docs.docker.com/storage/volumes)).

5. Configurações no Laravel

*   Gere uma chave para sua aplicação, com o comando:
```
	docker-compose exec app php artisan key:generate
```

Reinicie o container app, para que essa alteração na variável .env tenha efeito: 
```
	docker-compose stop app
	docker-compose up -d app
```

Pronto! Agora para rodar comandos no seu container Laravel, basta seguir o seguinte padrão (estando no diretório onde se encontra o arquivo docker-compose.yml):

```
	docker-compose exec app comando
```

5. phpMyAdmin

Você pode gerenciar seu banco de dados local graficamente com o phpMyAdmin. Nesta infraestrutura, é inicializado um container phpMyAdmin para vocÊ. Para acessá-lo, visite http://localhost:3030 na sua máquina. 

As credenciais de acesso ao banco de dados se encontram nas variáveis "MYSQL_USER" e "MYSQL_PASSWORD" do serviço de banco de dados no docker-compose.yml.
