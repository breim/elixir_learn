# Estruturas de Controle

Estruturas de controle de acordo com o Wikipedia
>Em ciência da computação, estrutura de controle (ou fluxo de controle) refere-se à ordem em que instruções, expressões e chamadas de função são executadas ou avaliadas em programas de computador sob programação imperativa ou funcional.


## IF e UNLESS
Interprete o IF em português como se fosse "SE" e o ELSE como se fosse "SE NÃO" ou seja se a primeira condição for verdadeira ele executa o que está dentro do trecho do IF, caso não tenha nenhuma condição que satisfaça ele roda o que está dentro do ELSE.

Unless diferente do IF que espera uma condição verdadeira ele espera uma condição falsa para entrar na sua estrutura de controle.

> Lembre-se toda estrutura de controle termina com "end"

Exemplo:

	verdadeiro = true
	
	if verdadeiro do
		IO.puts "Condição verdadeira"
	else
		IO.puts "Condição falsa"
	end

Saída: **Condição verdadeira**

Podemos fazer comparações lógicas como o exemplo abaixo.

	a = 10; b = 20
	
	if a == b do
		IO.puts "Os números são iguais"
	else
		IO.puts "Os números são diferentes"
	end

Saída: **Os números são diferentes**


#### Unless
Exemplo do **unless**:
	
	value = true
	
	unless value do
		IO.puts "Valor é falso"
	else
		IO.puts "Valor é verdadeiro"
	end
	
Saída: **Valor é verdadeiro**



## COND

Elixir não tem a condição **else if** nos casos que precisamos checar mais de uma condição podemos utilizar a estrutura de controle **cond**.
	
	cond do
		10 == a ->
			IO.puts "10 é igual A"
		20 == b ->
			IO.puts "20 é igual B"
	end

Saída: **10 é igual A**

> COND irá executar a primeira condição que for verdadeira.

Veja outro exemplo quando a condição for verdadeira atribuímos um novo valor a variável **b** :

	a = 10; b = 20
	
	cond do
		10 == a ->
			b = 1
		20 == b ->
			IO.puts "20 é igual B"
	end
	
	IO.puts a+b

Saída: **11**

Caso nenhuma condição seja atingida um erro irá acontecer e interromper a execução desse bloco de código, para evitar isso podemos adicionar uma condição final equivalente a true (podendo ser interpretada como o ELSE).

Exemplo:

	cond do
		10+10 == 50 ->
			IO.puts "10+10 são 50"
		10 != 10 ->
			IO.puts "os números são diferentes"
		true ->
			IO.puts "Nenhuma das condições anteriores é verdadeira"
	end
	
Saída: **Nenhuma das condições anteriores é verdadeira**
