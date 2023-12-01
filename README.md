Atividade em que se faz pesquisas dentro de um bando de dados SQL usando do CRUD - CREADTE, READ, UPDATE, DELET;

1- Quantas vezes Natalie Portman foi indicada ao Oscar?

r: 1 filme select * from filmes where nome_do_indicado like '%Natalie Portman%' and vencedor = 'Sim’

2- Quantos Oscars Natalie Portman ganhou?

r: Não ganhou select * from filmes where nome_do_indicado like '%Amy Adams%' and vencedor = 'Sim’

3- Amy Adams já ganhou algum Oscar?

r: 2011 e 2020 select ano_cerimonia from filmes where nome_filme like '%Toy Story%' and vencedor = 'Sim’

4- A série de filmes Toy Story ganhou um Oscar em quais anos?

r: A partir de 1977 select ano_cerimonia from filmes where categoria = 'actress’

5- A partir de que ano que a categoria "Actress" deixa de existir?

r: 1976 select ano_filmagem from filmes where categoria = 'actress’

6- O primeiro Oscar para melhor Atriz foi para quem? Em que ano?

r: Janet Gaynor no ano de 1927 select ano_filmagem, vencedor, nome_do_indicado from filmes where categoria = 'actress' order by ano_filmagem

7- Na coluna/campo "Vencedor", altere todos os valores com "Sim" para 1 e todos os valores "Não" para 0.

r: update filmes set vencedor = '1' where vencedor = 'Sim' update filmes set vencedor = '0' where vencedor = 'Não'

8- Em qual edição do Oscar "Crash" ganhou o prêmio principal?

r: Edição 78
select * from filmes where nome_filme like '%Crash%' and categoria like '%best picture%' and vencedor like '%Sim%’

9- Bom... dê um Oscar para um filme que merece muito, mas não ganhou.

r: update filmes set vencedor = '1' where nome_filme ='Joker' and categoria = 'Best Picture';

10- O filme Central do Brasil aparece no Oscar?

r: Não select * from filmes where nome_filme like '%Central do Brasil%';

11- Inclua no banco 3 filmes que nunca foram nem nomeados ao Oscar, mas que merecem ser.

r: insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('2016', '2017', '89', ' Best Picture', 'Michael Gracey', 'O Rei do Show', '1');

insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('2016', '2017', '89', 'Best Picture', 'Stephen Chbosky', 'Extraordinário', '0');


insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('2017', '2018', '90', 'Best Picture', 'George Tillman Jr.', 'The Hate U Give', '1');
12- Pensando no ano em que você nasceu: Qual foi o Oscar de melhor filme, Melhor Atriz e Melhor Diretor?

r: Melhor Filme: Gladiator select * from filmes where ano_cerimonia = '2001' and categoria = 'Best Picture'and vencedor = '1';

Melhor Atriz: Julia Roberts
  select * from filmes where ano_cerimonia = '2001' and vencedor ='1' and categoria = 'ACTRESS IN A LEADING ROLE';

Melhor Diretor: Steven Soderbergh
  select * from filmes where ano_cerimonia = '2001' and vencedor ='1' and categoria = 'directing';
13- Agora procure 7 atrizes que não sejam americanas, europeias ou brasileiras. Vamos cadastrá-los no nosso banco com o prêmio que você quiser.

insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('2010', '2011', '83', 'ACTRESS', 'Viola Davis', 'Histórias Cruzadas', '1');

insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('1953', '1954', '26', 'ACTRESS', 'Dorothy Dandridge', 'Carmen Jones', '1');

insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('2015', '2016', '88', 'Actress', 'YU-MI JUNG', 'Invasão Zumbi', '1');

insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('2019', '2020', '92', 'ACTRESS', 'Park Shin-hye', '#Alive', '1');

insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('2018', '2019', '91', 'ACTRESS', 'Cho Yeo-jeong', 'Parasita', '1');

insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('2021', '2022', '94', 'ACTRESS', 'Kanna Hashimoto', 'Re/Member', '1');

insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('2021', '2022', '94', 'ACTRESS', 'Park Se Hyun', 'Vingança pelo Passado', '0');

insert into filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES ('2009', '2010', '82', 'actress', 'Noriko Aoyama', 'Atividade Paranormal em Tóquio', '1');

14- Agora vamos falar da sua vida. Me diga o nome de uma pessoa que você admira e o que ela fez na sua vida. Agora me diz: Quê prêmio essa pessoa merece?# oscar_vai_para
minha mãe e meu pai, quanha o premio de esforço 
