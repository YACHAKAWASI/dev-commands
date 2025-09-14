# Guía para subir archivos a GitHub

## 1) Inicializa (si aún no lo hiciste)
```bash
git init

2) Configura tu identidad

git config user.name "YACHAKAWASI"
git config user.email "louis9ramos@gmail.com"

3) Añade solo tu archivo

git add instalacion_docker.md

4) Crea el commit

git commit -m "Subo guia instalacion_docker.md"

5) Conecta con tu repo en GitHub

git branch -M master
git remote add origin https://github.com/YACHAKAWASI/dev-commands.git 2>/dev/null || \
git remote set-url origin https://github.com/YACHAKAWASI/dev-commands.git

6) Empujar cambios iniciales

git push -u origin master

7) Subir actualizaciones

git add .
git commit -m "Agrego guia de comandos Git"
git push
