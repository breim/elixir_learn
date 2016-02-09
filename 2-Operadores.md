# Operadores

Operadores de acordo com o Wikipedia
>Operadores são símbolos que representam atribuições, cálculos e ordem dos dados. As operações seguem uma ordem de prioridades, ou seja, alguns cálculos (ou outros) são processados antes de outros


## Operadores aritméticos

Operador  | Função
------------- | -------------
+ | Adição
- | Subtração
* | Multiplicação
/ | Divisão


Exemplos 

	iex(1)> num1 = 20
	20
	iex(2)> num2 = 30
	30
	iex(3)> num1+num2
	50
	iex(4)> num1-num2
	-10
	iex(5)> num1 = 5 
	5
	iex(6)> num2 = 20
	20
	iex(7)> num2/num1
	4.0
	iex(8)> (num2/num1)*2
	8.0

> Em elixir o operador '/' sempre retorna o valor em float.	
	
Também podemos utilizar algumas **funções** prontas

Para receber a divisão de números inteiros

	iex(9)> div(10, 2)
	5

Sabermos o resto da divisão

	iex(10)> rem(10, 3)
	1
	
## Operadores de comparação

Operador  | Função
------------- | -------------
**==** | Checa se o valor corresponde ao mesmo valor comparado(verifica se é idêntico), retornando true ou false
**!=** | Checa se os valores são diferentes, retornando true ou false
**>** | Verifica se o valor é maior que (se o valor da esquerda é maior que o da direita), retornando true ou false
**<** | Verifica se o valor é menor que (se o valor da esquerda é menor que o da direita), retornando true ou false
**>=** | Verifica se o valor é menor que (se o valor da esquerda é menor que o da direita), retornando true ou false
**<=** | Verifica se o valor é menor ou igual, retornando true ou false
**<=>** | Operador de combinação. Retorna 0 se o primeiro operador for igual o segundo, 1 se o primeiro operador for maior que o segundo e -1 se o primeiro operador for menor que o segundo
**===** | Verifica se o objeto tem o mesmo valor e tipo de dados, retornando true ou false

Exemplos 

	iex(10)> true and true
	true
	iex(11)> "texto" == "texto"
	true
	iex(12)> 10 != 10
	false
	iex(13)> 5 > 2
	true
	iex(14)> 5 < 10
	true
	iex(15)> 5 >= 5
	true
	iex(16)> 5 <= 6
	true
	iex(17)> 5 === 5
	true
	iex(18)> 5 === "5"
	false


	
## Operadores lógicos

Operador  | Função
------------- | -------------
**AND** | podemos ler como "E" se os dois operadores retornarem true então a condição é verdadeira
**OR** | podemos ler como OU Se qualquer um dos dois operandos são diferentes de zero, então a condição se torna verdade
**&&** | mesma coisa do operador AND
**`||`**  | mesma coisa do Operador OR
**!**  | Comprador negativo Ex: !(10 == 11) retorna true
**not** | Mesma coisa do ponto de esclamação

Exemplos

	iex(1)> false and true
	false
	iex(2)> false or true
	true
	iex(3)> true and true
	true
	iex(4)> true && true
	true
	iex(5)> true || false
	true
	iex(6)> true || true 
	true
	iex(7)> !(10 == 10)
	false
	iex(8)> not(10==10)
	false
