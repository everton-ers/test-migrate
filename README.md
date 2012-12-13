test-migrate
============



######################################
Migrar um repo SVN para o Github
######################################

Destino:
git@github.com:everton-ers/test-migrate.git

Origem:
git svn clone https://cesmactex.svn.codeplex.com/svn

tentativa para trazer projeto svn com svn2git (nao funcionou)
$ ruby /var/lib/gems/1.8/gems/svn2git-2.2.2/bin/svn2git https://cesmactex.svn.codeplex.com/svn


1. criar diretorio para o projeto svn
git init

1.1 . checar se o git-svn vem instalado com a instalacao padrao do git-core
caso contrario:
$ sudo apt-get install git-core git-svn ruby rubygems
$ sudo gem install svn2git

2. trazer projeto svn (funcionou)
git svn clone http://latex-uhm-thesis.googlecode.com/svn/trunk/ latex-uhm-thesis-read-only

3. git push git@github.com:everton-ers/test-migrate.git master

Referencias

https://help.github.com/articles/importing-from-subversion

https://github.com/nirvdrum/svn2git

http://setanta.wordpress.com/2008/04/13/git-svn-rapidinho/

http://www.kernel.org/pub/software/scm/git/docs/git-svn.html
