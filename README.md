# mi-proyecto

Descripción: En esta actividad, el estudiante implementará un flujo básico de DevOps utilizando Git y GitHub, simulando el desarrollo, mantenimiento y despliegue de un proyecto web estático. 


Objetivo: Al finalizar la actividad, el alumno será capaz de:


Configurar Git en su equipo local
Crear y administrar un repositorio en GitHub
Aplicar buenas prácticas de control de versiones
Trabajar con ramas (branches)
Simular un flujo DevOps sin servicios en la nube
Documentar un proyecto de software


Estructura del proyecto: 
mi-proyecto-devops/
│── src/
│   ├── index.html
│   ├── styles.css
│── scripts/
│   └── deploy.sh
│── README.md
│── .gitignore


Flujo de trabajo utilizado: Para este proyecto se utilizó un flujo de trabajo basado en ramas (Feature Branch Workflow), que consiste en los siguientes pasos:

Configuración Local: Clonación del repositorio remoto y configuración de identidad de Git.

Desarrollo en Rama Principal (main): Creación de la estructura base y el primer commit con la versión estable del proyecto.

Automatización (Scripting): Creación de un script de shell (.sh) para simular el proceso de deployment (despliegue) de forma local.

Creación de Ramas de Función (feature-update): Uso de ramas independientes para desarrollar nuevas características sin afectar el código principal.

Integración: Carga de las diferentes ramas al repositorio remoto en GitHub para mantener un historial de cambios organizado.


Comandos Git principales:
Git
GitHub
Editor de código (VS Code, Sublime Text, etc.)
Navegador web 
