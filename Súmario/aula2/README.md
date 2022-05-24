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






















