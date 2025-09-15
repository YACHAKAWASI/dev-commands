# Guía para subir archivos a GitHub

## 1) Inicializa (si aún no lo hiciste)
```bash
git init
```

## 2) Configura tu identidad
```bash
git config user.name "YACHAKAWASI"
git config user.email "louis9ramos@gmail.com"
```

## 3) Añade solo tu archivo
```bash
git add instalacion_docker.md
```
para  todo los archivo en el proyecto
```bash
git add .
```
## 4) Crea el commit
```bash
git commit -m "Subo guia instalacion_docker.md"
```

## 5) Conecta con tu repo en GitHub
```bash
git branch -M master
git remote add origin https://github.com/YACHAKAWASI/dev-commands.git 2>/dev/null || \
git remote set-url origin https://github.com/YACHAKAWASI/dev-commands.git
```

## (Opcional) Guarda credenciales para no escribir el token cada vez
```bash
git config --global credential.helper store
```

## 6) Empujar cambios iniciales
```bash
git push -u origin master
```

## 7) Subir actualizaciones
```bash
git add .
git commit -m "Agrego guia de comandos Git"
git push
```
