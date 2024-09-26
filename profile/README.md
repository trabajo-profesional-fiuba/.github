# Trabajo Profesional - 1C2024

## Sistema de seguimiento y gestión administrativa para Trabajos Profesionales de la Facultad de Ingeniería de la Universidad de Buenos Aires

[![Static Badge](https://img.shields.io/badge/documentacion-v1-blue)](https://trabajo-profesional-fiuba.readme.io/docs/getting-started)

### Integrantes

| Rol      | Nombre y Apellido    | Mail                |
| -------- | -------------------- | ------------------- |
| Alumno   | Celeste Dituro       | cdituro@fi.uba.ar   |
| Alumno   | Victoria Abril Lopez | vlopez@fi.uba.ar    |
| Alumno   | Iván Lautaro Pfaab   | ipfaab@fi.uba.ar    |
| Alumno   | Alejo Villores       | avillores@fi.uba.ar |
| Tutor    | Carlos Fontela       | cfontela@fi.uba.ar  |
| Co-tutor | Iván Terzano         | iterzano@fi.uba.ar  |

## Motivación 🏆

El cambio de plan de carrera de Ingenieria Infomatica en el año 2023 abrio la posibilidad de una nueva materia para facilitarle a los estudiantes el desarrollo y entrega de su Trabajo Profesional, facilitando las etapas que en años anteriores solían poner trabas en el proceso a tal punto que habia alumnos a punto de recibirse que decidian dejar la carrera dado que no podian avanzar con esta etapa final.

Como toda materia reciente, presenta muchisimos desafios y sorpresas que no estan contempladas al momento de su creación. 

Nosotros, tenemos el objetivo de facilitar, automatizar y mejorar la calidad de la materia desde el lado de la ingenieria informatica, aplicando herramientas, técnicas y metodologias para desarrollar un software que proporcione todas las cualidades mencionadas anteriormente.

Nos guiamos con la filosofia _"El valor que estamos aportando, es mejor que lo antes habia?"_.

## Informe

El informe tiene como objetivo formalizar el trabajo que se realiza durante los meses que dura el Trabajo Profesional. Se explica en el, varias decisiones, aspectos, conceptos y propositos que hacen que este trabajo tenga como resultado un trabajo final para la carrera de Ingenieria Informatica.

Durante los meses de desarrollo se ira agregando, modificando y borrando diferentes aspectos del siguiente [Informe](https://docs.google.com/document/d/1OGQHTen0Jq10fhsqWkeuYwOUYCHxB5LMsyyRzwK2HSs/edit?usp=sharing). En el se encuentran secciones donde se detalla las distintas decisiones, algoritmos y pruebas que el equipo realizo.

## Minutas con el tutor
[Minutas con Carlos](https://github.com/trabajo-profesional-fiuba/.github/blob/main/profile/minutas.md)

## Arquitectura 👷

Nuestra arquitectura principal se encuentra montada en la **nube**. Utilizamos como provedores **Microsoft Azure** y **Render**.

La **calidad** del desarrollo y la facilidad de integrar codigo constantemente y dinamicamente es algo principal que el equipo busca y trata de seguir las mejores practicas dentro de las posibilidades que actualmente tenemos en terminos de tiempos y costos.

![image](https://github.com/user-attachments/assets/9bf66605-c82e-41bd-b211-7c5cd4c4a72b)

## Desarrollo 📑

Cada repositorio posee en sus `README.md` informacion relevante apropiada a ese proyecto. Ambos proyectos comparten el mismo backlog y Kanba board donde los tickets tienen un seguimiento mediante propiedades. 

El equipo de desarrollo sigue la metodologia de trabajo agil, tomando componenentes de Scrum para poder organizar su trabajo de la mejor manera posible.

Para eso cada tarea se encuentra descripta en el [Backlog](https://github.com/orgs/trabajo-profesional-fiuba/projects/1) donde se detalla la `Priority`, `Kind` y `Status`. De esta manera las tareas poseen diferentes categorias que hacen que el equipo elija en cada sprint cuales son las necesarias para aportar la mayor cantidad de valor.

Ademas, las issues siguen un workflow que se encuentra en formato de tablero [Kanban](https://github.com/orgs/trabajo-profesional-fiuba/projects/1/views/2) donde cada tarea pasa por diferentes estados antes de ser cerrada.

**Time Tracking** ⏲️. Para poder registrar la cantidad de tiempo que nos llevan las tareas se propone utilizar Google Calendar, donde se registra la tarea como un evento que pertence al calendario que el grupo armo. Luego, cada domingo se corre un script automatizado que recorre los eventos y construye una planilla de datos con los mismos.

Para los **PRs**, hemos adoptado una IA que nos realiza un resumen de lo realizado, esta es invocada llamando dentro de la descripciona la hora de crear el PR `@coderabbitai summary`. 

## Licencias

En esta sección, menciona las licencias aplicables a la API. Si hay restricciones de uso o condiciones específicas, asegúrate de comunicarlas claramente.
