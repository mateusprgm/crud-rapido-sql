/* 	
	Olá, vamos aprender criar um banco SQL sem muito encher o saco.

	Palavras Chave -> Palavras/nomes reservados pelo sistema.

	Primeiro, instale o MySql em sua máquina.
	Segundo, instale o XAMPP em sua máquina.
	Terceiro, inicie o XAMPP.
	Quarto, Abra o MySql em sua máquina.

	Para criar um banco de dados é necessário rodar o seguinte comando:
/*

Create Schema NomeDoMeuBanco; /* pronto, banco criado. */

Create Table MinhaTabela(
	id int primary key not null auto_increment, /* o atributo 'auto_increment' vai incrementar o ID de forma automatica a cada registro que for sendo adicionado.*/
	nome varchar(100)
);

/* 
	Desta forma, criamos nossa primeira table ou tabela...
	Agora vamos para o CRUD, significado desta sigla???
	Este: C de Create(Criar), R de Read(Ler), U de Update(Atualizar) e D de Delete(Excluir).

	Tudo isso se aplicaria em em registros do nosso banco, como buscar, criar, atualizar ou deletar um registro.

	Primeiro, como criar um registro pro nosso banco recém nascido:
/* 
	1.CREATE -> Insert ->  comando responsável por inserir registros.
	
	linha 1: Indica que que você está inserindo um dado na table a 'MinhaTabela' entre parentes mostra quais campos você quer preencher na inserção, nesse caso o 'nome'.
	Linha 2: Indica quais valores está sendo armazenado no devido atributo declarado anteriormente, no caso o 'nome' receberá o valor "nomeDeFulano"
	Desta forma constitui o seguinte código: 
*/	
	/*linha 1*/insert into MinhaTabela(nome) 
	/*linha 2*/values("NomeDeFulano");
/*
	Pronto, desta forma finalizamos o Create.
	agora vamos para o Read
*/
	
/* 	
	2.READ -> Select -> comando responsável por buscar registros.

	O asterisco representado por '*' significa all(tudo) ou seja, se ele é declarado perante o select, indica que eu estou buscando todas as colunas da tal tabela, informada depois do 'from' que nesse caso seria 'MinhaTabela'.

	Logo temos: 
*/

	select * from MinhaTabela;
/*
	3.UPDATE -> Update -> comando responsável por atualizar registros.

	Após a palavra chave 'update' é declarado o nome da tabela a qual você quer alterar algum dado, após a palavra chave 'set' deverá ser colocado o nome do atributo a ser atualizado e respectivamente seu valor, não esquecendo da cláusula 'where' que dirá QUAL REGISTRO estará sendo ALTERADO.

	No exemplo abaixo estaremos alterando o atributo 'nome' da tabela MinhaTabela onde o 'id' for igual a '1'.
*/

	update MinhaTabela set nome = "NomeDeSicrano" where id = 1;
/*
	4.DELETE -> Delete -> comando responsável por excluir registros.

	Após a palavra chave 'from' virá o nome da tabela a qual você estará deletando 1 registro ou mais de acordo com a condição a ser colocada na cláusula 'where'.
	E não menos importante o 'id' que indicará qual registro será deletado.

	Abaixo temos o seguinte exemplo:
	Exclua da tabela 'MinhaTabela' o registro de id igual à 1. 
*/

	delete from MinhaTabela where id = 1;

/*

	Pronto, criamos um CRUD completo.

*/