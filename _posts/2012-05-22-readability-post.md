---
layout: post
title: "Estructura de ramas para cada repositorio"
date: 2017-09-28
excerpt: "Como estructurar las ramas en los repositorios de github y que workflow usar"
tags: [github, workflow, rules]
comments: false
---
# Flujo de trabajo (Workflow)
El flujo propuesto de trabajo para el equipo en cuánto al uso de los repositorios es el propuesto por Github, este flujo es llamado
[GithubFlow](https://guides.github.com/introduction/flow/). Este flujo propone el usar *forks* y una única rama *master*.
El flujo que usaremos propone que cada miembro del equipo tenga su *fork* y en vez de usar una rama *master* en cada proyecto, este tenga 2, *master* y *staging*.

## Rama *master* (Producción)
Esta rama se denomina la rama de producción, en esta rama esta el código que se encuentra en el sitio de producción de cada proyecto.
Esta por demás decir que esta rama es donde el proyecto es estable y en donde se encuentran los cambios que el cliente o dueño ha pedido.
No se deben hacer pruebas sobre esta rama, solo los líderes en el departamento pueden tener acceso a escribir sobre esta rama.
Esta rama debe servir como respaldo en caso de que la rama staging se descomponga o tenga problemas.
Solo se debe hacer un *merge* sobre esta rama cuándo se hayan probado y aprobado por los líderes y clientes dueños del proyecto.

Se usará el la estrategia de despliegues programados para hacer *merge* hacia esta rama, esto junto con el uso de [milestones](https://guides.github.com/features/issues/#filtering) para tener registro puntual de las cosas a desplegar.

Junto con el uso de despliegues automáticos se usarán hooks de github para que a la hora de hacer un *merge* hacia *master* estos cambios se desplieguen automaticamente al sitio de producción.

## Rama *staging* (Desarrollo)
La rama de staging sirve como un ambiente en donde se integran todos los PR de los integrantes del equipo y que a su vez sirve como base para todos los cambios y tareas que se deben realizar.
Todos los integrantes deben basar sus cambios en esta rama y deben enviar todos sus PR hacia esta rama a menos que sea necesario enviarlo hacia otra rama pero esto depende del lider del proyecto ó área.
A esta rama siempre se estarán integrando cambios una vez aprobados y probados por el lider o los revizores. Una vez integrado algún cambio y gracias al flujo de integración continua este cambio se desplegará hacia el ambiente de desarrollo o (stage) para que pueda ser validado por el cliente.

## *Pull Request* (PR)
Todos los PR's deben ir hacia la rama *staging*. Hay ciertas reglas que hay que seguir en la creación de un PR, estas en resumen son:
* Deben ir bien documentados
  * Debe explicar el problema que quiere resolver
  * Deben contener imágenes de lo que se hizo
    * Antes y después
  * Deben explicar el procedimiento que llevarón a cabo para resolver el problema
  * Debe contener las instrucciones para que el revizor pueda llevar a cabo la solución en su ambiente local.
* Deben pertenecer a un milestone
* Deben tener un asignado y revisores, en la mayoria de los casos los revisores son los líderes de área pero en determinado caso puede tambien pertenecer a otra área.
![Pull Request]({{ "/assets/uploads/2017/10/pull_request_1.png" | absolute_url }})


## Integración a master
Una vez que pasó un periodo de tiempo en el que se efectuarón pruebas internas y con el cliente es tiempo de pasar a producción, si recordamos que todo lo que este en la rama master
se es lo que debe estar en el ambiente de producción entonces lo que haremos es hacer un PR de la rama *staging* hacia la rama *master*. Esto se hará en el caso de un plan de despliegues programados un día especifico de la semana (que no sea viernes) a una hora específica, esto obviamente acordado anteriormente con el cliente. En otro caso se deberá tratar de hacerlo no mas de 2 veses a la semana, el objetivo es tratar de llevar un seguimiento de lo que se desliega, en el caso de hacerlo un mayor número de veses esto se perdería.

La razón de contar con 2 despliegues es debido a que puede que surga un imprevisto y debamos desplegar una segunda vez. Se trata de hacer un despliegue por periodo de tiempo acordado ya sea *sprint*, *fase* o *módulo*, lo que es lo mismo un despliegue por milestone programado.

El PR de integración debe de tener las siguientes caracteristicas:
* En su descripción deberá ir el link del milestone al que pertenece
* En su título debe ir la leyenda **Integration to master**
* Deberá tener la etiqueta de **integration**
![Pull Request]({{ "/assets/uploads/2017/10/label_1.png" | absolute_url }})
* Deberá asignarse al menos a un revisor

## Milestones
Los milestones son un feature de Github que permite envolver o englobar algunos PR, esto nos sirve para delimitar que cambios se efectuarón y agregaron al proyecto en un periodo de tiempo.
![Milestones]({{ "/assets/uploads/2017/10/milestones_1.png" | absolute_url }})

### Criterios para el uso de un milestone
El uso de milestones en el equipo será para delimitar las tareas que se deban hacer en los periodos de tiempo comprendidos para:
* Sprints
* Fases
* Módulos o features


Es decir un sprint deberá ocuparse para delimitar los PR de las tareas que comprenden un sprint, este puede ser de 1 a 2 semanas de trabajo dependiendo de la organización del proyecto.

Tambien se puede considerar una fase para el uso de un milestone por ejemplo la fase de tareas de mantenimiento que comprende de la fecha x a la fecha y.

Para la creación de un módulo especifico del proyecto podría englobarse en un milestone, es decir dependiendo de la organización manejo del proyecto un feature como **crear el módulo de administracion**
tambien podría considerarse como un milestone.

Abordaremos más a fondo el tema de los milestones en el post de milestones.
