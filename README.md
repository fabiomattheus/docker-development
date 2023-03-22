# Docker-Development
   Ambiente em desenvolvimento docker implementado para facilitar e dar rapidez na configuração do ambiente de desenvolvimento de software nas mais diversas linguagens. 
   
## Conteúdo do Projeto:  
   A versão atual do projeto comtempla os serviços Mysql, PHPMyAdmim, Redis, Ofelia Schedule e um projeto de Fluxo de Caixa desenvolvido em Laravel/PHP que poderá ser clonado do GitHub e manipulado por comandos bash através de um terminal.
   
 ## Como utilizar:
 ### 1 - Faça um clone do projeto através do repositório abaixo:
     git clone https://github.com/fabiomattheus/docker-development.git
 
 ### 2 - Acesse a raiz do diretório do projeto:
     cd docker-development
 
 ### 3 - Execute o comando abaixo para visualizar o caminho do projeto:
     pwd
 
 ### 4 - Copie a saída do comando pwd mostarado na tela:
 Exemplo: /home/seu_usuario/caminho_do_projeto/docker-development
 
 ### Acesse o arquivo .bashrc:
     gedit ~/.bashrc

 ### 5 - Cole na última linha do arquivo .bashrc as instruções descritas abaixo e modifique o seu usuário e o caminho do projeto confome mostrado no item 3: 
     function call { 
        cd /home/fabio/projects/docker-development && bash call $* 
        cd -
     }
     export HOST_UID=$(id -u)
 
 ### Nota: export HOST_UID=$(id -u) servirá para que o id do usuário seja encontrado no momento da construção do container do projeto Fluxo de Caixa    
    
 ### 6 - Execute o comando call e se tudo estiver certo, deverá ser mostrado um menu confome imagem abaixo:   
     call
     
![alt text](https://github.com/fabiomattheus/docker-development/blob/main/menu-docker-development.png)

### 7 - Execute o camando abaixo para clonar o projeto de Fluxo de Caixa:
    call clone

### 8 - Execute o comando abaixo para construção dos containers docker e configuração do Projeto Fluxo de Caixa Laravel DDD
    call init
 
### 9 - Execute o comando docker ps para visualizar os containers:
    docker ps 
    
### Nota: Se tudo correu bem até aqui,  os containers docker estão up e agora poderemos utilizar os comandos do laravel para manipulação do projeto Fluxo de Caixa Laravel DDD.

### 10 - Execute o comando abaixo para limpar o banco de dados:
    call artisan migrate:fresh

### 11 - Execute o comando abaixo para executar todos os testes:
    call artisan test

### Nota: Através do comando call artisan e/ou call composer você poderá complementá-lo com qualquer flag igualmente quando utilizado localmente php artisan:

### 12 - Execute o comando abaixo para certificar que os namespaces dos arquivos estão fidedignos:
    call composer dump-autoload

### Nota: Para executar o comando call não é necessário entrar dentro do container com a flag exec, pois dentro do script do arquivo call, disponível na raiz do projeto, os comandos docker são executados com a flag run --rm, ou seja, o comando levatará o container caso não esteja up, e assim que usá-lo, o removerá.  



    
    
 


    
