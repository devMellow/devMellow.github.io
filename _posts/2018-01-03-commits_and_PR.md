---
layout: post
title: "Convenciones para ramas, commits, PR y comentarios de Teamwork"
date: 2018-01-03
excerpt: "Como documentar commits, Pull Request, ramas y meta tags para comentarios"
tags: [consulting, guide, git, workflow]
comments: false
---
# Ramas
Siguiendo el flujo de desarrollo que se basa en github flow en donde se crea un fork del proyecto y se hacen ramas de donde se sacan los PR el nombre de las ramas que
se debe seguir en el equpo de desarrollo es el siguiente.

```
{numero de la tarea en teamwork}-{descripcion-corta-de-la-tarea-en-ingles}
```

## Ejemplo
```
1234578-add-readme-file
```

Es decir dependiendo para cada tarea se debe crear una rama con esta especificación, esta puede salir de `staging` o de `QA`

# Commits
Para los commits también se debe seguir un patron y algunas convenciones. Cada commit debe tener una descripción y el debe contener únicamente los cambios y archivos
que definan la descripción, por ejemplo si modifique alguna descripción en el `README.md` un ejemplo de commit será el siguiente.

```
"Change requirements for install on README"
```

## Casos especiales de mensaje
Hay algunos casos en los cuales se requiere una meta etiqueta en el mensaje del commit, estas son:
* `[WIP]`: Esta se ocupa para delimitar que ese commit en especifico contiene cambios que no se han concluidoi o que no estan listos para una revisión, WIP quiere decir *Work In Progress*
* `[RC]`: *Resolve Conflicts*, esta etiqueta se utiliza para indicar que en ese commit se resolvieron conflictos entre ramas, se debe indicar la rama con la que se tuvo comflicto denotando en el mensaje con
la palabra `FROM:`
* `TODO:`: Indica lo que hay que hacer o falta en un commit que se esta trabajando

### Ejemplos:
* `"[WIP] Changes over README TODO: Finish the requirements especifications and contributors`
* `"[RC] Resolve conflicts on README file FROM: eldeibid/123456-change-readme"`

# Pull Request
Los Pull Request(PR) deben ir documentados en lenguaje markdown que es el que ocupa Github por defecto, se deben tener las siguientes secciones en el PR

* **Related task** : En esta sección debe tener el nombre de la tarea tal y como aparece en Teamwork y el link hacia la misma

```
* [Crear documentacion de creacion de ramas y PR](https://mellow.teamwork.com/#tasks/6913838)
```

* **Issue description**: En esta sección se debe describir detalladamente el problema por el cuál surge la tarea, se debe ser lo más descriptivo posible en este punto, el uso de imagenes o
contenido multimedia es muy recomendable y en muchos casos obligado.
* **Solution description**: Esta sección describe detalladamente lo que se llevo a cabo para solucionar el problema, de igual manera el uso de multimedia es muy recomendable y en muchos casos obligado
* **Tests**: En esta sección se deben colocar los pasos que se deben llevar a cabo para probar la solución así como los datos qeu se requieren para la misma en caso de que haya un revizor externo

Las secciones anteriores son obligatorias y se determinará si se puede prescindir o agregar de alguna en caso de que la tarea así lo requiera

# Meta etiquetas para teamwork
## Despliegue
Esta son meta etiquetas qeu se deben poner en los comentarios de Teamwork en caso de:
* `[DS]`: Despliegue a staging
* `[DP]`: Despliegue a producción
* `[PR]`: Indicar la liga del pull request
* `[MR]`: Indica que se hizo merge del PR a una rama, se debe indicar la rama en el comentario
* `[PRI]`: Indicar que es un pull request de integración, por ejemplo cuando se van a pasar cambios de la rama staging a master

### Ejemplo
```
* [PR] https://github.com/devMellow/juslab/pull/62

* [DD] Listo en desarrollo

* [MR] Hacia QA

```

La mayoria de las tareas de desarrollo deberían llevar por lo menos las 3 primeras indicando el url de pull request, el momento en el que se hizo desplieguea desarrollo y a producción.

Estas meta etiquetas sirven a los revisores para ubicar de una manera más rápida estos 3 momentos de la tarea, así como en las notificaciones por mail o móvil.

Estas meta etiquetas son obligatorias para los casos y tareas que se ocupen.

