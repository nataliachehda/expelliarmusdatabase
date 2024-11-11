# ExpelliarmusDatabase
## Descripción del Proyecto
**Expelliarmus Database** es una base de datos en donde los
 usuarios pueden gestionar y analizar los
 enfrentamientos y aventuras de la saga de Harry
 Potter. También pueden interactuar con los datos para crear sus
 propios enfrentamientos, organizando y analizando los
 resultados de manera dinámica. La base de datos facilita la
 asignación de elementos mágicos para los combates (varitas,
 pociones, hechizos y objetos). También permite hacer un
 seguimiento de los personajes en cada combate, registrando
 sus habilidades, equipo y contribución a la batalla. Además, se
 facilita el cálculo automatizado de los resultados de los
 enfrentamientos, determinando ganadores y perdedores según
 la suma de fuerzas de los bandos involucrados y el poder de los
 elementos utilizados. Los usuarios también tienen la capacidad
 de generar informes personalizados sobre el desempeño de los
 personajes en combate, su historial de batallas, y las
 estadísticas relacionadas con los enfrentamientos. Así se ofrece
 una herramienta organizada y accesible para aquellos
 interesados en explorar y gestionar el fascinante mundo de
 Harry Potter

## Contenidos
1. [Estructura de la Base de Datos](#estructura-de-la-base-de-datos)
2. [Vistas](#vistas)
3. [Funciones](#funciones)
4. [Procedimientos Almacenados](#procedimientos-almacenados)
5. [Instalacion](#instalacion)

## Estructura de la Base de Datos
La base de datos contiene las siguientes tablas:

- **Personajes**: Registra los personajes con sus habilidades y nivel de poder.
- **Elementos mágicos**: Varitas, Hechizos, Pociones y Objetos. Registra cada tipo de elemento mágico con sus características y fuerza.
- **Localizaciones**: Describe los lugares en donde ocurren los enfrentamientos.
- **Bandos**: Identifica los bandos en los cuales participan los personajes.
- **Personajes_Bandos**: Relaciona a los personajes con sus respectivos bandos.
- **Enfrentamientos**: Almacena los enfrentamientos, incluyendo la fecha y ubicación.
- **Personajes_Enfrentamientos**: Relaciona a los personajes en cada enfrentamiento, junto con los elementos mágicos que usaron y su equipo (buenos o malos).

## Vistas
La base de datos incluye vistas que permiten consultas específicas:

- **vista_bandos_integrantes**: Muestra los personajes de cada bando.
- **vista_localizaciones_enfrentamientos**: Lista de enfrentamientos con su ubicación y fecha.
- **vista_personajes_elementos_enfrentamientos**: Registra qué elementos usaron los personajes en cada enfrentamiento.
- **vista_resultados_enfrentamientos**: Presenta el resultado de cada enfrentamiento, incluyendo el bando ganador y perdedor, junto con la fuerza total de ambos.

## Funciones
-**elemento_mas_usado**: Devuelve el elemento mágico más utilizado (por tipo) en los enfrentamientos.
-**calcular_ganador**: Compara dos personajes y determina el ganador según su fuerza total.

## Procedimientos Almacenados
- **apostar_enfrentamiento**: Utiliza calcular_ganador para simular una apuesta en un duelo entre dos personajes y evalúa el resultado.
- **estadísticas_personajes**: Presenta la performance de cada personaje en las batallas, indicando enfrentamientos ganados y perdidos.
- **enfrentar_personajes**: Crea enfrentamientos ficticios entre dos personajes seleccionados, registrando el ganador en la tabla batallas.

## Instalacion
Ejecutar el script SQL proporcionado en un gestor de base de datos compatible (MySQL).
Observar la estructura: se incluyen sentencia de borrado si existe la base para evitar errores, se proporciona en primer lugar las tablas y se insertan los datos en el orden correspondiente. Luego podemos ver las vistas, funciones, store procedures y triggers.