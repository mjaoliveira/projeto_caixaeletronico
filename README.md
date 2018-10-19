# projeto_caixaeletronico

mysql

create database projeto_caixaeletronico
default character set utf8
default collate utf8_general_ci;

create table contas(
id int auto_increment primary key not null,
titular varchar(100)not null,
agencia int not null,
conta int not null,
senha varchar(32),
saldo float
)default charset = utf8;

create table historico(
id int auto_increment primary key not null,
id_conta int,
tipo tinyint(1),
valor float,
data_operacao datetime
)default charset = utf8;

insert into contas
(titular, agencia, conta, senha, saldo)
values
('Mariana Santos',123,322,md5("12345"),0);

select * from contas;

update contas SET senha = md5("12345") where id = 2;
update contas SET titular = 'Maria Do Carmo' where id = 2;
update contas SET conta = 333 where id = 2;