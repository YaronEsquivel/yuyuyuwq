# Se describen algunas recomendaciones para el uso de la herramienta liquibase

## Nombrado de changesets

`<changeSet author="authorName" id="changelog-1.0">`

* Auhor: Se debe especificar el nombre de usuario de quien aplica los cambios.
* id: Es un número único para identificar el cambio, podría ser el numero de issue atendido y la fecha en que se aplica el cambio
Ej: TICKET-180117-001

## Orden de los changesets

Por ningun motivo se deben de alterar los changesets ya insertados o manipular las tabla de control a mano, ya que esto podría provocar incosistencias que liquibase ya no podría manejar de manera segura.
En caso de ser estrictamente necesario alterar las tablas de control,se debe notificar al equipo involucrado para detener la aplicación de cambios hasta que se realice la correción.

## Generación de nuevos archivos changelog

```xml
<databaseChangeLog xmlns="http://www.li....">
  <include file="db.changelog-1.0.xml"/> 
  <include file="db.changelog-1.1.xml"/> 
  <include file="db.changelog-2.0.xml"/> 
</databaseChangeLog>
```

* Se deberá generar un nuevo archivo changelog en cada nueva (version, sprint, entregable) para poder relacionar nuestra version de bd con la versión del código correspondiente.


[Regresar](http://devtools.certum.com/bitbucket/projects/ARQ/repos/liquibase/browse)