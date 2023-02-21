Documentación API
Descripción

Esta API provee acceso a información sobre películas y series de diferentes plataformas. Los datos provienen de un conjunto de datasets ya limpios y transformados.
Consultas disponibles
Película con mayor duración

Devuelve la película con mayor duración de acuerdo a los filtros opcionales especificados.

URL
/movies/get_max_duration/{year}/{platform}/{duration_type}

Parámetros URL

    year (opcional): año de estreno de la película.
    platform (opcional): plataforma en la que se encuentra la película.
    duration_type (opcional): tipo de duración de la película. Valores posibles: "min" (minutos) o "season" (temporadas).


# Cantidad de películas por plataforma con un puntaje mayor a XX en determinado año

Devuelve la cantidad de películas por plataforma con un puntaje mayor al especificado en determinado año.

URL

bash

/movies/score_count

Método

sql

GET

Parámetros URL

    platform: plataforma de las películas a buscar.
    scored: puntaje mínimo para incluir una película.
    year: año de estreno de las películas.

Respuesta

go

{
    "platform": <string>,
    "count": <int>
}

# Cantidad de películas por plataforma

Devuelve la cantidad de películas por plataforma.

URL

bash

/movies/count_platform

Método

sql

GET

Parámetros URL

    platform (opcional): plataforma de las películas a buscar.

Respuesta

go

{
    "platform": <string>,
    "count": <int>
}

Actor que más se repite según plataforma y año

Devuelve el actor que más se repite en las películas de una plataforma y año específicos.

URL

bash

/movies/top_actor

Método

sql

GET

Parámetros URL

    platform: plataforma de las películas a buscar.
    year: año de estreno de las películas.

Respuesta

go

{
    "platform": <string>,
    "year": <int>,
    "actor": <string>,
    "count": <int>
}
