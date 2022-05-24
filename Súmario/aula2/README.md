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


Também podemos extrair mais de um valor usando a c()função dentro dos colchetes. Vamos extrair os valores nas posições 1º , 5º , 6º e 8º do vetor criado.
