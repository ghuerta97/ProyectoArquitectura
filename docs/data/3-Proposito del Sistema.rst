Proposito del sistema
=================================

Descripción del problema - Contexto
--------------------------
Para implementar las herramientas de producción de software y su documentación [5–8] referidas en la introducción, se considera el problema de la creación de una aplicación web y móvil, que permita obtener parámetros medioambientales como temperatura y humedad, y visualizarlos gráficamente en un periodo de tiempo definido por el usuario.

Adicionalmente, se debe mantener un foro de preguntas y respuestas sobre la situación climática para los usuarios del sistema, en particular a través de la visualización de la aplicación a través del sistema operativo Android.


.. image:: images2/diagramacontexto.png
    :scale: 70 %
    :align: center

Visión, objetivos y área
----------------

- Visión: Producir software robusto y de alta calidad que entregue valor a sus usuarios, en base a métodos sistemáticos fundamentados en modelos y documentación, con un importante enfoque arquitectural.
- Objetivos: Concebir, diseñar e implementar una aplicación móvil y web siguiendo A Visual Ad-Hoc Methodology, que permita capturar, visualizar y establecer un diálogo con expertos, sobre parámetros medioambientales. Dar un valor esencial a la documentación en la producción de la aplicación, siguiendo A Template for Documenting Software and Firmware Architectures.
- Área: Tecnologías de la información aplicadas a la meteorología, con el fin de entregar información de interés a un usuario genérico y a pequeñas empresas agrícolas para entregar una mejora potencial en sus procesos de negocio.

Stakeholders
-----------------
- Administrador de preguntas de usuarios: Interesado en administrar los permisos de usuario, filtrar la publicación de preguntas y responderlas.

- Usuario móvil: Usuario final de la aplicación móvil. Está interesado en visualizar gráficamente los parámetros medioambientales en un periodo de tiempo de los disponibles: durante el día, por semana y por mes.

- Usuario web: Usuario final de la aplicación web. Está interesado en visualizar gráficamente los parámetros medioambientales en un periodo de tiempo de los disponibles: durante el día, por semana y por mes.

- Pequeños empresarios agrícolas: Interesado en alimentar la información disponible para la toma de decisiones de negocio en base al historial de parámetros medioambientales en sus plantaciones.

Historias de usuario
-----------------

-----------------
Usuario móvil
-----------------

1.-Como un usuario móvil quiero poder realizar una pregunta medioambiental con la finalidad de que un usuario web me responda y sea publicada en un foro medioambiental.


2.-Como un usuario móvil quiero poder desplegar un listado de preguntas medioambientales clasificadas por categoría de contestadas, no contestadas y todas las preguntas con la finalidad de leer preguntas hechas por otros usuarios con sus respectivas respuestas.


3.-Como un usuario móvil quiero poder desplegar una gráfica de datos de humedad y temperatura en un intervalo de tiempo con la finalidad de comparar temperaturas históricas.

-----------------
Usuario web
-----------------

4.-Como un un usuario web quiero poder desplegar una gráfica de datos de humedad y temperatura en un intervalo de tiempo con la finalidad de comparar temperaturas históricas.


5.-Como un usuario web quiero poder responder una pregunta medioambiental hecha por un usuario movil con la finalidad de que mi respuesta sea publicada en el foro.

-----------------
Usuario moderador
-----------------

6.-Como un usuario administrador quiero poder administrar los usuarios del sistema con la finalidad de eliminar a usuarios irrespetuosos.


7.-Como un usuario administrador quiero poder gestionar todas las preguntas del sistema con la finalidad de poder eliminar preguntas y/o respuestas.


8.-Como un usuario administrador quiero poder tener la capacidad de permitir o no permitir si las preguntas y respuestas puedan ser o no publicadas con la finalidad de restringir mensajes ofensivos e inadecuados.



Requerimientos no funcionales
-----------------
- Se hace uso de una sistema de registro y de inicio de sesión para aumentar la seguridad y usabilidad de la aplicación. La autenticación permite establecer un blackboard de preguntas y respuestas donde la identidad de los participantes es no repudiable. Por otra parte, permite definir distintos roles de usuario, en particular para el caso del administrador.
- El rendimiento de la aplicación se ve potenciado por un enfoque minimalista de diseño, es decir, sólo contiene elementos que aportan significativamente a su funcionalidad o usabilidad.
- El sistema es extensible al estar conformado por servicios independientes encapsulados que pueden ser reutilizados. Esto se refleja en particular para los servicios de "Backend" y "App", donde si bien se encuentran acoplados en el flujo de actividades del sistema, pueden comunicarse con otros servicios en una evolución del sistema o ser independientemente considerados para otros sistemas.
