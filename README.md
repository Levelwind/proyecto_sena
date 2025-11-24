# Proyecto: proyecto sena

## Objetivo del proyecto

El objetivo de este proyecto es desarrollar aprender a utilizar git hub .

## Integrante

- Nombre completo: [sebastian castaño Vargas ]

## Fecha

 24 de noviembre de 2025

## ¿Qué es Git?

Git es un sistema de control de versiones distribuido diseñado para manejar proyectos de software con rapidez y eficiencia. Permite llevar un historial de los cambios realizados en el código, volver a versiones anteriores y colaborar con otras personas sin sobreescribir el trabajo ajeno. Git almacena los cambios en commits que contienen información sobre quién, cuándo y qué se modificó. Al ser distribuido, cada colaborador tiene una copia completa del repositorio, lo que mejora la resiliencia y la velocidad. Git también facilita la creación de ramas para trabajar en funcionalidades aisladas y luego fusionarlas (merge) al proyecto principal. Gracias a sus herramientas de fusión y manejo de conflictos, Git es escalable para proyectos pequeños y grandes. Git se utiliza conjuntamente con servicios remotos como GitHub, GitLab o Bitbucket para sincronizar trabajo entre desarrolladores.

## 10 comandos de Git explicados

1. git init

  Crea un nuevo repositorio Git local en la carpeta actual. Prepara el directorio para empezar a versionar.

2. git clone <url>

  Descarga (clona) un repositorio remoto completo a tu máquina local, incluyendo historial de commits y ramas.

3. git status

  Muestra el estado actual del repositorio: archivos modificados, sin seguimiento (untracked) y qué se ha preparado para commit.

4. git add <archivo|.>

  Añade archivos al área de preparación (staging area) para que formen parte del próximo commit.

5. git commit -m "mensaje"

  Crea un nuevo commit con los cambios preparados y un mensaje descriptivo que explica la modificación.

6. git branch

  Lista las ramas locales. git branch <nombre> crea una rama nueva.

7. git checkout <rama> o git switch <rama>

  Cambia a otra rama. git switch -c <rama> crea y cambia a una nueva rama.

8. git pull origin <rama>

  Trae (fetch) y fusiona (merge) los cambios del remoto a tu rama local. Útil para sincronizar trabajo ajeno.

9. git push origin <rama>

  Envía (push) tus commits locales a la rama correspondiente en el repositorio remoto.

10. git log --oneline

  Muestra el historial de commits de forma compacta. Útil para revisar rápidamente el historial.

## Flujo de trabajo recomendado

1. Trabaja en main únicamente para la versión estable; crea ramas para nuevas funcionalidades:

  - git switch -c feature/nombre-funcionalidad

2. Haz commits pequeños y con mensajes claros:

  - git commit -m "feat: agregar validación de email en registro"

3. Antes de subir, actualiza tu rama con los últimos cambios de main:

  - git fetch origin

  - git rebase origin/main (o git merge origin/main si prefieres merge)

4. Crea un Pull Request (PR) o Merge Request (MR) en la plataforma remota para revisión.

5. Después de aprobación, fusiona a main y elimina la rama de feature.

## Problemas encontrados hoy

- Error al empujar (push): ! \[rejected] main -> main (fetch first) — el remoto tenía commits que no estaban en local.

- Posibles causas: GitHub tenía un commit (README o inicial) y el historial local no coincidía; se intentó git push sin sincronizar primero.

- Acción tomada: se recomienda realizar git pull para integrar los cambios remotos antes de hacer push, o forzar (--force) *solo si* se está absolutamente seguro de sobrescribir el remoto.

## Conclusión del día

Hoy se dejó documentada la estructura básica del proyecto y la configuración inicial del repositorio. Se abordó el problema de sincronización con el remoto y se estableció el flujo de trabajo recomendado para evitar conflictos futuros. Próximo paso: implementar la primera funcionalidad en una rama separada y abrir un Pull Request para revisión.

