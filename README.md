Hosting del sitio: Netlify (https://www.netlify.com/)
pgaleotti@southcom.co / C3-68$GK*5@h8U]3

Token bitbucket app: token bitbucket app

Código: Bitbucket (https://bitbucket.org/southcom/workspace/overview/)
user southcom o mail pgaleotti@southcom.co
clave: B1t8uck3t


PC: C:\Users\pgaleotti\OneDrive - Pyxis Portal\Southcom\site 2026



Si se hacen cambios en el bitbucket, hay que hacer sync con el PC para la edición del contenido.

Ejemplo:
git status (verifica si están sync los repositorios del PC y de bitbucket)
git pull --rebase origin main (sincroniza)
git log --oneline --decorate -5 (visualiza los commits)


Flujo de trabajo:
Edición con Visual Studio Code
Agregar cambio al commit
git add .
git commit -m "Agrego nueva sección de servicios"
Push
git push

----- NUEVA VERSION ----

$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

# asegurarse de estar actualizado en main
$ git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.
$ git pull origin main
From https://bitbucket.org/southcom/southcom-site
 * branch            main       -> FETCH_HEAD
Already up to date.

# crea rama v2 y se posiciona en ella
$ git checkout -b v2
Switched to a new branch 'v2'

# upload v2 a bitbucket
$ git push -u origin v2
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create pull request for v2:
remote:   https://bitbucket.org/southcom/southcom-site/pull-requests/new?source=v2&t=1
remote:
To https://bitbucket.org/southcom/southcom-site.git
 * [new branch]      v2 -> v2
branch 'v2' set up to track 'origin/v2'.

#primer commit

$ git commit --allow-empty -m "Initialize v2 branch"
[v2 b6a2649] Initialize v2 branch
$ git push
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 197 bytes | 197.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create pull request for v2:
remote:   https://bitbucket.org/southcom/southcom-site/pull-requests/new?source=v2&t=1
remote:
To https://bitbucket.org/southcom/southcom-site.git
   4982f22..b6a2649  v2 -> v2


# crear

para cuando se finaliza, tenes todo en el branch v2, (a mi me fallo el checkou+merge) asi que al final hice:

git push origin v2:main (hace el push de v2 a main directo en el repo y ahi publico ok.
