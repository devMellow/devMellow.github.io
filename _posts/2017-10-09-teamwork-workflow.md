---
layout: post
title: "Como gestionar un proyecto con Teamwork"
date: 2017-10-09
excerpt: "Como gestionar las tareas de un proyecto con Teamwork para el equipo de Mellow Consulting"
tags: [consulting, guide, teamwork]
comments: false
---
# Teamwork
Teamwork es la herramienta para gestión de tareas que ocupamos en Teamwork, en esta guia se tratarán la gestión desde 2 perfiles en el equipo,
la parte administrativa y la del equipo de desarrollo, si bien las 2 conviven en la gestión de trabajo los procesos y responsabilidades son un poco diferentes en
el flujo de trabajo.

Se da por hecho que para seguir los pasos de esta guía el lector es un miembro del equipo de Mellow Consulting dado de alta en el Teamwork

# Proyectos
Todo el equipo de Mellow Consulting debe gestionar el trabajo en tareas de Teamwork, la manera de hacer esto es delimitando el trabajo en **proyectos**.
Cada proyecto debe de tener tareas que dividan el trabajo de dicho trabajo. Cada proyecto debe cumplir las siguientes caracteristicas:
* Debe tener un grupo de miembros de especialidades diferentes ya sea, diseño, desarrollo, marketing, project managers, etc.
* Cada miembro debe de tener un role especifico para su especialidad.
* Cada proyecto debe tener un **project manager**
* Cada proyecto debe de tener un nombre único que represente y defina su contexto, este nombre debe de ser corto y todos los miembros de consulting deben de identificarlo fácilmente.
* Cada proyecto debe de tener tasklist que delimitan un grupo de tareas y que se pueden utilizar como *milestone*.
* Generalmente los proyectos se definen en el contexto de Mellow Conculting por el cliente para quien es el proyecto.
* Cada proyecto debe de tener un responsable por área que este relacionada con el proyecto, esto no limita al número de integrantes por área.
* Las tareas de cada deben ser gestionadas principalmente por el **project manager** así como por los responsables del área.
* Los proyectos deben estar a su vez divididos en milestones, estos delimitan un número de tareas que se realizarán en un periodo de tiempo acordado.
* Cada proyecto debe tener una vista de **Board** en donde deben estar las coumnas *backlog*, *sprint*, *in progress*, *on validation* y *done*.

## Creación de proyectos en Teamwork
El miembro debe tener los permisos para la creación de nuevos proyectos.
Para crear un proyecto y estando dentro del dashboard de Teamwork solo se debe ir a la sección de **proyectos**

![Projects]({{ "/assets/uploads/2017/10/projects_1.png" | absolute_url }})

Esto nos lleva al dashboard de proyectos en donde veremos los proyectos activos a los que tenemos acceso en la organización.

![Projects]({{ "/assets/uploads/2017/10/projects_2.png" | absolute_url }})

En esta sección podemos ver un botón que nos permitirá agregar un nuevo proyecto.

![Projects]({{ "/assets/uploads/2017/10/projects_3.png" | absolute_url }})

Al darle click nos aparecerá un modal en el cuál podremos colocar la información del proyecto en cuestión.

![Projects]({{ "/assets/uploads/2017/10/projects_4.png" | absolute_url }})

## Agregar miembros al proyecto
En todos los proyectos deben estar agregados solo los miembros del equipo que esten trabajando en el. Para agregar a un miembro al proyecto primero debe estar agregado a la organización.
Una vez dicho esto, para agregar a un miembro al proyecto nos debemos dirijir a el dashboard del proyecto, esto se hace elijiendo el proyecto en cuestión en el panel de projectos.
Una vez en el dashboard del proyecto podremos ver todas las opciones en el menú, una de ellas es **People** o **Personas** (esto puede variar dependiendo de la versión de Teamwork o el lenguaje)

![Projects]({{ "/assets/uploads/2017/10/projects_5.png" | absolute_url }})

Una vez en este panel solo se da click en el boton **add people**

![Projects]({{ "/assets/uploads/2017/10/projects_6.png" | absolute_url }})

Y se abrirá un modal en donde se tendrá que escojer de entre los miembros de la organización cuál es el que debemos agregar.

![Projects]({{ "/assets/uploads/2017/10/projects_7.png" | absolute_url }})

# Tareas
Las tareas son la parte fundamental de un proyecto, estas le dan sentido y existencia a un proyecto en Teamwork.

Las tareas deben cumplir con ciertas caracteristicas en un proyecto, estas son:
* Deben de tener solo un responsable a menos que sea una tarea en la que se deba checar por varios miembros del equipo, or ejemplo una revisión o junta

![Tasks]({{ "/assets/uploads/2017/10/tasks_1.png" | absolute_url }})

* El nombre debe comenzar con una tag entre brackets ([]) y en mayúsculas, esta tag describirá el contexto o sección a la que pertenece la tarea.
Por ejemplo [LANDING] o [HOME].

![Tasks]({{ "/assets/uploads/2017/10/tasks_2.png" | absolute_url }})

* El titulo de la tarea debe ser corto pero claro para poderla identtificar
* Se debe agregar una descripción más específica siempre con excepción de que con el título sea claro, el responsable de realizar la tarea siempre puede pedir que la descripción sea más específica
adjuntando imágenes, archivos, etc.

* La tarea debe pertenecer a un **tasklist** para que pueda ser agrupado en un **milestone**

![Tasks]({{ "/assets/uploads/2017/10/tasks_3.png" | absolute_url }})

* La estimación siempre debe ponerla la persona final que realizará la tarea así como la fecha de inicio y fin, se puede sugerir una fecha de inicio y de fin pero no se debe colocar fecha de inicio y fin
si la tarea no ha sido estimada y valorada por el responsable.

* La prioridad de la tarea también depende de un consenso entre la parte administrativa y el área responsable. Puede haber tareas urgentes pero eso estas se deben ocupar en casos muy extremos.

Estos puntos son los mínimos que debe cumplir una tarea en la plataforma para el equipo.

## Crear task

Aparte de las consideraciones anteriores una tarea tambien puede tener:
* Prioridad
![Tasks]({{ "/assets/uploads/2017/10/tasklist_5.png" | absolute_url }})
* Fecha de inicio y fecha de fin

![Tasks]({{ "/assets/uploads/2017/10/tasklist_6.png" | absolute_url }})

* Tiempo estimado de desarrollo

![Tasks]({{ "/assets/uploads/2017/10/tasks_4.png" | absolute_url }})

* Descripción de la task
Siempre se debe de describir muy bien una tarea para evitar perdida de tiempo rebotandola entre el responsable y el solicitante, siempre se podrá rebotar una tarea si el ejecutante no la comprende.

* Una vez que se tengan estos datos se debe de colocar un responsable de la tarea, este no siempre es el que la va a realizar ya que puede pasar por un lider antes para que este la asigne a alguien de su equipo, esto depende del flujo que se maneje en el área y proyecto.


## Crear *tasklist*
Un **tasklist** sirve para agrupar un conjunto de tareas con un fin en común, este puede ser para:
* Delimitar áreas en un desarrollo por ejemplo *backend*, *design*, etc.
* Delimitar un periodo de tiempo; *sprint 1*, *desarrollo del 5 al 10 de octubre*
* Delimitar alguna fase del proyecto; *Fase 1*, *ajustes post-entrega*

Para crear un *tasklist* se debe de estar en el dashboard de un proyecto en la sección de **tasks**

![Tasklist]({{ "/assets/uploads/2017/10/tasklist_1.png" | absolute_url }})

Para añadir un taskslist hay que dar click en el botón de **add tasklist**

![Tasklist]({{ "/assets/uploads/2017/10/tasklist_2.png" | absolute_url }})

Nos saldrá un modal en donde debemos especificar el detalle de la tasklist

![Tasklist]({{ "/assets/uploads/2017/10/tasklist_3.png" | absolute_url }})

Una vez creada la tasklist solo hay que arrastrar las tareas que correspondan a ese tasklist, esto depende del fin del tasklist, como lo mencionamos estos
pueden ser para definir un periodo de tiempo, una fase y área.

![Tasklist]({{ "/assets/uploads/2017/10/tasklist_4.png" | absolute_url }})


# Milestones
Los milestones no son más que un grupo de tareas de un proyecto delimitadas en un periodo de tiempo acordado, por ejemplo el proyecto de Juan tiene 20 tareas que estan divididas en
milestones de 1 semana de duración, el primer milestone corresponde a la creación de la landing page que va del 1 al 5 de enero.
Hay que tener las siguientes consideraciones para la creación de milestones:
* Para la creación de milestones se requiere que primero esten creadas y estimadas las tareas del proyecto por el miembro del equipo que la va a realizar.
* Ver la disponibilidad de tiempo que el integrante o integrantes del equipo responsables de esas tareas ya que si contamos con que una tarea esta estimada en 8 horas (un día laboral)
puede que el miembro del equipo solo este programado para dedicarle 4 horas (dos días laborales) a esa tarea. Por eso es importante estimar las tareas en un principio y reguntar por la
disponibilidad de tiempo de los equipos para ese proyecto, esto con el fin de calcular mejor el sprint.
La operación es fácil, con tareas estimadas y disponibilidad de los equipos se delimitan sprints que se adecuen a la disponibilidad de tiempo de los equipos.
* No olvidar que las tareas tienen una duración **estimada**, en realidad cuándo se trata con trabajos como los que el equipo de Mellow Consulting trabaja (marketing, desarrollo y diseño)
se debe considerar siempre los factores humanos del equipo como la concentración, enfermedad, motivación, etc. Una estimación también esta directamente relacionada a la experiencia de quien
la va a realizar.
* Un milestone debe tener una fecha de inicio y fin, esto depende del cálculo de la disponibilidad de los integrantes contra las horas estimadas en ese periodo de tiempo.
* Siempre debe haber un producto o **entregable** funcional al final de cada milestone, es decir la conclución de un milestone siempre debe ser algo funcional que el cliente final pueda usar, pensemos que los milestones deben ser calculados sobre un **mínimo producto viable** *(MVP)*. No hay excusa al final de cada milestone siempre debemos entregar algo que el usuario final pueda usar.
* Un milestone debe tener una tasklist y una tasklist debe pertenecer a un milestone

## Crear un milestone
Para crear un milestone se debe estar en el dashboard del proyecto en cuestión.


![Milestones]({{ "/assets/uploads/2017/10/milestones_1.png" | absolute_url }})

![Milestones]({{ "/assets/uploads/2017/10/milestones_2.png" | absolute_url }})

Damos click en el boton *add milestone*

![Milestones]({{ "/assets/uploads/2017/10/milestones_3.png" | absolute_url }})

Se nos abrirá un modal en el que especificaremos los detalles del milestone, para este se deben de tener estas consideraciones.
* En caso de que el milestone pertenezca a una **fase de desarrollo** se deberá colocar un titulo parecido a: **Fase: [nombre de la fase]**
* En caso de que el milestone pertenezca a un **periodo de tiempo** se deberá colocar un título como: **Desarrollo del [dia de inicio] hasta el [día de fin] de [mes]**
* En caso de que el milestone pertenezca a un **área** del equipo este deberá colocar un título como: **[AREA] hasta el [dia de fin] de [mes de fin]**

También se debe especificar la fecha de fin del milestone


![Milestones]({{ "/assets/uploads/2017/10/milestones_4.png" | absolute_url }})

Al final tambien se debe agregar una tasklist al milestone


![Milestones]({{ "/assets/uploads/2017/10/milestones_5.png" | absolute_url }})


# Flujo de trabajo en teamwork

Una vez vistos los puntos anteriores ahora debemos crear un flujo de trabajo entre las áreas del equipo en un proyecto, en resumen es el siguiente.

* El **solicitante** crea la(s) tarea(s) con una descripción clara de lo que se debe realizar, coloca como **responsable** ya sea al lider del área a quien va dirigida la tarea o al responsable directamente,
esto depende del flujo acordado para el proyecto.

* El **responsable** coloca en la tarea sus comentarios si es que los hay y estima la tarea, en caso de que no quede claro lo que se debe realizar en la tarea debe colocar sus comentarios y cambiar el responsable de la tarea por la persona que le tenga que resolver esas dudas. En el caso de que haya dudas se entra en un ciclo de comentarios en la tarea hasta que estos se resuelvan y se pueda estimar la tarea.

* Una vez estimada el solicitante pone sus comentarios, la coloca en un tasklist, asigna un milestone y devuelve cambiando el responsable de a tarea al área que la va a ejecutar.

* El área ejecutante deberá realizar las tareas y colocar comentarios en caso de tener obstáculos, reestimar la tarea, terminarla, desplegarla, etc.

