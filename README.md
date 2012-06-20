###Instalação do projeto

Instale o RVM seguindo o tutorial do site deles
-------------
https://rvm.io//rvm/install/

Instale o Ruby 1.9.3
--------------------
`rvm install 1.9.3`

Crie o gemset para o projeto
----------------------------
`rvm use 1.9.3; rvm gemset create viagem_certa; rvm gemset use viagem_certa`

Instale o git
-------------
`sudo apt-get install git-core`

Clone o projeto
---------------
`git clone https://github.com/sucurilabs/viagem_certa.git`

Crie o .rvmrc para sempre que entrar no projeto usar o ruby e gemset corretos
-----------------------------------------------------------------------------
`cd viagem_certa; echo 'rvm use 1.9.3@viagem_certa' > .rvmrc`

Execute o bundle para instalar as dependencias do projeto
---------------------------------------------------------
`bundle`

Crie o banco e execute as migrações
-----------------------------------
`rake db:create; rake db:migrate`

Inicie o servidor
-----------------
`rails s`