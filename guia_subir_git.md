# 1) inicializa (si aún no lo hiciste)
git init

# 2) identidad
git config user.name "YACHAKAWASI"
git config user.email "louis9ramos@gmail.com"

# 3) añade solo tu archivo
git add instalacion_docker.md

# 4) crea el commit
git commit -m "Subo guia instalacion_docker.md"

# 5) conecta con tu repo en GitHub
git branch -M master
git remote add origin https://github.com/YACHAKAWASI/dev-commands.git 2>/dev/null || \
git remote set-url origin https://github.com/YACHAKAWASI/dev-commands.git

# (opcional) guarda credenciales para no escribir el token cada vez
git config --global credential.helper store


6) empujar 
git push -u origin master

7)  subir actualziacion

git add .
git commit -m "Agrego guia de comandos Git"
git push
