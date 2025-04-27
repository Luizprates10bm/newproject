CREATE DATABASE faculdade_db
USE faculdade_db

CREATE TABLE tbl_aluno (
  id_aluno INT AUTO_INCREMENT PRIMARY KEY,
  nome_aluno VARCHAR(100) NOT NULL,
  data_nascimento DATE NOT NULL,
  email VARCHAR(100)
);


CREATE TABLE tbl_curso (
  id_curso INT AUTO_INCREMENT PRIMARY KEY,
  nome_curso VARCHAR(100) NOT NULL
);


CREATE TABLE tbl_Disciplina (
  id_disciplina INT AUTO_INCREMENT PRIMARY KEY,
  nome_disciplina VARCHAR(100) NOT NULL,
  carga_horaria INT NOT NULL,
  id_curso INT,
  FOREIGN KEY (id_curso) REFERENCES tbl_curso(id_curso)
);



CREATE TABLE tbl_professor (
  id_professor INT AUTO_INCREMENT PRIMARY KEY,
  nome_professor VARCHAR(100) NOT NULL,
  email VARCHAR(100)
);

CREATE TABLE tbl_turma (
  id_turma INT AUTO_INCREMENT PRIMARY KEY,
  id_disciplina INT,
  id_professor INT,
  id_curso INT,
  semestre VARCHAR(10) NOT NULL,
  FOREIGN KEY (id_disciplina) REFERENCES tbl_disciplina(id_disciplina),
  FOREIGN KEY (id_professor) REFERENCES tbl_professor(id_professor),
  FOREIGN KEY (id_curso) REFERENCES tbl_curso(id_curso)
);



CREATE TABLE tbl_matricula (
  id_matricula INT AUTO_INCREMENT PRIMARY KEY,
  id_aluno INT,
  id_turma INT,
  nota DECIMAL(4,2) NOT NULL,
  FOREIGN KEY (id_aluno) REFERENCES tbl_aluno(id_aluno),
  FOREIGN KEY (id_turma) REFERENCES tbl_turma(id_turma),
  UNIQUE (id_aluno, id_turma)
);


INSERT INTO tbl_aluno (nome_aluno, data_nascimento, email) VALUES
('Bernardo Silva', '2000-05-10', 'bernardo.silva@email.com'),
('João Souza', '1999-08-22', 'joao.souza@email.com'),
('Maria Costa', '2001-01-15', 'maria.costa@email.com'),
('Isadora Augusto', '1999-07-19', 'isadora.aug@email.com'),
('Matheus Valente', '1998-08-16', 'matheus.valen@email.com'),
('Thiago castro', '1994-10-23', 'thiago.castro@email.com');


INSERT INTO tbl_curso (nome_curso) VALUES
('Análise e Desenvolvimento de Sistemas'),
('Engenharia Civil'),
('Administração');


INSERT INTO tbl_disciplina (nome_disciplina, carga_horaria, id_curso) VALUES
('Banco de Dados', 60, 1),
('Cálculo', 80, 2),
('Gestão de Pessoas', 60, 3);



INSERT INTO tbl_matricula (id_aluno, id_turma, nota) VALUES
(1, 1, 8.5),
(2, 2, 7.0),
(3, 3, 9.2),
(4, 1, 7.5),
(5, 2, 9.0),
(6, 3, 7.8);


INSERT INTO tbl_professor (nome_professor, email) VALUES
('Matheus Henrique', 'matheus.henrique@email.com'),
('Raquel Lima', 'raquel.lima@email.com'),
('Sérgio Pires', 'sergio.pires@email.com');



INSERT INTO tbl_turma (id_disciplina, id_professor, id_curso, semestre) VALUES
(1, 1, 1, '2025.1'),
(2, 2, 2, '2025.1'),
(3, 3, 3, '2025.1');