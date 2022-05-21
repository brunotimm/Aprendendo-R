# Aula 1
## Funções

### O que são objetos?
Os objetos são tudo aquilo que você cria em R. Esses objetos podem ser quase qualquer coisa, desde um único número ou cadeia de caracteres (como uma palavra) até estruturas altamente complexas, como a saída de um gráfico, análises estatísticas e etc.
Para criarmos um objeto basta darmos o nome ao objeto e atribuir a ele um valor por meio do operador de atribuição <- (também conhecido como *operador gets*). Vamos criar um primeiro objeto
  
    obj1 <- 98
  
* criamos um objeto que contem o valor 98

Todos os objetos que você criarmos serão armazenados na área de trabalho atual e podemos visualizar todos os objetos na área de trabalho no RStudio clicando na guia *Environment*.

![Imagem1b](https://user-images.githubusercontent.com/96084042/168702888-07935538-b338-4ddd-881c-e711b0d8dd53.png)

Ha algumas informações relevantes nessa seção que serão abordados mais detalhadamente no tópico de estrutura e tipos de dados, mas que valem apena serem explicados de forma simples por agora. Temos, o nome do objeto, o tipo de dado que ele é na coluna *Type*, o comprimento do objeto é dado por *lenght*, e o valor atribuido ao objeto é dado pela caluna *Value*.


Para vermos o objeto que criamos podemos chama-lo de duas formas distintas, que são:

    print(obj1) 

ou

    obj1 
    
O resultado entretanto, é o mesmo independentemente da forma adotada

![Imagem1a](https://user-images.githubusercontent.com/96084042/168704073-80b62640-da79-4bb9-8510-808f2ed7e7fa.png)


Podemos criar objetos que contenham cadeias de caracteres (também conhecidos como *string*) 

    obj2 <- "cachorro e gato"
    
![imagem1d](https://user-images.githubusercontent.com/96084042/168705819-23336469-7d30-479e-9e06-8a3cbbcd68d9.png)

Observe o tipo de dado que caracteriza o nosso objeto 2.

* Quando criamos um objeto que contenha um string, essa precisa ser escrita entre aspas, caso contrário R retornará um erro, veja

![Imagem1c](https://user-images.githubusercontent.com/96084042/168705107-54acd40c-5bb4-45f8-b62f-80a1d5ba86b4.png)


Podemos alterar o valor de um objeto já criado. Para isso, basta atribuirmos outro valor a esse objeto

    obj2 <- 10 
    
 ![imagem1e](https://user-images.githubusercontent.com/96084042/168705917-66665c78-1c62-4b6b-9776-0d7e6b654de6.png)

* Mais uma vez, observe que o tipo de dado mudou.




Uma vez que criamos nossos objetos, podemos realizer operaçõe aritméticas com eles. 

![imagem1f](https://user-images.githubusercontent.com/96084042/168835147-23bdc6a6-1416-42e2-a4ff-4cc26fe09752.png)


* Vale dizer que o R funciona como uma calculadora e devido a isso segue as ordens das operações matemáticas. 


No entanto se tentarmos realizar ações com objetos do tipo caracter, o R retornará um erro

![imagem1g](https://user-images.githubusercontent.com/96084042/168837016-38bd2508-abc6-4a35-8d80-fd29ac7e8c86.png)

* A mensagem de erro está informando que ambos os objetos não são um número e, portanto, não podem ser somados.


### Funções
A medida que progredimos no aprendizado e uso da linguagem iremos nos deparar com problemas e tarefas que demandem estruturas mais complexas do que os simples objetos que criamos, em decorrência disso as funções são importantes e facilitam muito a otimização de códigos e tarefas, além de nos ajudar a resolver muitos problemas. Mas o que são funções? Pense em funções como um meio de personalizar as funcionalidades do R, funções são estruturas que contém uma série de instruções para realizar uma tarefa específica.
A primeira função que abordo é bem simples mas muito importante para realizar muitas tarefas e também para utilizar funções mais complexas que serão abordadas adiante. Estou falando da função c() (abreviação de concatenar). Essa função armazena uma série de valores em uma estrutura de dados chamada vetor. (os vetores serão detalhados no tópico 3). Vamos criar nosso primeiro vetor

    vetor1 <- c(2,,4,6,8,10,4)
    
* O que vai dentro da função é o que chamamos de argumento. Um argumento nada mais é que a personalização das funcionalidades das funções. Cada função possui diferentes argumentos que podem ser encontrados no documento de ajuda associado a cada função na guia de ajuda, e que são acessados por meio da função help(), caso você não saiba como usar a função. Além disso, os argumentos de uma função sempre separados por vírgulas. 


Com o nosso primeiro vetor criado podemos usar outras funções para calcular algumas estatísticas. Por exemplo, podemos calcular a média, a variância, o desvio padrão e número de elementos em nosso vetor usando as seguintes funções

##### Média e Mediana

    mean(vetor1) 
  
    median(vetor1)

![imagem1h](https://user-images.githubusercontent.com/96084042/168922037-e2fe6a25-7353-41ff-b6ad-fb71af1aac7a.png)


##### Variância, Desvio Padrão e Número de Elementos

    var(vetor1)
    
    sd(vetor1)
    
    length(vetor1)


![imagem1i](https://user-images.githubusercontent.com/96084042/168922473-8a6f76da-8e7f-45c2-9d93-9845708c974b.png)


Se quisermos utilizar ou precisarmos utilizar os valores resultantes, basta atribuirmos esses a novos objetos, veja: 

    media_vetor1 <- mean(vetor1)
    
    var_vetor1 <- var(vetor1)
    
    desvio_vetor1 <- sd(vetor1)



![imagem1j](https://user-images.githubusercontent.com/96084042/168925634-885704b4-8e33-4b6b-8dd1-c383d321777f.png)


### Sequências
Quando queremos trabalhar com sequencias regulares de valores pode ser útil criar vetores para isso. Há duas formas a se fazer isso, por meio da função seq() ou com a utilização do símbolo : que separa o intervalo de valores, vejamos: 

##### Ordem crescente
    my_seq <- 20:30

![imagem1k](https://user-images.githubusercontent.com/96084042/169661003-2643f1b8-c124-4e42-8150-37086723632c.png)
* observem que essa sequência tem como caractéristica de seus dados números inteiros, diferentemente dos objetos que foram criados anteriormente. 

##### Ordem decrescente
    my_seq2 <- 40:30 

![imagem1k2](https://user-images.githubusercontent.com/96084042/169661042-40c358e8-42d0-4bf3-bc7b-7d4c99286197.png)


##### Usando a função seq()
    my_seq3 <- seq(from = 100, to = 110, by = 3) 

![imagem1k3](https://user-images.githubusercontent.com/96084042/169661045-73f25e81-50a3-4d57-a17b-859d7b486d6f.png)

* Os argumentos *from* e *to* indicam respectivamente onde começa e onde termina a sequência, o argumento *by* indica ao R de quanto em quanto é a contagem.


### Repetições
É possível repetir as sequências e valores que criamos quantas vezes desejarmos através da função rep()

    my_seq4 <- rep(0.5, times = 3)
    my_seq4
    
 ![imagemL](https://user-images.githubusercontent.com/96084042/169661428-f4b1262b-d4ca-4312-9915-27b7567b1835.png)   
    
* a primeira parte do argumento indica o numero a ser repetido (0,5), a segunda com o argumento *time*, o nº de vezes que desejamos repetir nosso dado.


Também podemos fazer repetições de caractéres

![imagemL1](https://user-images.githubusercontent.com/96084042/169662029-c22d0ab6-34ed-470f-9806-df0c6bc059c0.png)


Repetindo uma sequência

![imagemL2](https://user-images.githubusercontent.com/96084042/169662079-6d2829fd-5fac-402a-a614-2eeb6bfa0ed4.png)

Se quisermos repetir os elementos da série ao invés da série como um todo, usamos o argumento *each* 

![imagemL3](https://user-images.githubusercontent.com/96084042/169662162-0608ee06-9f40-4518-9ba9-d68d7cfa1a47.png)


### Aninhamento de funções: funções dentro de funções 








