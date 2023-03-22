# Docker-Development
   Ambiente em desenvolvimento docker implementado para facilitar desenvolvimento de software nas mais diversas linguagens. 
   
## Conteúdo do Projeto:  
   A versão atual do projeto comtempla os serviços Mysql, PHPMyAdmim, Redis, Ofelia Schedule e um projeto de Fluxo de Caixa desenvolvido em Laravel/PHP que poderá ser clonado do GitHub e manipulado por comando bash através de um terminal.
   
 ## Como utilizar:
 ### 1 - Faça um clone do projeto através do repositório abaixo:
     git clone https://github.com/fabiomattheus/docker-development.git
 
 ### 2 - Acesse o diretório do projeto:
     cd docker-development
 
 ### 3 - Execute o comando abaixo:
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
 
 ### Nota: export HOST_UID=$(id -u) servirá para que o id do usuário seja encontrado no momento da construção do conteiner do projeto Fluxo de Caixa    
    
 ### 6 - Execute o comando  call e se tudo estiver certo, deverá ser mostrado um menu confome imagem abaixo:   
![alt text](https://github.com/fabiomattheus/docker-development/blob/main/menu-docker-development.png)
