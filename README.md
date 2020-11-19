# html-css-primeirapaginadaweb


Exemplificando o nível de importância de algumas propriedades no CSS3 com autoria de Pedro Marins (https://www.linkedin.com/in/pedromarins/)

inline = 1000 vlr
id = 100 vlr
class = 10 vlr
tag = 1

ex: p = 1

form p = 1+ 1 = 2

.teste = 10
p.text = 11

Então sempre quando estamos criando css, precisamos pensar o quão especifico  é o nosso marcador e o quão for ele vai ser, para que ele não seja sobrescrito  por qualquer outro. Além de não cometemos erros no nosso código. 
Por isso a recomendação de criar classes para os elementos é muito boa, ele não é genérico o suficiente para que eu mude a tag, e ele não é especifico como um identificador para que ele só funcione naquele elemento. Ele é um estilo que pode ser replicado varias vezes como a classe e em vários elementos.
A única forma de alterarmos isso, algo mais forte que o identificador é quando temos o estilo inline que seria colocada no HTML e não no CSS, nada substitui ele sendo o mais forte por estar no elemento.

Melhorando a semântica do HTML5

Quando eu poderia usar esse aqui além do que eu já estou usando? Quando, por exemplo, eu tenho o preenchimento dos dados de um cartão de crédito. Todos os dados referentes àquele cartão podem estar dentro de um fieldset. Ou os dados de um endereço. E dentro de um fieldset não temos parágrafos, nós temos o título, e o título de um fildset é chamado de legend.
