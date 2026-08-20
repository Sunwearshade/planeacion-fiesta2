# XV Años María — Demostración educativa de Git

Este repositorio es una **demostración educativa de Git aplicado al control de versiones de un proyecto real de organización**: la fiesta de **XV años de María Fernanda Ríos Salas**, programada para el **14 de marzo de 2026**.

No es una aplicación ni un programa. Son archivos de documentación (Markdown y CSV) que representan los entregables del proyecto. Lo importante aquí **no son los archivos, sino el historial de Git**: cada fase de la administración de proyectos quedó registrada en un commit.

## Las 5 fases del proyecto y sus commits

| # | Fase de administración de proyectos | Mensaje del commit | Carpeta | Qué se documentó |
|---|-------------------------------------|--------------------|---------|------------------|
| 1 | **Inicio** | `Define proyecto de XV años` | `01-inicio/` | Acta de constitución, interesados, viabilidad |
| 2 | **Planificación** | `Agrega planificacion del evento` | `02-planificacion/` | EDT, cronograma, presupuesto, riesgos |
| 3 | **Ejecución** | `Registra ejecucion y proveedores` | `03-ejecucion/` | Tareas ejecutadas y contratos con proveedores |
| 4 | **Seguimiento y control** | `Agrega seguimiento y control` | `04-seguimiento/` | KPIs y control de cambios |
| 5 | **Cierre** | `Cierra proyecto y documenta lecciones` | `05-cierre/` | Entregables finales y lecciones aprendidas |

Además existe la rama **`cambio-banquete`**, donde se registró una solicitud de cambio (incremento del costo del banquete) que después se integró a `main` mediante un **merge**.

## Estructura del repositorio

```text
planeacion-fiesta2/
├── README.md
├── 01-inicio/
│   ├── acta-constitucion.md
│   ├── interesados.md
│   └── viabilidad.md
├── 02-planificacion/
│   ├── edt.md
│   ├── cronograma.md
│   ├── presupuesto.csv
│   └── riesgos.md
├── 03-ejecucion/
│   ├── tareas.md
│   └── proveedores.md
├── 04-seguimiento/
│   ├── kpis.md
│   └── cambios.md
└── 05-cierre/
    ├── entregables.md
    └── lecciones-aprendidas.md
```

## Conceptos de Git explicados con este proyecto

**¿Qué es Git?**
Git es un sistema de **control de versiones**: guarda "fotografías" del proyecto a lo largo del tiempo. Permite ver quién cambió qué, cuándo y por qué, regresar a una versión anterior y trabajar en equipo sin sobrescribir el trabajo de los demás. Aquí lo usamos para versionar la documentación de una fiesta de XV años, no código.

**¿Qué es un commit?**
Un commit es una **versión guardada** del proyecto, con un mensaje que explica el cambio. En esta demostración cada fase del proyecto es un commit: el primero es el inicio, el segundo la planificación, y así sucesivamente. El historial de commits *es* la historia del proyecto.

**¿Qué es una branch (rama)?**
Una rama es una **línea de trabajo paralela**. Permite probar un cambio sin afectar la versión oficial. Aquí creamos la rama `cambio-banquete` para registrar un aumento en el costo del banquete: mientras el cambio vivía en esa rama, `main` seguía intacta con el presupuesto original.

**¿Qué hace `git add`?**
Prepara (agrega al *staging area*) los archivos que quieres incluir en el siguiente commit. Es decir: "estos cambios sí van en la próxima versión". `git add .` agrega todo lo modificado.

**¿Qué hace `git push`?**
**Sube** los commits locales al repositorio remoto (GitHub), para respaldarlos y compartirlos con el equipo.

**¿Qué hace `git pull`?**
**Baja** los cambios que otras personas subieron al repositorio remoto y los integra en tu copia local. Es lo contrario de `push`.

**¿Qué hace `git merge`?**
**Integra** el trabajo de una rama dentro de otra. Aquí, `git merge cambio-banquete` trajo el presupuesto actualizado desde la rama hacia `main`, dejando el cambio aprobado en la versión oficial.

## Comandos útiles para revisar la demostración

```bash
git log --oneline --graph --all   # historial visual con ramas
git status                        # estado actual del repositorio
git diff                          # cambios aún no preparados
git branch                        # lista de ramas
git show <hash>                   # detalle de un commit
```
