# Começando em Elixir

Elixir é uma linguagem de programação multiparadigma, com suporte a programação funcional, concorrente,  tem como objetivo ser uma linguagem de programação de propósito geral
que roda em uma maquina virtual do Erlang(BEAM). Ela constrói em cima do Erlang para fornecer um sistema distribuído, tolerante a falhas, real-time, non-stop e ela também suporta metaprogramação com suporte a macros e poliformismo via protocolos.


## Instalando o Elixir 


#### Mac
Instale o homebrew ele é um gerenciador de pacotes para o Mac.
Abra seu terminal e rode o seguinte comando:

```ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```

Atualize seu brew para a última versão:

```brew update```

E por último rode:

```brew install elixir```

#### Ubuntu
Adicione o pacote do Erlang:
```wget https://packages.erlang-solutions.com/erlang-solutions_1.0_all.deb && sudo dpkg -i erlang-solutions_1.0_all.deb```

Atualize os pacotes de sua máquina:

```sudo apt-get update```

Rode:

```sudo apt-get install elixir```


#### Windows
[Baixe o instalador neste link e clique em next, next, ..., finish.](https://s3.amazonaws.com/s3.hex.pm/elixir-websetup.exe)

#### Outras distribuições
Confira no [site da lang.](http://elixir-lang.org/install.html)

## Primeiros passos

Vamos para nossa linha de comando em nosso terminal ou shell e digite ```iex``` e será exibida a seguinte informação em sua tela

```
Interactive Elixir (1.1.1) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)>
``` 

Agora estamos dentro do interpretador do Elixir

Podemos sair do iex pressionando Ctrl+C e selecionando a opção 'a' para interromper o seu funcionamento.

Uma das melhores maneiras de começar é usando nosso terminal como uma calculadora. Então podemos pedir para realizarmos algumas opereções aritméticas:


	Interactive Elixir (1.1.1) - press Ctrl+C to exit (type h() ENTER for help)
	iex(1)> 10+10
	20
	iex(2)> 9*9
	81
	iex(3)> 5+9
	14
	iex(4)> 100/5
	20.0
	iex(5)> 10-3
	7
	iex(6)> 2*(4+4)
	16

### Tipos básicos de dados
Temos o suporte a **boolean**, **integer**, **float**, **atom**, **symbol**, **strings**, **listas** e **tuple**.

#### Boolean
São valores considerados como ``true`` e ``false`` <em>verdadeiro ou falso</em> podendo ser respresentados da seguinte forma em nosso iex: 

	iex(1)> true
	true
	iex(2)> false
	false
	iex(3)> true == false
	false
	iex(4)> false == false 
	true
	
No exemplo acima utilizamos o operador de compração ``==`` que verifica se ambos valores correspondem retornando true se forem igual ou false se forem diferentes. Iremos ver operadores de comparação mais a frente.

### Integer
São números inteiros em Erlang / Elixir são limitadas apenas pela memória disponível no sistema, então não há praticamente nenhum limite de quão grande eles podem ser.

	iex(1)> 100
	100
	iex(2)> 200
	200
Também podemos colocar o caracter _ para facilitar a leitura de números grandes

	iex(3)> 1_000
	1000
	iex(4)> 1_234_456
	1234456

#### Strings
São uma cadeia de caracteres dentro de aspas duplas codificados em UTF-8

	iex(1)> "Olá mundo"
	"Olá mundo"
	iex(2)> "Eu sou uma cadeira de caracteres limitados em aspas duplas !"
	"Eu sou uma cadeira de caracteres limitados em aspas duplas !"

As strings podem ser escapadas utilizando \n :

	iex(3)> "Ola
	...(3)> mundo"
	"Ola\nmundo"
	iex(4)> "Ola\nmundo"
	"Ola\nmundo"

Podem ser exibidas utilizando a função ``IO.puts`` do módulo IO:

	iex(5)> IO.puts "Ola\nmundo"
	Ola
	mundo
	:ok
	
Conseguimos utilizar algumas funções do modulo String do Elixir

	iex(1)> String.length("Ola mundo")
	9
	iex(2)> String.upcase("ola mundo")
	"OLA MUNDO"
	iex(3)> String.downcase("OLA MunDO")
	"ola mundo"
	iex(4)> String.reverse("Ola Mundo")
	"odnuM alO"
	iex(5)> String.contains? "O nome dele é José", "José"
	true
	iex(6)> String.contains? "O nome dele é José Valim", ["José", "Valim"]
	true
	iex(7)> String.contains? "O nome dele é José Valim", ["Pedro", "Valim"]
	true
	iex(8)> String.duplicate("Ola ", 10)
	"Ola Ola Ola Ola Ola Ola Ola Ola Ola Ola "
	iex(9)> String.replace("a,b,c", ",", "-")
	"a-b-c"

#### Floats

São números com ponto flutuante.<br/>
O senhor tem R$25,50 ? basta colocar um ponto "."

	iex(1)> 100.20
	100.2  
	iex(2)> 25.50
	25.5
	iex(3)> 29.923
	29.923



