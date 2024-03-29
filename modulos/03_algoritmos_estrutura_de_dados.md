# 03 - Algoritmos e Estrutura de Dados

Nesse módulo iremos abordar dois estudos em conjunto, o da semana passada e o dessa. O estudo desse módulo é denso, os nossos capítulos de agora em diante vão depender muito da sua dedicação aos estudos.

## Objetivos
Fixar o entendimento de estruturas basicas de dados, tipagens de dados e funções.

## Tipos de dados

Cada dado em programação deve possuir um tipo. Tipos são formas de identificar como um valor se identifica e seus comportamentos.

### Number

O tipo Number é a forma de se identificar números.

```ruby
my_num = 10
```

Números podem ser usados em operações matemáticas de qualquer tipo:

```ruby
soma = 10 + 10 # 20

subtracao = 10 - 5 # 5

divisão = 10 / 2 # 5

resto = 10 % 3 # 1

multiplicacao = 10 * 3 # 30
```

### String

O tipo String é a forma de se identificar textos.
<br>Strings podem ser identificadas com aspas (`"` ou `'`)

```ruby
texto = "Meu texto"
outro_texto = 'Meu outro texto'
```

### Boolean

O tipo Boolean é uma forma de se identificar apenas `false` ou `true`.
<br>Comparações também podem ser identificadas como booleans.

```ruby
boolean = true
outro_boolean = 10 + 10 == 19 # false
```

### Array

O tipo Array é uma forma de se identificar uma lista de valores que podem ser de qualquer um dos tipos apresentados aqui.
<br>Para declarar um array, usamos colchetes e separamos cada item com vírgulas.
<br>Para acessarmos um valor do array, precisamos especificar a posição do elemento que queremos acessar comecando pela posição `0`.

```ruby
array = [1, 2, 3, 4]
array[0] # 1
array[3] # 4
array[5] # nil (em ruby, nil representa um falor nulo)
```

### Hashmaps

O tipo Hashmap é uma forma de se identificar chaves que armazenam valores.
<br>Para declarar um hashmap, usamos chaves e, também, separamos cada item com vírgulas.
<br>Para acessarmos um valor do hashmap, precisamos especificar qual chave queremos acessar.

```ruby
hashmap = {
  chave1: 10,
  chave2: "Olá"
}

hashmap["chave1"] # 10
hashmap["chave2"] # "Olá"
```

## Condicionais

Condicionais são blocos de execução que só podem ser executados baseado em uma condição.<br>
Podemos também especificar uma exceção caso nenhuma das condições tenham sido atendidas.

```ruby
number = 10
is_pair = number % 2 == 0

if is_pair
  puts "is pair"
end
```
Podemos especificar várias condições uma em cima da outra para definir que apenas uma seja atendida.<br>

```ruby
if number == 1
  puts "1"
elsif number == 2
  puts "2"
else
  puts "nothing"
end
```

## Estruturas de repetição

Estruturas de repetição são blocos de execução que podem ser executados repetidas vezes enquanto uma condição for ou não satisfeita.

```ruby
number = 0

while number < 3
  puts number
end

# 0
# 1
# 2
```

## Funções

Funções são blocos de códigos que podem ser declarados e executados quando for necessário.<br>
Elas podem receber parâmetros que são valores para serem utilizados.<br>
O valor da ultima linha da função é o valor que a função retorna para ser utilizado.

```ruby
def somar(valor1, valor2)
  resultado = valor1 + valor2

  resultado
end

valor = somar(2, 3)

puts valor # 5
```

## Observações finais
Esse módulo introduz o contexto geral de como estruturas de dados funcionam, o seu desenvolvimento em algoritmos irá depender de como você usa essas estruturas para resovler um problema.
