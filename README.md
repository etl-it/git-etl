# README ETL

*Este manual constituye una guía de la metodología de trabajo a seguir dentro de la Organización ETL-IT, perteneciente al departamento de Telemática de la Universidad Carlos III de Madrid.*
*Si desea más información o tiene alguna duda tiene a su disposición los sitios web: [Guru IT (Apertura de incidencias)](guru.it.uc3m.es) y [Wiki ETL](etl.it.uc3m.es)*

## Git básico

### Más en profundidad
[ProGit ePub version, 2nd Edition](https://github.com/etl-it/git-etl/blob/master/progit-es.1091.epub?raw=true)


## Permisos dentro de la organización
Existen tres tipos de usuarios: member, billing managers y owner. Los billing managers por el momento vamos a descartarlos ya que trabajamos con la versión gratuita de GitHub.



## Branching
Todos los usuarios de la organización seguirán el siguiente esquema de branching:

![etl-branching](/Git-org-branch.png)

Hay tres tipos de ramas, dos de ellas fijas: ramas de característica (para desarrollo), rama de documentación/integración y rama de pruebas.
Solo desde esta última rama se pueden hacer pull-request al master. Para poder realizar un pull a la rama master desde la rama testing es necesario que al menos otro usuario dé el visto bueno, excepto casos concretos donde se indique lo contrario.

Todas las ramas que contemplen nuevas características deben salir de la rama principal, dado que será la única rama con contenido estable. Pueden crearse ramas más pequeñas de características por debajo de la original, pero solo podrá hacerse **merge con la rama madre**, no con otros antecesores. 

### Creación y gestión de ramas

Al crear ramas deben indicarse iniciales del autor, caracteristica y fecha. Por ejemplo:

~~~
rj-docs-1804
~~~

### Pull requests

##
