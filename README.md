# SQL NA PRÁTICA

-- SELECIONANDO O BANCO DE DADOS A SER USADO

use curso2;

-- CRIANDO UMA TABELA "USERS"

			CREATE TABLE users( 
				user_id INT NOT NULL AUTO_INCREMENT,
				first_name VARCHAR(100),
				last_name VARCHAR(100),
				sallary INT,
				dob DATE,
				PRIMARY KEY (user_id));
            
            
-- EXCLUINDO TABELA

			DROP TABLE users;
            
-- INSERINDO DADOS NA TABELA

			INSERT INTO users(first_name,last_name, sallary, dob) 
            VALUE ("Carlos Abraão", "Mendonça Chaves", 500, "1984-08-22");
            
            INSERT INTO users(first_name,last_name, sallary, dob)  
            VALUE ("Ricardo Oliveira", "Santos Chaves", 1000, "1974-07-22");
            
-- INSERINDO MAIS DE UM REGISTRO AO MESMO TEMPO
                        
             INSERT INTO users(first_name,last_name, sallary, dob)  
			 VALUE ("Alexandro Santos", "Moreira Assis", 1500, "1978-07-12"),
				   ("Suzane Luana", "Melo Santos", 500, "1979-07-12");
            
-- SELECIONANDO TABELA USERS

			SELECT * 
			FROM users;


-- ATUALIZANDO DADOS DA TABELA
-- POSSO ATUALIZAR MAIS DE UMA COLUNA, QUE NEM NO CASO COLUNA "SALLARY E "LAST_NAME"

			UPDATE users 
			SET last_name = "Lobato Lima", sallary = 10000
			WHERE  user_id = 4;

-- DELETANDO DADOS DA TABELA

			DELETE FROM users
            WHERE user_id = 3;
            

