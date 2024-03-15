# 02 - (Hello, World!)
No nosso módulo passado, buscamos compreender melhor as funcionalidades do nosso terminal e do sistema operacional.
Aprendemos sobre alguns comandos e que estes são nada menos do que arquivos binários que recebem argumentos e executam uma determinada tarefa.

## Objetivos
Nesse módulo iremos abordar sobre os binários de execução de uma linguagem de programação e iremos escrever nossa primeira linha de código em `ruby`.

## 1 - Package Managers
É de comum acordo que haja uma organização para fazermos downloads de pacotes diferentes. 
Pacotes são nada mais do que conjunto de arquivos que servem um propósito que podem ser instalados na sua máquina local.

Para isso existem os gerenciadores de pacotes, estes que possuem uma gama de pacotes que podem ser baixados via linha de comando no seu terminal.
Existem vários para cada sistema operacional, mas é comum que pelo menos um ja venha pré instalado na sua máquina.

Para Linux/Ubuntu, temos o: `apt` ([Advanced Packaging Tool](https://ubuntu.com/server/docs/package-management))
- Este já virá instalado no seu linux, não se preocupe.

Para Mac, temos o: `brew` ([Homebrew](https://brew.sh))
- Este precisa ser instalado no seu SO (Sistema Operacional).
- Para isso, acesse a [página do homebrew](https://brew.sh) e siga as instruções para instalá-lo.

## 2 - Instalação do Ruby
Antes de aprendermos sobre o ruby de fato, vamos manter no tópico de instalação instalando os binarios do ruby para que possamos executar arquivos de textos com a interpretação do ruby.

Para instalar, vamos utilizar o exemplo da documentação do ruby.

Para `Ubuntu`, execute o seguinte comando no seu terminal:

```bash
  sudo apt-get install ruby-full
```

Este comando vai pedir a sua senha, pois você está executando ele com permissões de root (administrador) ao especificar `sudo` antes do comando

Para `MacOS`, execute o seguinte comando no seu terminal:

```bash
  brew install ruby
```

Depois da instalação, você pode checar

```bash
  ruby --version
```

## 3 - Linguagem de Programação
O conceito de linguagem é nada mais do que um conjunto de padrões de comunicação entre dois ou mais pontos como o inglês, português, etc.<br>
Esse mesmo pretexto funciona para linguagens de programação. Elas possuem um padrão de comunicação que executam tarefas binárias no seu SO e permitem que o que vai ser feito possa ser interpretado por outras pessoas.

Para isso, linguagens de programação são escrita em arquivos de texto e são interpretados ou compilados traduzir seu texto em binários que seu processador irá entender.<br>
Seu processador não entende o texto que você escreveu baseado no padrão estabelecido pela sua linguagem de programação. O seu processador entende instruções binárias e quem sabe traduzir seu texto para essas instruções pode ser um compilador ou um interpretador.

### 3.1 - Compiladores
Compiladores são ferramentas que entendem seu texto escrito baseado nos padrões da sua linguagem de programação, geram os binários de execução e criam um arquivo com esses binários.
Após a geração desses binários estáticos, você vai poder executa-los de maneira direta sem nenhuma tradução simultanea.

- Exemplos de linguagens compiladas: C, C++, Go e Rust

#### Prós
- Eficiência: Códigos compilados são mais rápidos pois são executados em binários nativos sem tradução simultânea.
- Portabilidade: A execução do código compilado se resume somente a execução direta do arquivo binário.
- Otimizações: Compiladores sabem otimizar seu código para rodar da forma mais benéfica possível para seu sistema.
- Segurança: Códigos compilados em binários não possuem legibilidade para permitir que seu código de fato seja revelado.

#### Contras
- Tempo de compilação mais longo: Compilar código pode levar mais tempo do que interpretá-lo, especialmente para bases de código grandes, porque o compilador precisa analisar todo o código-fonte e gerar código de máquina ou bytecode antes da execução.
- Binários específicos da plataforma: O código compilado é frequentemente específico da arquitetura do seu processador, dessa forma seu código tem que ser compilado várias vezes para diferentes processadores para funcionar globalmente.
- Falta de Interatividade: Como a compilação é uma etapa separada da execução, pode ser menos interativa durante o desenvolvimento em comparação com a interpretação, onde as alterações podem ser testadas rapidamente sem recompilação.

### 3.2 - Interpretadores
Interpretadores são ferramentas que possuem o mesmo entendimento do seu código, porém ele adiciona uma camada de abstração que geralmente faz traduções simultaneas em tempo de execução do seu código.<br>
Essa abstração no geral são máquinas virtuais que compilam seu código em `bytecode` (instruções binárias otimizadas que somente a máquina virtual entende) e traduzem para binários nativos do seu processador.

- Exemplos de linguagens interpretadas: Ruby, Java, Javascript e Elixir.

#### Prós
- Interatividade: Linguagens interpretadas normalmente oferecem uma experiência de desenvolvimento mais interativa, já que as alterações no código podem ser testadas imediatamente sem a necessidade de uma etapa de compilação separada.
- Independência de Plataforma: O código interpretado é frequentemente mais portátil do que o código compilado, porque o interpretador abstrai o hardware e o sistema operacional subjacentes, permitindo que o mesmo código seja executado em diferentes plataformas sem modificação.
- Facilidade de Depuração: Depurar código interpretado pode ser mais fácil, pois os interpretadores podem fornecer mensagens de erro mais detalhadas e ferramentas de depuração interativas.

#### Contras
- Overhead de Desempenho: O código interpretado tende a ser mais lento que o código compilado, pois é executado linha por linha, com cada linha sendo traduzida em código de máquina ou bytecode em tempo de execução.
- Dependência do Interpretador: O código interpretado requer a presença de um interpretador na máquina de destino, que pode nem sempre estar disponível ou atualizado.
- Riscos de Segurança: Como o código-fonte original geralmente é distribuído com programas interpretados, ele pode ser mais vulnerável à engenharia reversa e modificações não autorizadas.

### 3.2.1 - Qual é melhor?
A resposta como sempre é: depende. Em geral, se duas ou mais coisas existem e são constantemente utilizadas, é porque dependem de um cenário específico.

- Linguagens compiladas sempre vão ser mais rápidas e eficientes do que interpretadas, mas costumam ser mais difíceis de compreender e escrever devido a um conjunto de regras que permitam essa rapidez e eficiência serem cobertas.
> Exemplos de uso: Sistemas operacionais, banco de dados, serviços que exigem extrema rapidez de execução em larga escala de uso.
- Linguagens interpretadas sempre vão ser mais simples de desenvolver e mais facéis de receberem novas implementações, possibilitando um ambiente mais dinâmico de desenvolvimento. Mas o que permite essa flexibilidade afeta na velocidade dessas linguagens.
> Exemplos de uso: Aplicações web, apps mobile, serviçoes que dependem mais de rapidez no desenvolvimento a praticidade de uso.

## 4 - Ruby
[Ruby](https://en.wikipedia.org/wiki/History_of_Ruby#:~:text=The%20history%20of%20the%20Ruby,the%20Ruby%20on%20Rails%20framework.) é uma linguagem de programação interpretada criada no Japão por *Yukihiro Matsumoto* em 1993.
O que faz essa linguagem ser a escolhida por nós para desenvolvermos ao longo do nosso grupo é a simplicidade de uso. Sua forma de escrever é bem simples e chega as vezes a parecer com que você está lendo um texto em ingles de fato.

### 4.1 - Sintaxe
Toda linguagem tem um padrão de escrita para ser executada. Para compreender melhor sobre como o código de ruby costuma ser escrito, leia o que puder nessa [documentação](https://en.wikipedia.org/wiki/Ruby_syntax).

## 5 - Minha primeira linha de código
Vamos executar nossa primeira linha de código em ruby. Para isso precisamos de seguir o passo a passo:

1. Crie uma pasta no seu terminal que você gostaria de separar para códigos, vou usar o exemplo `coding`:
```bash
mkdir coding
```

<hr>

2. Entre na sua pasta criada:
```bash
cd coding
```

<hr>

3. Abra a pasta no seu VS Code para facilitar criação/edição dos arquivos:
```bash
code .
```

- O comando `code` é um comando do próprio Vs Code para abrir um diretório/pasta e o argumento que sucede o comando é o diretório que você quer abrir, no caso escrevemos "." pois já estamos no diretório que queremos abrir.

<hr>

4. No seu Vs Code, crie um arquivo novo e nomeie ele do que você quiser, desde que ele termine em `.rb`,:
<img width="373" alt="Screenshot 2024-03-14 at 15 49 48" src="https://github.com/code-faith/classroom/assets/76123031/014b1e6d-94c9-4190-9089-f46ab693c11f">

- Nesse caso vamos usar o nome `main.rb`.
- A extensão de um arquivo como `.rb`, `.png`, etc, são meras formalidades para especificar o tipo de conteúdo escrito no arquivo. O interpretador vai entender mesmo se não tiver a extensão, mas vamos manter essa formalidade em dia.

<hr>

5. No seu editor, adicione o código abaixo:
```ruby
names = ["John", "Bob", "Alice"]

names.each do |name|
  puts name
end
```

<hr>

6. No seu terminal `Ubuntu/MacOS`, execute o seguinte comando:
```bash
ruby main.rb
```

- Você deverá ver printado no seu terminal o seguinte:
```bash
John
Bob
Alice
```

### 5.1 O que aconteceu?
Para resumir o que aconteceu no código:

1. Executamos o comando `ruby` que espera interpretar um arquivo de texto para binários nativos. No caso apontamos o arquivo `main.rb`
2. No código declaramos uma `váriavel` names
3. Atribuímos como valor para essa variável a lista de strings (textos): ["John", "Bob", "Alice"]
4. Iteramos por esta lista com o comando `.each`, percorrendo texto a texto.
5. Para cada linha printamos (imprimimos) o texto armazenado na variável `name` no terminal com o comando `puts`

### 5.2 Não entendi nada do que você falou
Essa reação é de se esperar em uma introdução a programação, não se preocupe. Tudo isso será explicado no nosso próximo módulo!

## Observações Finais
Estudem o que não entenderam e reforcem o que ja entenderam deste módulo. Nosso próximo módulo já iremos aprofundar em algoritmos e o entendimento mais claro desse módulo é bem necessário.
