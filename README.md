# Projeto DesafioTegra

Implementação da lógica de carrinho de compras de uma loja de livros.

# Linguagem e Ferramentas de Desenvolvimento

Este projeto foi desenvolvido em PHP7, utilizando os editores de código-fonte VSCODE e SUBLIME.
O SGBD utilizado para a criação das tabelas e procedures foi o Mysql, utilizando a ferramenta MYSQL WORKBENCH.
Obs.: Foi utilizado o servidor web local XAMP para o desenvolvimento do projeto completo.

# Configurando o Projeto DesafioTegra

Segue abaixo as configurações necessárias para que o projeto seja executado corretamente e em sua totalidade:

  # -  Copiar código abaixo e colar dentro do arquivo httpd-vhosts.conf, localizado na pasta: C:\xampp\apache\conf\extra\httpd-vhosts.conf
        
              <VirtualHost *:80>
                  ServerAdmin webmaster@hcode.com.br
                  DocumentRoot "C:\ProjetoTegra"
                  ServerName www.tegrabooks.com
                  ErrorLog "logs/dummy-host2.example.com-error.log"
                  CustomLog "logs/dummy-host2.example.com-access.log" common
                  <Directory "C:\ProjetoTegra">
                      Require all granted

                      RewriteEngine On

                      RewriteCond %{REQUEST_FILENAME} !-d
                      RewriteCond %{REQUEST_FILENAME} !-f
                      RewriteRule ^ index.php [QSA,L]
                  </Directory>
              </VirtualHost>
              
  # - Abrir arquivo host, localiado em C:\Windows\System32\drivers\etc\hosts
      Copiar e colar endereço virtual abaixo:
          127.0.0.1	www.tegrabooks.com
          
  # - Executar script sql TegraBook.sql, localizado dentro do repositório, no caminho ProjetoTegra\Databases\TegraBook.sql
  
  Depois de configurado o arquivo, abrir o navegador e inserir o virtual host www.tegrabooks.com
 
  
  
  # TELA DE ADMINISTRADOR
    Foi desenvolvido um módulo de administrador para poder listar, inserir, alterar e excluir os produtos, usuários e catetoria de produtos.
    OBS.: Login padrão: Admin
          Senha:        1234
 
 # TELA DE VENDAS
   Na tela principal de vendas, é possível visualizar os produtos, inserir no carrinho de compras e finalizar compra, gerando um boleto.
  
