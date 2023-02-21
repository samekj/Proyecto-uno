# Documentación API
Descripción

Esta API provee acceso a información sobre películas y series de diferentes plataformas: amazon, disney, netflix y hulu. Los datos provienen de un conjunto de datasets ya limpios y transformados.

## - Consultas disponibles

### Documentación

Entra a la documentación proporcionada por FastAPI

URL

    https://proyecto_1-2-n4048090.deta.app/docs

### Película con mayor duración

Devuelve la película con mayor duración de acuerdo a los filtros opcionales especificados.

URL
    https://proyecto_1-2-n4048090.deta.app/get_max_duration/{year}/{platform}/{duration_type}

Parámetros URL

- year: año de estreno de la película.
- platform: plataforma en la que se encuentra la película: amazon, disney, netflix, hulu.
- duration_type: tipo de duración de la película. Valores posibles: "min" (minutos) o "season" (temporadas).

### Cantidad de películas por plataforma con un puntaje mayor a XX en determinado año

Devuelve la cantidad de películas por plataforma con un puntaje mayor al especificado en determinado año.

URL
    https://proyecto_1-2-n4048090.deta.app/score_count/{platform}/{scored}/{year}

Parámetros URL

- platform: plataforma de las películas a buscar: amazon, disney, netflix, hulu.
- scored: puntaje mínimo para incluir una película.
- year: año de estreno de las películas.

### Cantidad de películas por plataforma

Devuelve la cantidad de películas por plataforma.

URL

    https://proyecto_1-2-n4048090.deta.app/get_count_platform/{platform}

Parámetros URL

- platform: plataforma de las películas a buscar: amazon, disney, netflix, hulu.


### Actor que más se repite según plataforma y año

Devuelve el actor que más se repite en las películas de una plataforma y año específicos.

URL

    https://proyecto_1-2-n4048090.deta.app/get_actor/{platform}/{year}

Parámetros URL

- platform: plataforma de las películas a buscar: amazon, disney, netflix, hulu.

- year: año de estreno de las películas.