# Backups manuales. Viviendo peligrosamente.

unfichero.txt

unfichero2.txt

unfichero2_final.txt

unfichero2_final_final.txt

unfichero2_final_esta_si_que_si.txt

# Máquina del tiempo

<Cosas muy importantes que no queremos perder>

git status

git commit


git add unfichero.txt 

git commit -m"Version inicial"

git log

Más cosas importantes que tampoco queremos perder.

git status

git add unfichero.txt 

git status

git commit -m"Version entregada para su revision"


git log

git show b9a7:unfichero.txt 

git diff b9a7..HEAD


# Edición colaborativa

https://codepen.io/duongphuhiep/post/git-merge-conflicts

$ mkdir repo

$ cd repo

$ git init --bare --shared pf5.git

$ cd ..

$ mkdir joseba

$ mkdir josu

$ git clone repo/pf5.git/ joseba

$ git clone repo/pf5.git/ josu

$ code joseba

$ code josu

# Joseba 

$ vi test/test_main.py

$ vi src/main.py

$ git commit -- No hay nada agregado

-- VSCode con terminal y vista Git (para ver el efecto de los comandos )---

$ git status

$ git add test

$ git status

$ git commit -m"Empty test for git practice"

$ git log

# Josu

$ git log -- nada que mostrar en este universo paralelo. Comprobar también vista Explorer.

# Joseba

$ git push

$ git log            -- ver que ahora dice origin/main al lado del commit

# Josu

$ git pull           -- No hay cambios en la vista git -> cambiar a Explorer para ver los fichero


-- cambios en el mismo fichero test/test_main.py y commit de ambos

# Joseba

$ git status

$ git add test/test_main.py

$ git commit -m"Joseba's change practicing concurrent changes"

$ git log            -- Ver a qué commit apunta HEAD y a cual origin/master


# Josu

$ git status

$ git add test/test_main.py

$ git commit -m"Josu's change practicing concurrent changes"

$ git log            -- Ver a qué commit apunta HEAD y a cual origin/master


# Joseba

$ git push

$ git log

# Joseba

$ git pull                    -- Se queja de de que no puede hacerlo porque hay conflictos

$ git pull --rebase           -- Nos indica como marcar como resueltos los conflinctos 'git add/rm' y los diferentes 'git rebase --continue|skip|abort'

$ git status                  -- Probar las diferentes opciones 'Accept' de VSCode (ctr+z en cada una)

$ git add test/test_main.py   -- una vez arreglado

$ git rebase --continue -m"Joseba's and Josu's changes reconciled"







