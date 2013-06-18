######################################
Migrar um repo SVN para o Github
######################################

Destino:
git@github.com:everton-ers/test-migrate.git

Origem:
http://latex-uhm-thesis.googlecode.com/svn/trunk/

tentativa para trazer projeto svn com svn2git (nao funcionou).


- Criar diretorio para o projeto SVN que sera migrado para GIT.

git init

- Checar se o git-svn vem instalado com a instalacao padrao do git-core.

caso contrario:

$ sudo apt-get install git-core git-svn 

- Trazer projeto svn (funcionou). O comando 'git svn' lê o projeto SVN e parseia-o para tornar-se um projeto GIT.

git svn clone http://latex-uhm-thesis.googlecode.com/svn/trunk/ dir_latex-uhm-thesis-read-only

- A partir deste momento o projeto que era SVN agora eh GIT, portanto voce pode 'commita-lo' para o servidor do GITHUB.
Certifique-se de criar o repositorio no github deste projeto.

git push git@github.com:everton-ers/test-migrate.git master

Referencias:

https://help.github.com/articles/importing-from-subversion

https://github.com/nirvdrum/svn2git

http://setanta.wordpress.com/2008/04/13/git-svn-rapidinho/

http://www.kernel.org/pub/software/scm/git/docs/git-svn.html
