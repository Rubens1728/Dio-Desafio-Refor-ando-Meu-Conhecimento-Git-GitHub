# ***Meu passo-a-passo***: :footprints:


## *** 1. Criptografando com Sha1***.

#### *1.1 Crio um arquivo*
#### *1.2 No mesmo diretório em que foi criado o arquivo, clico com o botão direito do mouse e clico com o botão esquerdo do mouse no Git Bash para iniciá-lo direto no diretório, obs. (estou usando o windows 11, para iniciar o Git Bash conforme descrito acima, ao clicar com o botão direito do mouse, tive que ir na opção* ***mostrar mais opções***)

#### *1.3 No Git Bash digito o seguinte comando:*
*openssl sha1 nome do arquivo e dou enter, será gerado um código alfanumérico. Pronto está feito*.

## ***2. Gerando chave SSH***.

#### *2.1 Para gerar a chave **SSH**, no terminal Git Bash digito o seguinte comando*:
*ssh-keygen -t ed25519 -C obs:(o **c** é maiúscula) depois do c,  coloco o e-mail usado para criar a minha conta no GitHub e dou enter, será apresentada uma mensagem informando onde  a chave será salva. 
Depois de confirmar o local onde a chave será slva ao dar enter, será pedido para criar uma senha, depois de criar e confirmar a senha a chave estará criada*. 

## ***3. Adicionando usuário para autenticação no servidor remoto***.

#### *3.1 Para fazer isso uso o seguinte comando no Git Bash*:
*git config --global user.name "Nome do usuário" entre as aspas mesmo e dou enter, depois uso o mesmo comando, mas ao invés de .name, vou colocar o e-mail.
git config --global user.email então coloco o e-mail e depois dou enter, após esses processos não aparece nenhuma mensagem de confirmação de inclusão com exito, o que de certa forma a confirma.
caso eu queira me certificar se de fato deu certo, uso o comando git config --list e busco por usuário(user)*.

***Obs: tanto o nome de usuário, quanto o e-mail, é ideal que sejam os mesmos cadastrados no GitHub***.

## ***4. Iniciando o Git***.

#### ***4.1 Para esse fim, uso o comando***:
*Git Init*

## ***5. Adicionando o Agent***.

#### ***5.1 para adicionar o agent, uso o comando***:
*eval $(ssh-agent -s) e dou enter*

## ***6. Extraindo o conteúdo da chave***.

#### ***6.1 Acesso o diretório onde estão as chaves ssh, abro o git bash no mesmo diretório, e digito o comando:***
*cat e a chave pública e dou enter*

***Obs: a chave pública tem o seu final com as iniciais pub***

## ***7 Criando um commit***.

#### ***7.1 Acesso o diretório onde está o arquivo, abro o git bash no mesmo diretório, torno o arquivo conhecido no git com o comando***:
*git add Asterisco ou git add . e dou enter*.

#### ***7.2 Para me certificar se o arquivo foi adicionando ao staged, uso o comando***:
*git status e dou enter*

***Estando tudo certo será mostrada a mensagem new file: e o nome do arquivo e sua extensão na cor verde, em seguida dou o comando***:

*git commit -m "" e dou enter*

***entre as aspas escrevo algo para identificar o commit***.

## ***8.Criando um Repositório no GitHub***.

### ***8.1 Após fazer o meu cadastro no GitHub, vou até o canto superior direito onde acessamos o perfil, ao lado tem o sinal de + com uma setinha para baixo, clico na setinha e escolho a opção (novo repositório), dou um nome para o repositório e coloco uma descrição e seleciono a opção (Adicionar um arquivo README) e depois clico em clicar rpositóro***.

## ***9. Enviando os arquivos para o Servidor Remoto (GitHub)***.

### ***9.1 Com o repositório já criado, no canto superior direito onde acessamos o perfil clico na setinha para baixo e seleciono (seus repositórios) e acesso o repósitório que criei, vou em código, seleciono HTTPS e copio o link, volto ao git e digito o seguinte comando***:
*git remote add origin e o link do repositório, em seguida dou enter*.

### ***9.2 Depois de adicionar o link do repositório, eu dou o seguinte comando***:

*git push oring master*.

## ***10 Clonando o Repositório*** do servidor remoto.

### ***10.1 Acesso o GitHub, no canto superior direito onde acessamos o perfil clico na setinha para baixo e seleciono (seus repositórios) e acesso o repósitório que criei, vou em código, seleciono SSH, copio o link e volto ao git bash e dou o comando***:

*Git clone e colo o link, em seguida dou enter.

***depois de atualizar as informações volto a fazer o upload novamente***.