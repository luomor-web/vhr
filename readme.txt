drop user 'vhr'@'127.0.0.1';
create database vhr default character set utf8mb4 collate utf8mb4_unicode_ci;
use vhr;
create user 'vhr'@'127.0.0.1' identified by '123465';
grant all privileges on vhr.* to 'vhr'@'127.0.0.1';
flush privileges;


create user 'vhr'@'localhost' identified by '123465';
grant all privileges on vhr.* to 'vhr'@'localhost';
flush privileges;
