# ENTRETERIMENTO-QUESTOES


01. Crie um script SQL que mostre todas as colunas, onde liste apenas o TIPO "série" da tabela de ENTRETERIMENTO;
    RESPOSTA:  SELECT `NOME`,`TIPO` FROM `ENTRETERIMENTO` WHERE TIPO = "SÉRIE"  
2. Crie um script SQL que mostre todas as colunas, onde liste apenas o TIPO "série" da tabela de ENTRETERIMENTO, mas em ordem alfabética de NOMES(de A até Z);
    RESPOSTA:  SELECT `NOME`,`TIPO` FROM `ENTRETERIMENTO` WHERE TIPO = "SÉRIE" ORDER BY NOME ASC 
3. Crie um script SQL que mostre apenas o TIPO "série" da tabela de ENTRETERIMENTO, porém de forma alfabética INVERTIDA (de Z para A);
    RESPOSTA: SELECT `NOME`,`TIPO` FROM `ENTRETERIMENTO` WHERE TIPO = "SÉRIE" ORDER BY NOME DESC 
4. Crie um script SQL que mostre apenas o TIPO "FILME" da tabela de ENTRETERIMENTO;
    RESPOSTA: SELECT `NOME`,`TIPO` FROM `ENTRETERIMENTO` WHERE TIPO = "FILME" 
5. Liste os filmes que foram produzidos antes dos anos 2000;
    RESPOSTA: SELECT `ID`, `NOME`, `TIPO`, `ANO_LANCAMENTO` FROM `ENTRETERIMENTO` WHERE TIPO = "FILME" AND ANO_LANCAMENTO < 2000 
6. Liste as séries que foram produzidas após o ano 2015;
    RESPOSTA: SELECT `ID`, `NOME`, `TIPO`, `ANO_LANCAMENTO` FROM `ENTRETERIMENTO` WHERE TIPO = "SÉRIES" AND ANO_LANCAMENTO > 2015
7. Liste os filmes de ação(e suas variações, como por exemplo: Ação/Drama);
    RESPOSTA:  SELECT NOME, GENERO FROM ENTRETERIMENTO WHERE genero LIKE "%Ação%" 
8. Mostre os filmes que tem duração superior a 2horas;
    RESPOSTA: SELECT `ID`, `NOME`, `TIPO`, `DURACAO_MINUTOS` FROM `ENTRETERIMENTO` WHERE TIPO = "FILME" AND DURACAO_MINUTOS >120 
9. Liste as séries que foram produzidas entre os anos de 2012 até 2016, em ordem de ano e em seguida pelo nome da série;
    RESPOSTA: SELECT `NOME`, `TIPO`, `ANO_LANCAMENTO` FROM `ENTRETERIMENTO` WHERE TIPO = "SÉRIE" AND ANO_LANCAMENTO BETWEEN 2012 AND 2016 ORDER BY ANO_LANCAMENTO ASC, NOME ASC;
10. Mostre os filmes que o ator Brad Pitt trabalhou por onde do filme mais antigo para o mais novo;
    RESPOSTA: SELECT * FROM `ENTRETERIMENTO` WHERE TIPO = 'FILME' AND ATOR_PRINCIPAL = 'Brad Pitt ' ORDER BY ANO_LANCAMENTO ASC 
11. Liste apenas o campo NOME, DIRETOR, ATOR PRINCIAL dos itens que são do gênero "crime" (e suas variações) e o ator seja "John Travolta";
    RESPOSTA: SELECT NOME, GENERO, DIRETOR, ATOR_PRINCIPAL FROM ENTRETERIMENTO WHERE GENERO LIKE "%Crime%" AND ATOR_PRINCIPAL= "John Travolta" 
12. Liste os itens que a duração seja superior a 2 horas e que o ator NÃO seja Christian Bale ou Tim Robbins
    RESPOSTA: SELECT NOME, DURACAO_MINUTOS, ATOR_PRINCIPAL FROM ENTRETERIMENTO WHERE DURACAO_MINUTOS > 120 AND ATOR_PRINCIPAL NOT IN ('Christian Bale', 'Tim Robbins') 
13. Liste os itens que NÃO seja de Comédia ou drama;
    RESPOSTA: SELECT NOME, GENERO FROM ENTRETERIMENTO WHERE GENERO NOT IN ('Comédia', 'Drama') 
14. Liste todos os itens que foram criados, que não seja dos anos 2000, 2001 ou 2002;
    RESPOSTA: SELECT NOME, ANO_LANCAMENTO FROM ENTRETERIMENTO WHERE ANO_LANCAMENTO NOT IN (2000, 2001, 2002) 
15. Liste os itens que tiveram como ator Wagner Moura ou Leonardo DiCaprio ou Keanu Reeves
    RESPOSTA: SELECT NOME, ATOR_PRINCIPAL FROM ENTRETERIMENTO WHERE ATOR_PRINCIPAL IN ('Wagner Moura ', 'Leonardo DiCaprio', 'Keanu Reeves') 
