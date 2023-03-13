# git-general-knowledge
Comandos más comunes de Git

###### Book GIT
https://progit2.s3.amazonaws.com/en/2015-09-27-d6ba8/progit-en.844.pdf
http://www.mobilefish.com/developer/git/git.html

###### Commands
###### Your Identity
`git config --global user.name "John Doe"`
`git config --global user.email johndoe@example.com`

###### Checking Your Settings
`git config --list`
`git config user.name`

###### Set interface of colors
`git config --global user.ui true`

###### Cloning an Existing Repository
`git clone <URL>`

###### Committing Your Changes
`git commit -m "comments"`

###### Remove file from your staging area /before commit
`git rm --cached README`
`###### git rm with pattern - You can pass files, directories, and file-glob patterns `
`git rm log/\*.log`

###### Moving Files
`git mv file_from dir/file_to`

###### Viewing the Commit History
`git log --decorate --oneline`
`git log --pretty=format:"%h - %an, %ae, %ar : %s"`
`git log --pretty=format:"%h - %an, %ar : %s"`
`git log --pretty=oneline`

###### Limiting Log Output
`git log -p -2`
`git log --since=2.weeks [--since, --after, --until, --before ]`
`git log --since="2008-01-15"`
`git log --author Ricardo`

###### Short Status
`git status -s`

###### This command takes your staging area and uses it for the commit and fusion with back commit
 `git commit -m 'initial commit'`
`$ git add forgotten_file`
#Sobreescribir commit
`$ git commit --amend -m ""`

###### Unstaging a Staged File
`git reset HEAD <file>`

###### Unmodifying a Modified File
`git checkout -- <file>`


###### Showing Your Remotes
`git remote -v`

###### Adding Remote Repositories
`git remote add <remote-name]> <url>`

###### For example, if you want to fetch all the information that Paul has but that you don’t yet have in your repository,
`git fetch <remote-name]> `

###### Pushing to Your Remotes
`git push origin master`
`git push origin name_of_your_new_branch`

###### Get all remote brach
`git ls-remote`
`git remote show`

#Inspecting a Remote
`git remote show [remote-name]`

###### Removing and Renaming Remotes
`git remote rename pb paul`
`git remote rm paul`

###### Listing Your Tags
`git tag`
`git tag -l "v1.8.5*"`

###### Creating Tags
`git tag -a v1.4 -m 'my version 1.4'`
`git show v1.4`

###### View all branch
`git branch -v`
###### Delete brach
`git branch -d <nombre_branch>`
###### view all branches, locals and remotes
`git branch --all`
###### show remotes branch
`git branch -r`
###### delete local branch
`git branch -d branch_name`
###### rename local branch
`git branch -m old_branch_name new_branch_name`

###### Stash
`git stash: es otro de los limbos, como el staging area. Para agregar los cambios estos deben estar en el staging `area.
`git stash list: nos muestra la lista de stash que tengamos.`
`git stash drop stash@{numero}: nos permite borrar un stash.`
`git stash apply: aplicamos el último cambio`

###### Add proxy http and https
`git config --global http.proxy http://proxyuser:proxypwd@proxy.server.com:8080`
`git config --global http.proxy http://BANCOAZTECA/\B270062:Grupo852Salinas3@10.50.8.20:8080`
`git config --global --unset http.proxy`


###### git tag: nos permite agregar etiquetas a nuestros cambios

git tag 
-a para la anotación
-m para el mensaje
-l nos muestra la lista de etiquetas
-f para renombrar
-d para borrar

###### git log: configurando el logger

git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"

###### git reset

git reset --soft [SHA 1]: 
Elimina los cambios hasta el staging area
git reset --mixed [SHA 1]: 
Elimina los cambios hasta el working area
git reset --hard [SHA 1]: 
Regresa hasta el commit del [SHA 1], si hay forma de recuperar si tenemos el SHA-1(commit)

###### Git stash

git stash: es otro de los limbos, como el staging area. Para agregar los cambios estos deben estar en el staging area.
git stash list: nos muestra la lista de stash que tengamos.
git stash drop stash@{numero}: nos permite borrar un stash.
git stash apply: aplicamos el último cambio

git remote add origin "http..."
git remote remove origin
git remote -v

$ git fetch origin master

git pull origin master

###### es igual a los dos pasos anteriores git fecth y git merge

git push origin master
git push origin master --tags
git push origin [otra_rama]

