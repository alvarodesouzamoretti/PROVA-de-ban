create database escola;
use escola;
create table aluno(
id_aluno int not null auto_increment,
nome varchar(100),
sexo char(1),
cpf varchar(14),
tel_cel varchar (20),
tel_res varchar (20),
email varchar (200),
dt_nascimento varchar (10),
senha varchar(200),
confirmar_senha varchar (100),
primary key (id_aluno)
);

desc aluno;

create table livro(
id_livro int not null auto_increment,
titulo varchar (100),
genero varchar (30),
ano varchar (30),
isbn varchar (13),
primary key (id_livro)
);

desc livro ;

create table emprestimos(
id_emprestimo int not null auto_increment,
cod_aluno int,
cod_livro int, 
data_emprestimo date,
data_devolucao date,
estatus varchar (10),

primary key (id_emprestimo)
);

desc emprestimo;


create table aluno_e_emprestimo(
id_aluno_e_emprestimo int not null auto_increment,
cod_aluno int,
cod_emprestimo int,


primary key (id_aluno_e_emprestimo)
);


alter table emprestimos add foreign 
key (cod_aluno) references
aluno(id_aluno)




