# Aula 3
## Tipos de Dados
R tem seis tipos básicos de dados; numérico, inteiro, lógico, complexo, caractere e brutos. Compreender os diferentes tipos de dados e como o R lida com esses dados é importante e útil para lidar com alguns problemas e imprevistos durante os trabalhos que se realiza, mas principalmente quando se trata da importação e manipulação de base de dados. 


Os tipos de dados são: 

* *Dados numéricos:* 
São números que contêm um decimal. Na verdade, eles também podem ser números inteiros, mas não vamos entrar em detalhes sobre isso nesse material.

* *Dados inteiros:*
Os inteiros são números inteiros (os números sem um ponto decimal).

* *Dados lógicos:*
Os dados lógicos assumem o valor de TRUEou FALSE. Há também outro tipo especial de lógica chamada NApara representar valores ausentes.

* *Caracteres:*
Dados de caractere são usados para representar valores de string. Caracteres nada mais são do que uma palavra (ou várias palavras). Um tipo especial de string de caracteres é um factor , que é uma string mas com atributos adicionais (como níveis ou uma ordem). Abordaremos os fatores mais tarde.

* *Dados Brutos:*
Dados brutos sao os dados que encontramos nas planilhas eletrônicas (como Excel por exemplo). Eles são brutos porque não receberam qualquer tipo de tratamento ou organização até a coleta feita. 


![imagem3a](https://user-images.githubusercontent.com/96084042/174133950-e01b134e-3d80-4ffe-b686-274a3ffd5bbd.png)

Outra maneira de descobrir um tipo de daod é por meio de um teste lógico, com a função is.tipodedado que se quer confirmar. Os resultados desse comando resultaram sempre em *TRUE* ou *FALSE* o que signfica se o seu objeto corresponde ou não ao tipo de dado que você atribuiu a ele. 

![imagem3b](https://user-images.githubusercontent.com/96084042/174135026-bf26ed6d-e051-4ec8-b936-d507c0d06373.png)


Em alguns momentos pode ser necessário converter o tipo de dado de uma variavel. Esse processo pode ser realizado por meio da familia de funções de coerção as.nomeclass

![imagem3c](https://user-images.githubusercontent.com/96084042/174137134-c952e053-6126-4ebc-b2fc-83c348bc5bd8.png)




