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

Entendendo transformações no CSS3

E o que é mais possível fazer com o transform? Existe uma outra propriedade chamada “rotate” que inclina o meu item quantos graus eu quiser. E aqui vamos colocar 70 graus. Nós usamos a medida de graus em inglês que são “degrees”, “transform: rotate(70deg);”. Quando carrego isso aqui e passo o mouse por cima do elemento, ele roda o meu item em 70 graus; e quando tira o mouse, ele volta para original.

Reparem que ele parou proporcionalmente, e por que isso aconteceu? No CSS a leitura é sempre feita de cima para baixo. O último item sobrescreve o anterior, então aqui, como temos duas propriedades iguais, a última que vai ser lida. Essa aqui vai ser lida e vai ser ignorada. Como que eu faço então para somar essas duas propriedades no transform? Eu simplesmente adiciono uma depois da outra, com um espaço. Se eu salvar isso aqui e recarregar no meu navegador, ele vai aumentar e rodar.

E aqui eu posso colocar qualquer coisa. Eu posso colocar para rodar mil graus, eu posso colocar para aumentar por três vezes, que ele vai fazer essa maluquice aqui. Não é isso que queremos para o nosso usuário. Queremos para o nosso usuário só que esse item aumente em 20%.

Existem outras transformações possíveis e vale muito a pena você explorar, porque facilita muito a criação e a mudança de itens quando ele já está carregado na página via CSS. Agora que vimos as transformações, vamos seguir a nossa página e terminar o conteúdo usando tabelas.

Estilos na tabela

Para isso usamos a vírgula e marcamos a tag. Se quiser vamos deixar isso um pouco mais específico, podemos colocar uma classe na tabela e só fazer nas células do cabeçalho do conteúdo daquela tabela específica. Mas já que botamos a vírgula, todos os itens então devem ficar com essa borda preta marcando esse conteúdo.

Melhorando a semântica do HTML5

Quando eu poderia usar esse aqui além do que eu já estou usando? Quando, por exemplo, eu tenho o preenchimento dos dados de um cartão de crédito. Todos os dados referentes àquele cartão podem estar dentro de um fieldset. Ou os dados de um endereço. E dentro de um fieldset não temos parágrafos, nós temos o título, e o título de um fildset é chamado de legend.
