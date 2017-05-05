# README ETL

*Este manual constituye una guía de la metodología de trabajo a seguir dentro de la Organización ETL-IT, perteneciente al departamento de Telemática de la Universidad Carlos III de Madrid.*
*Si desea más información o tiene alguna duda tiene a su disposición los sitios web: [Guru IT (Apertura de incidencias)](guru.it.uc3m.es) y [Wiki ETL](etl.it.uc3m.es)*


## Branching
Todos los usuarios de la organización seguirán el siguiente esquema de branching:

![etl-branching](/Git-org-branch.png)

Hay tres tipos de ramas, dos de ellas fijas: **ramas de característica (para desarrollo), rama de documentación/integración y rama de pruebas**.
**Solo desde la rama testing se puede hacer pull-request al master**. 

Todas las ramas que contemplen nuevas características deben salir de la rama principal, dado que será la única rama con contenido estable. Pueden crearse ramas más pequeñas de características por debajo de la original, pero solo podrá hacerse **merge con la rama madre**, no con otros antecesores. 

### Creación y gestión de ramas
Al crear ramas deben indicarse iniciales del autor, caracteristica y fecha. Por ejemplo:

~~~
rj-docs-1804
rj-docsv2.0-1904
~~~
El segundo ejemplo sería una rama que nace de la primera, sobre una característica en la que ya estábamos trabajando añadimos más cosas. Luego tendríamos que hacer merge sobre la primera rama y seguir normalmente. **No hay límite de profundidad de ramas** siempre y cuando se haga un uso inteligente que no desbarate el repositorio con muchas versiones de cosas que no llegan a terminarse (no pasan a las ramas siguientes ni al master).

Todos los repositorios deben tener al menos las siguientes ramas:
~~~
master
integration
testing
~~~

Las ramas *dev* solo son obligatorias cuando se añade nuevo contenido, pero no tienen por qué mantenerse en el repositorio una vez se ha terminado con ellas.

### Integración y documentación
La rama de documentación/integración tiene como fin unificar características antes de pasar a la rama de testing y añadir lo necesario para la correcta comprensión del código: comentarios, mensajes de debug, documentación...

Debe estar bien documentado para poder pasar luego a la rama testing. Debe documentarse para que lo entienda cualquiera que no tenga que ver con el código o el repositorio.

### Testing
La rama de testing es autoexplicativa, se utilizará para depurar el código y probarlo en clientes (o donde sea menester). De aquí el código debería salir completo y funcionando, en su versión estable, para poder hacer pull de aquí al master.

### Pull requests
Para poder realizar un pull a la rama master desde la rama testing es **necesario que al menos otro usuario dé el visto bueno**, excepto casos concretos donde se indique lo contrario.

### IMPORTANTE
**Se recuerda que las ramas de integración y testing no deben eliminarse nunca, solo se pueden eliminar las ramas dev una vez se ha terminado con ellas**


## Permisos
### Organización
Existen tres tipos de usuarios: member, billing managers y owner. Los billing managers por el momento vamos a descartarlos ya que trabajamos con la versión gratuita de GitHub.
Por defecto a los usuarios nuevos se les etiqueta como members, [aquí un enlace sobre permisos según el rol](https://help.github.com/articles/permission-levels-for-an-organization/).

### Repositorio
En cuanto a los permisos en cada repositorio concreto tenemos tres básicos: read, write y admin. Hay que tener en cuenta que los usuarios que figuren en la organización como owner tendrán permisos especiales también dentro de los repositorios.
Los permisos más interesantes son los de write y admin para colaboradores del repositorio, [aquí pueden verse los permisos que conlleva cada rol dentro del repositorio](https://help.github.com/articles/repository-permission-levels-for-an-organization/)


## Projects
Para los proyecto se utilizará el método [Kanban](https://es.wikipedia.org/wiki/Kanban_(desarrollo)). Se crearán los proyectos necesarios para lo que se esté desarrollando y un proyecto concreto con información sobre las ramas de desarrollo que se vayan creando. Por ejemplo, el Proyecto Ambari es un proyecto Big Data que despliega un sistema distribuido, por lo tanto cuenta con las [pizarras](https://github.com/RyuS3ki/ambari-etl/projects) (o proyectos) siguientes: servidor, cliente, servicios y branch info.

## Cosas interesantes
### Git básico
[Manual ETL](https://docs.google.com/a/uc3m.es/document/d/1AymDs7Jm28_VOf0QsCYPWyv69oOD8kFmtP0JYTx9FNw/edit?usp=sharing) (Solo con correo UC3M)
[Git Cheatsheet](https://www.git-tower.com/blog/content/posts/54-git-cheat-sheet/git-cheat-sheet-large01.png)

### Más en profundidad
[ProGit ePub version, 2nd Edition](https://github.com/etl-it/git-etl/blob/master/progit-es.1091.epub?raw=true)


_Rebeca Jiménez Guillén, mayo de 2017_

