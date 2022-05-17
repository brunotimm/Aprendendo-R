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

![imagem1f](https://user-images.githubusercontent.com/96084042/168707653-5e63a3d4-35f8-4057-a3e9-1d71d7353627.png)


* Vale dizer que o R funciona como uma calculadora e devido a isso segue as ordens das operações matemáticas. 











