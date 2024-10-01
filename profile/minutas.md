# Introducción 

El siguiente texto tiene como objetivo detallar los puntos importantes que vamos hablando durante las reuniones con Carlos.

## 5 de Agosto

- Los tutores definen antes de comenzar la cursada cuantos grupos van a poder tutorear
- Junto a los temas, viene un booleano que indica si el tema puede ser tomado por mas de un equipo. (unico/no_unico)
- Necesitamos las columnas: `LEGAJO(PADRON),NOMBRE,APELLIDO,EMAIL` - Evaluar si no debemos hacerlos desde el lado del backend.
- Recordarle a Carlos el servidor
- Posterior a cargar los csv agregar tabla con los resultados
- Si alumno selecciona "tengo tema y tutor, darle la posibilidad de poner el tema y el tutor (mail del tutor)"

## 19 de Agosto

- Tutor, Invitado, Auxiliar -> Son todos tutores
- Este cuatrimestre hay menos alumnos que antes (73 alumnos)
- Joquin Gomez nos aportaria trabajo y ale molinari tutorearia nuestro grupo. Tenemos que definir el alcance y realizar una reunion con los todos.
- Hosting - Alternativa de hostearlo localmente exponiendo el puerto.

## 30 de Septiembre

- No necesariamente tiene que ser tutor para revisar una propuesta.
- Los equipos ya están enviando las propuestas de la manera
tradicional. Carlos decidió que se haga de esta forma para acelerar el
proceso.

- Updates
    - Hosteo
        - La posibilidad de reunirse con el equipo de IT es muy
remota. Hoy por hoy no es algo que tenga solución para el momento de
presentar/finalizar el sistema
    - Front
        - Anteproyecto
            - Desde el front pedir un título para el archivo que se sube
            - Mostrar tutor y título
            - Permitir asignar revisor. Este proceso tiene que ser
manual porque es muy subjetivo, Carlos evalúa el tema y el tutor a la
hora de elegir el revisor de un equipo.
        - Login
            - Gestionar el acceso utilizando firebase oauth
            - Google access
        - Tutor
            - Mejorar la nomenclatura del learning path utilizada para el tutor
                - Aprobado vs Desaprobado
            - Learning path
                - Mostrar todo pero grisar las fases que todavía no
están disponibles
        - Admin
            - Agregar o cambiar la nomenclatura de “Algoritmos” para
que sea más friendly
            - Agregar “activar” en la columna de toggles ← ya agregue
esta nota arriba, la saco
            - “General” y “Dashboard” hacen lo mismo, cambiarlo por “Inicio”.
            - Agregar fotos de usuarios, es más amigable.
    - Back
        - Agregar titulo al csv que se guarda
        - asignar revisor a un grupo
        - devolver tutor y título del archivo
    - Next steps
        - ¿Qué hacemos con el cuatri que le corresponde la asignación
de fechas de exposición? Mejorar el formulario de google que usamos
con el cuatri anterior. Si llegamos con el tiempo, la idea es que se
incluyan en el sistema.
        - Back: como se puede hacer storage de eso?
        - ¿Duración de persistencia de datos? La idea es guardar el
historial de los trabajos profesionales. Guardar siempre los informes
finales. Limpiarlos cada 2 años. Todos los datos salvo el informe
final, los cuales se guardan de manera permanente.

- Tareas

    - Para próximas reuniones mostrar informes de avances
        - compromisos
        - avances de compromisos: estados
        - métricas de avance
        - identificar riesgos como (hosting, seguridad), planificar
planes de contingencia y mitigación
