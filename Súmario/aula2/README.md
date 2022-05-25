# Aula 2
## Manipulando vetores

Após aprender a criar e usar objetos e vetores precisamos aprimorar as habilidades em trabalhar com esses, como manipular, resumir e classificar dados usando R . Veremos alguns exemplos simples usando vetores para ilustrar alguns conceitos importantes, mas desenvolveremos isso com muito mais detalhes no Capítulo 3.


### Extraindo elementos
Para extrair (também conhecido como indexação ou subscrito) um ou mais valores (mais geralmente conhecidos como elementos) de um vetor, usamos [ ]. Essa extração pode ser feita de duas maneiras por meio de Índice lógico ou por meio do Índice posicional. 

##### Índice posicional
    my_vec <- c(2,8,8,4,0,7,4,2)
    my_vec[4] 

* extração do valor(elemento) na posicao 4 do argumento 

![imagem2a](https://user-images.githubusercontent.com/96084042/169907823-35adb0b7-189e-47a2-b1d5-b115faa1a81b.png)

E podemos armazenar esse valor extraído em um outro objeto

    val4 <- my_vec[4] 
    val4
    
![imagem2b](https://user-images.githubusercontent.com/96084042/169907945-38e24e47-6ff5-48dd-9086-7aeaea495530.png)


Também podemos extrair mais de um valor usando a c()função dentro dos colchetes. Vamos extrair os valores nas posições 4º , 7º e 8º do vetor criado.

        my_vec[c(4,7,8)]
        
![imagem2c](https://user-images.githubusercontent.com/96084042/170108316-ada7c9fa-86e3-455a-abb9-fbc53e65e482.png)

Ou também extrair uma sequência de valores. Por exemplo extrair os valores da posição 3º até a posição 8º 

        my_vec[3:8]

![imagem2d](https://user-images.githubusercontent.com/96084042/170110053-ea6fd9aa-6c04-446a-b9f7-54dc51ebadbe.png)


##### Índice Lógico
Uma outra maneira útil de se extrair dados de um vetor é por meio de expressões lógicas. Nesse tipo de extração condicionamos a extração ao uso de expressões lógicas
como por exemplo extrair todos os elemenos maiores ou iguais a 3. 

        my_vec[my_vec > 3] 
        my_vec > 3
        
* Sem uso dos colchetes o R nos retorna se a condição dada por meio das expressão lógica é satisfeita. 

![imagem2e](https://user-images.githubusercontent.com/96084042/170112028-a2ac33a6-ba4a-4b09-b3e9-9dbfb55d7a49.png)

Podemos fazer o processo inverso também. Ao invés de usarmos os valores que queremos extrair, indicamos nos colchetes as condições *TRUE* e *FALSE* para que então o R nos retorne os valores correspondentes do vetor.

![imagem2e](https://user-images.githubusercontent.com/96084042/170112857-6dda9ffe-a672-477a-950d-30f4a600399f.png)

Os operadores lógicos para extração de valores via índice lógico são os mesmo das relaçãoes lógicas que usamos na matemática usual

##### Operadores lógicos

        my_vec[my_vec >= 3] maior ou igual
        my_vec[my_vec < 7]  menor que
        my_vec[my_vec <= 7]  menor ou igual que
        my_vec[my_vec == 8]  igual a
        my_vec[my_vec != 2] diferente de 


É possível combinar expressões lógicas (conhecidas como expressões booleanas). Para isso utilizamos os símbolos *&* que significa E; e o símbolo *|* que significa OU. Lembrando nosso vetor, temos:
       
       my_vec <- c(2,8,8,4,0,7,4,2)

![imagem2g](https://user-images.githubusercontent.com/96084042/170356294-414ac920-b2e8-41dd-9827-20b4872a5b20.png)


* a primeira expressão indica que queremos que o R retorne dentre os valores do nosso vetor valores menores que 8 E maiores que 4
* a segunda expressão indica que queremos que o R retorne os valores maiores que 5 OU maiores iguais a 7

Perceba que no primeiro caso queremos como resultado as duas condições indicadas pela expressão lógica, já no segundo caso queremos que uma das das duas condições seja satisfeita ou ambas. 


##### Substituindo Elementos

Podemos alterar os valores de alguns elementos em um vetor usando nossa [ ]notação em combinação com o operador de atribuição <-. Vamos por exemplo alterar o valor do elemento na posição 5 do nosso vetor que até então é 0 para 30

        my_vec[5] <- 30
        my_vec[5]
        my_vec

![imagem2a2](https://user-images.githubusercontent.com/96084042/170365727-2bf5b052-ce2f-4936-a77d-16462823c9ea.png)

E também alterar uma cadeia de valores 

    my_vec[c(1,7,8)] <- 179 
    my_vec
    my_vec[my_vec <= 7] <- 93
    my_vec

![imagem2b2](https://user-images.githubusercontent.com/96084042/170365992-d3cf6fe4-68be-477c-9f26-ff14b5e01cdf.png)

##### Elementos de pedido
Além de extrair elementos específicos de um vetor, também podemos ordenar os valores contidos nesse. Para classificar os valores do menor para o maior valor, podemos usar a função sort(). A função sort ordena em forma crescente os valores do vetor

    vecsort <- sort(my_vec) 
    vecsort

![imagem2c2](https://user-images.githubusercontent.com/96084042/170366822-f209f167-64f0-401d-9b77-ca77ac377840.png)

Para fazer a ordem decrescente adicionamos o argumento *decreasing = TRUE* 

    vecsort2 <- sort(my_vec, decreasing = TRUE) 
    vecsort2

![imagem2d2](https://user-images.githubusercontent.com/96084042/170367260-aa121ef6-b965-407b-a2fc-75847fda1056.png)

Outro modo de classificar os vetores é classifica-los um vetor de acordo com os valores de outro vetor. Para fazer isso, devemos usar a função order() em combinação com []. Vamos supor então a altura de um grupo de 5 crianças: Pedro, Carlos, Ana, Bia e Helen

    altura <- c(180, 155, 160, 167, 181) 
    altura
    
    nomes <- c("Pedro", "Ana", "Helen", "Carlos", "Bia") 
    nomes

![imagem2e2](https://user-images.githubusercontent.com/96084042/170368422-648a7eb3-3a23-4c8d-8c0c-d90c6cdc6b23.png)


Nosso objetivo é ordenar as pessoas em nomes ordem crescente das alturas. A primeira coisa que faremos é usar a  função order() com a variável altura para criar um vetor chamado altura_ordem

    altura_ordem <- order(height) 
    altura_ordem

    nomes <- c("Pedro", "Ana", "Helen", "Carlos", "Bia") 
    nomes

![imagem2f2](https://user-images.githubusercontent.com/96084042/170370050-958e8238-4d01-46c6-8b1e-cbc1797e7637.png)

Queremos que a função colocou em ordem as alturas em ordem de termos, portanto o 2 da saída corresponda ao 2º elemento do vetor altura, que representaria a menor altura (155) e portanto o primeiro elemento da ordem e assim sucessivamente. Após criado o vetor ordem das alturas criamos um vetor ordem por nomes e utilizando o objeto nomes, ordenamos as alturas através do nome das crianças.

    altura_ordem <- order(altura) 

    nomes_order <- nomes[altura_ordem] 
    nomes_order

![imagem2g2](https://user-images.githubusercontent.com/96084042/170370603-1c10de33-cb5f-408d-ac65-1f32769a7c45.png)



























