
# Cheat Sheet - Git + Github | Dicas e Comandos para Git + Github

-Abaixo vou explicar os comandos mais populares para usar o Git.

-Below i ll explain the most popular commands to use Git.

-(As palavras entre "aspas" são apenas strings do nome de repositorios, arquivos ou diretórios que você desejar criar em seu projeto).

-(The words in "quotes" are just strings of the name of repositories, files or directories that you want to create in your project).

# BRANCH


Cria como nome "new-branch";

Create as name "new-branch";
> ~>: git branch new-branch


Criar e mudar o código para o branch "new-branch";

Create and change the code for the "new-branch" branch;
> ~>: git checkout -b new-branch


Muda o código atual e a referência para a branch "new-branch";

Change the current code and reference to the "new-branch" branch;
> ~>: git checkout new-branch


Muda o código para a branch principal: "main" | "master";

Change code to main branch: "main" | "master";
> ~>: git checkout main | ~>: git checkout master


Delete a "new-branch";

Delete the "new-branch";
> ~>: git branch -d new-branch


Lista os branchs criados;

Lists the branches created;
> ~>: git branch


Listar os branches criados com os logs de commit;

List the branches created with the commit logs;
> ~>: git branch -v


Criando um branch remoto com o mesmo nome (Upload da branch desejada);

Creating a remote branch with the same name (Upload the desired branch);
> ~>: git push origin new-branch


Criando um branch remoto com nome diferente;

Creating a remote branch with a different name;
> ~>: git push origin new-branch:new-branch


Download de todos os arquivos do repositório (main | master) remoto para o localhost;

Download all files from remote repository (main | master) to localhost;
> ~>: git pull origin main | git pull origin master


Download de todas as branchs remotas;

Download all remote branches;
> ~>: git fetch origin


Baixar um branch remoto para edição ("new-branch");

Download a remote branch for editing ("new-branch");
> ~>: git checkout -b new branch origin/new-branch


Realiza o merge entre os branchs, ou seja, junta o ramo na arvore principal;

It performs the merge between the branches, that is, it joins the branch in the main tree;
> ~>: git merge new-branch

# STASH


Cria um stash, salva temporariamente as modigicações;

Create a stash, temporarily save changes;
> ~>: git stash


Lista os stashes criados;

Lists created stashes;
> ~>: git stash list


Volta ao último stash;

Returns to the last stash;
> ~>: git stash apply


Volta ao stash com índice "2";

Returns to stash with index "2";
> ~>: git stash apply stash@{2}


Cria um branch "my_branch" a partir de um stash;

Create a "my_branch" branch from a stash;
> ~>: git stash branch my_branch

# FILES - ADD


Adiciona todos os arquivos modificados do diretório "new-branch";
Exemplo: ~>: usr/projects/new-branch

Adds all modified files from the "new-branch" directory;
Example: ~>: usr/projects/new-branch
> ~>: git add .


Adiciona somente o arquivo "my_readme.txt";

Add only the file "my_readme.txt";
> ~>: git add my_readme.txt


Adiciona somente o diretorio "my_bkp";

Add only the directory "my_bkp";
> ~>: git add my_bkp


Adiciona um arquivo que está no .gitignore;

Adds a file that is in .gitignore;
> ~>: git add -f my_program_gitignore.py

# FILES - REMOVE


Remover arquivo "my_file.txt";

Remove file "my_file.txt";
> ~>: git rm my_file.txt


Remover diretório ("assets");

Remove directory ("assets");
> ~>: git rm -r assets

# COMMIT


Comitar um arquivo ("my_file.txt");

Commit a file ("my_file.txt");
> ~>: git commit my_file.txt


Comitar vários arquivos ("my_file.txt" & "my_file2.txt");

Commit multiple files ("my_file.txt" & "my_file2.txt");
> ~>: git commit my_file.txt my_file2.txt


Comitar informando mensagem;

Commit informing message;
> ~>: git commit my_file.txt -m "test 1 2 3"

# MODIFICATIONS


Mostra as modificações totais do projeto;

Shows the total changes to the project;
> ~>: gitk

Modificações feitas antes de enviar as modificações para o repositório remoto,

(usado para verificar e avaliar se esta tudo certo antes de subir seu novo commit);
Modifications made before committing the modifications to the remote repository,

(used to check and evaluate if everything is ok before uploading your new commit);
> ~>: git diff


Estado dos arquivos/diretórios;

Status of files/directories;
> ~>: git status


Alterando mensagem de commit já realizado;

Changing commit message already performed;
> ~>: git commit --amend -m "new message"


Alterar últimos commits, modificando as mensagens;

Change latest commits, modifying messages;
> ~~>: git rebase -i HEAD~3

# LOG


Exibe histórico dos ultimos commits;

Displays history of the last commits;
> ~>: git log


Exibe histórico com diff dos ultimos 3 commits;

Displays history with diff of the last 3 commits;
> ~>: git log -p -3


Exibir histórico no diretório ("usr/projects/new-branch");

Display history in directory ("usr/projects/new-branch");
> ~>: git log -- usr/projects/new-branch


Exibe histórico de commits com informações resumidas em uma linha(existem outros tipos);

Displays commit history with summarized information in one line (there are other types);
> ~>: git log --pretty=oneline


Exibe histórico de modificações de um arquivo("usr/projects/new-branch/my_file.txt");

Display a file's modification history("usr/projects/new-branch/my_file.txt");
> ~>: log --diff-filter=M -- usr/projects/new-branch/my_file.txt


Exibir histórico de um determinado autor ("user");

View history of a particular author ("user");
> ~>: git log --author=user

# CHERRY-PIC


Copia as informações desse commit;

Copy the information from that commit;
> ~>: git cherry-pick <commit-id>


Copia todos os commits entre o commit A e o commit B, inclusive A e B;

Copies all commits between commit A and commit B, including A and B;
> ~>: git cherry-pick A^..B

Copia todos os commits entre o commit A e o commit B, excluindo A.
Copies all commits between commit A and commit B, excluding A.
> ~>: git cherry-pick A..B

# GIT+GITHUB/BITBUCKET - COMMANDS


Verificar a versão instalada;

Check the installed version;
> ~>: git --version


Configura seu nome;

Set your name;
> ~>: git config --global user.name "yourname"


Configura seu e-mail;

Configure your email;
> ~>: git config --global user.email "your@email.com"


Envie o arquivo ao repositório remoto;

Upload the file to the remote repository;
> ~>: git remote add origin git@github.com:"User_github"/"repository"


Verifica os arquivos enviados;

Checks the uploaded files;
> ~>: git remote -v


Sincroniza o repositório local com o remoto;

Synchronizes the local repository with the remote one;
> ~>: git remote add origin https://github.com/name/repository.git


Inicia um repositório local na pasta atual;

Starts a local repository in the current folder;
> ~>: git init


Cria uma cópia do repositório local;

Creates a copy of the local repository;
> ~>: git clone ssh://git@github.com/[username]/[repository-name].git
