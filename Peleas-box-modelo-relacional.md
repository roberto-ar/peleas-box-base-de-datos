### ENTIDADES ###

- **Pelea** PIBOTE
    - pelea_id **(PK)**
    - arena **(FK)**
    - Fecha
    - Hora
    - peleador_1_id **(FK)**
    - peleador_2_id **(FK)**
    - division **(FK)**
    - organizacion **(FK)**
    - resultado **(FK)**
    - pais **(FK)**

- **Peleador** DATE
    - peleador_id **(PK)**
    - nombre
    - apellido
    - apodo
    - victorias
    - derrotas
    - empates
    - altura

- **Resultado** DATE
    - resultado_id **(PK)**
    - pelea **(FK)**
    - tipo_resultado **(FK)**

- **Tipo_resultado** CATALOGO
    - tipo_resultado_id **(PK)**
    - tipo_resultado

- **victoria** SUBENTIDAD
    - victoria_id **(PK)**
    - resultado **(FK)**
    - peleador_ganador **(FK)**
    - tipo

- **Detalle_KO** SUBENTIDAD
    - detalle_ko_id **(PK)**
    - victoria **(FK)**
    - round 

- **Detalle_desicion** SUBENTIDAD
    - detalle_desicion_id **(PK)**
    - victoria **(FK)**
    - desicion_unanime 

- **Divisiones** CATOLOGO
    - id_division **(PK)**
    - nombre
    - peso minimo
    - peso maximo 

- **Organizaciones** CATALOGO
    - id_organizacion **(PK)**
    - nombre

- **Campeones** PIBOTE CATALOGO
    - peleador **(FK)**
    - organizacion **(FK)**
    - division **(FK)**

- **Arenas** CATALOGO
    - arena_id **(PK)**
    - pais **(FK)**
    - lugar
    - nombre_arena

- **pais** CATALOGO
    - pais_id
    - nombre


## RELACIONES ##
- Una pelea pertenece a una arena (1 a N)
- Una pelea tiene un primer peleador (1 a 1)
- Una pelea tiene un segundo peleador (1 a 1)
- Una pelea pertenece a una division (1 a N)
- Una pelea pertenece a una organizacion (1 a N)
- Una pelea tiene un resultado (1 a 1)

- Un resultado tiene un tipo de resultado (victoria o empate) (1 a 1)
- Una victoria tiene un tipo de victoria (KO o desicion) (1 a 1)

- Una campeon pertenece a una division (1 a N)
- Un campeon pertenece a una organizacion (1 A N)
- Un campeon pertenece a un pais (1 A N)


- Una arena pertenece a un pais (1 A N)




