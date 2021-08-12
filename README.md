# Project-TPS1-106
My project final about an online store
create table usuarios (
    id_usuario INTEGER(11)  NOT NULL  AUTO_INCREMENT PRIMARY KEY,
    nombre     VARCHAR(45)  NOT NULL,
    apellido   VARCHAR(45)  NOT NULL,
    fecha_nmto DATE(60)     NOT NULL,
    numero_cel INTEGER(11)  NOT NULL,
    correo     VARCHAR(60)  NOT NULL,
    genero     VARCHAR(15)  NOT NULL,
    pasword    VARCHAR(200) NOT NULL,
    id_roles   INTEGER(11)  NOT NULL,
    id_pais    INTEGER(11)  NOT NULL,
    id_ciudad  INTEGER(11)  NOT NULL,
    CONSTRAINT usuarios_roles_fk FOREIGN KEY id_roles references roles(id_roles),
    CONSTRAINT usuarios_pais_fk FOREIGN KEY id_pais references pais(id_pais),
    CONSTRAINT usuarios_ciudad_fk FOREIGN KEY id_ciudad references ciudad(id_ciudad),
);
