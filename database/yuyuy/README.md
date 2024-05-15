# Liquibase
## Source Control for your database

Es una libreria opensource para el manejo y ejecución de cambios en base de datos.

## Descripción
Con liquibase podrás llevar el control de versiones de cualquier tipo de base de datos relaciónal, podras llevar una correcta administración de base de datos con tus clientes, sabrás en que version se encuentra cada ambiente y podrás fácilmente hacer refactoring a tus modelos.

Serás capaz de poder construir esquema en cualquier base de datos con un solo desarrollo y podrás integrar la administración de sus bases de datos a la herramienta fácilmente.

## Documentación

Dentro de la siguiente ruta en este repositorio podrás encontrar la documentación
[Documentacion Liquibase](http://devtools.certum.com/bitbucket/projects/ARQ/repos/liquibase/browse/documentacion/Lineamientos.md)

[Ejercicios](http://devtools.certum.com/bitbucket/projects/ARQ/repos/liquibase/browse/documentacion/ejercicios.md)

Mas detalles en: 
[Pagina oficial liquibase](http://www.liquibase.org/)

## Comandos que se pueden ejecutar para distintos propositos:

## Generar un changelog desde una base de datos existente

    liquibase --changeLogFile="changesets/db.changelog-#.#.#.#.xml" generateChangeLog

## Update

    liquibase --changeLogFile="changesets/db.changelog-master.xml" update

## Rollback a un changeset anterior

    liquibase --changeLogFile="changesets/db.changelog-master.xml" rollbackCount 1

## Generar un changelog de diferencias

    liquibase --changeLogFile="changesets/db.changelog-#.#.#.#.xml" diffChangeLog