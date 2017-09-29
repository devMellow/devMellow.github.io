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
Todos los integrantes deben basar sus cambios en esta rama.
