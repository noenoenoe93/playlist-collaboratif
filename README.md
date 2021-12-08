# playlist-collaboratif

CREATE DATABASE PlaylistCollaboratif;

CREATE TABLE utilisateurs (
user_id user PRIMARY KEY NOT NULL AUTO_INCREMENT,
votes int NOT NULL,
identifiant varchar(20) NOT NULL,
SuperVote int,
role_invite varchar(10) NOT NULL,
role_organisateur varchar(10) NOT NULL
);

CREATE TABLE playlist (
musique_id musique PRIMARY KEY NOT NULL AUTO_INCREMENT,
votes int NOT NULL,
duree minute NOT NULL,
style_musique varchar(15) NOT NULL,
titre varchar(20) NOT NULL
);

CREATE TABLE artist (
nom_id nom PRIMARY KEY NOT NULL
);

CREATE TABLE album (
id_album album PRIMARY KEY NOT NULL,
FOREIGN KEY(id_album) REFERENCES artist(nom_id)
);
