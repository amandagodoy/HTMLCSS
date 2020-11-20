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

Refazendo a página inicial

Em nosso site, temos uma descrição com o título "Sobre a Barbearia Alura". Trata-de se informações que são fechadas em si mesmas, como uma sessão. Em nosso código esse conteúdo está sendo envolvido por uma <div>, mas para casos assim utilizamos a tag <section>.
  
<section class="principal">
                <h2 class="titulo-centralizado">Sobre a Barbearia Alura</h2>

                <p>Localizada no coração da cidade a <strong>Barbearia Alura</strong> traz para o mercado o que há de melhor para o seu cabelo e barba. Fundada em 2019, a Barbearia Alura já é destaque na cidade e conquista novos clientes a cada dia.</p>

                <p id="missao"><em>Nossa missão é: <strong>"Proporcionar auto-estima e qualidade de vida aos clientes"</strong>.</em></p>

                <p>Oferecemos profissionais experientes e antenados às mudanças no mundo da moda. O atendimento possui padrão de excelência e agilidade, garantindo qualidade e satisfação dos nossos clientes.</p>
</section>

A diferença entre <div> e <section> é que no primeiro caso, trata-se apenas de uma divisão visual. Já no caso da <section> teremos uma divisão por conteúdo complexo, semanticamente homogêneo.

Na parte de benefícios, também possuímos conteúdos fechados em si, neste caso também substituiremos a <div> por <section>.
  
<section class="beneficios">
                <h3 class="titulo-centralizado">Benefícios</h3>

                <ul>
                    <li class="itens">Atendimento aos Clientes</li>
                    <li class="itens">Espaço diferenciado</li>
                    <li class="itens">Localização</li>
                    <li class="itens">Profissionais Qualificados</li>
                </ul>

                <img src="beneficios.jpg" class="imagembeneficios">
            </section>
          
Ao retornarmos para o navegador, perceberemos as sessões centralizadas, mas ainda resta fazermos ajustes nas imagens, lista de benefícios assim por diante. Faremos esse processo passo a passo, elemento por elemento, de forma que possamos revisar conteúdos que já conhecemos, assim como evoluirmos o projeto.

Teremos que em alguns pontos reescrever o que já foi feito, pois isso é rotineiro para quem trabalha com desenvolvimento, afinal sempre há implementações novas e atualizações. Sempre será necessário melhorar nossos conteúdos, refatorar códigos, realizar manutenções e reparos.

Seletores Avançados

Nesta aula, estudaremos os seletores avançados, uma forma específica de fazermos seleção de elementos de maneira mais rebuscada. Suponhamos que no interior da <main>, antes de se iniciar a <section>, nós tenhamos um <p> com um conteúdo qualquer. Se retornarmos para o nosso CSS,

<main>
            <p> qualquer conteudo</p>

            <section class="principal">
                <h2 class="titulo-principal">Sobre a Barbearia Alura</h2>

                <img class="utensilios" src="utensilios.jpg" alt="Utensilios de um barbeiro." />

                <p>Localizada no coração da cidade a <strong>Barbearia Alura</strong> traz para o mercado o que há de melhor para o seu cabelo e barba. Fundada em 2019, a Barbearia Alura já é destaque na cidade e conquista novos clientes a cada dia.</p>

                <p id="missao"><em>Nossa missão é: <strong>"Proporcionar auto-estima e qualidade de vida aos clientes"</strong>.</em></p>

                <p>Oferecemos profissionais experientes e antenados às mudanças no mundo da moda. O atendimento possui padrão de excelência e agilidade, garantindo qualidade e satisfação dos nossos clientes.</p>
</section>

No CSS, como fazemos para marcar esse parágrafo de vermelho? Podemos tentar escrever:

main p {
    background: red;
}

Ao carregarmos no navegador, veremos que todos os parágrafos estarão marcados de vermelho, pois coletamos os parágrafos que estavam dentro da <section>, afinal coletamos todos os parágrafos que estão dentro da <main>. Como podemos selecionar um parágrafo de maneira individual?

Com os seletores avançados do CSS,podemos selecionar os filhos diretos de <main>, para tanto, utilizaremos o sinal >, e todo os outros parágrafos serão ignorados, afinal são filhos diretos da <section> e não de <main>.

main > p {
    background: red; 
}

Mas como selecionar o primeiro parágrafo que sucede uma imagem, por exemplo? Conseguimos selecionar o primeiro filho com o seletor que acabamos de conhecer, mas neste caso estamos falando do primeiro irmão que vem depois de um elemento.

Neste caso, usamos img como elemento âncora e para o primeiro irmão usamos o sinal de "+"

img + p { 
    balckground: blue;
}
Para selecionar todos os parágrafos localizados depois de uma imagem usamos o seletor ~

img ~ p {
    background: yellow
} 

É importante lembrar que um seletor pode sobrescrever o outro, pois todos possuem a mesma força. Os seletores avançados nos ajudam a criar estilos mais complexos e utilizar o CSS de uma maneira incrível, com uma autonomia maior do HTML.

No CSS podemos, inclusive, excluir itens específicos. Se quisermos excluir todos os parágrafos que não compõe missao, escreveremos:

.principal p:not(#misssao) {
    background: orange;
}
A exclusão é um elemento poderoso no CSS, principalmente quando realizamos manutenção em algum código que já existe e que não demos modificar tanto o HTML.

Cálculo em CSS3

Como realizar cálculos dinâmicos de posicionamento de elementos no CSS, como altura e largura.

Nosso site deve estar preparado para dispositivos com diversos tamanhos de tela. Um grande problema enfrentado ao desenvolver um site harmonioso é justamente calcular a proporção s dimensões dos elementos em diferentes dispositivos.

Clicaremos sobre a imagem de utensílios de barbeiro com o botão direito do mouse, então selecionaremos a opção "Inspecionar" para acessarmos a ferramenta do desenvolvedor.

Em nosso CSS, verificaremos que o tamanho da imagem é de 120px, mas como podemos fazer com que esse tamanho seja proporcional? Basta mudar para percentual, isto é, 20% de largura tendo a tela como referência.

Para que a imagem sempre ocupe a medida correta em outros dispositivos, utilizamos a propriedade calc. O calculo que desejamos realizar é escrito entre parênteses, em que inserimos o primeiro valor, o tipo de operção e o resultado esperado.

.utensilios {
    width: calc(40% - 26px);
    float: left;
    Margin: 0 20px 20px 

}

Dessa forma, foi calculado precisamente 350px de largura para este elemento. É possível encadear quantas operações quisermos, no mesmo modelo de sintaxe.

.utensilios {
    width: calc(40% - (26px * 4);
    float: left;
    Margin: 0 20px 20px 

}

A propriedade calc nos dá o poder de fazer com o que calculemos valores proporcionais específicos.

Opacidade nos elementos

Como gerar opacidade em nossos elementos? A opacidade é uma camada a mais posta sobre a imagem, como um insulfilme para a janela de carro, que oferece níveis diferentes de proteção contra o Sol.

Utilizaremos a imagem da sessão "Benefícios" para compreendermos o funcionamento da ferramenta de opacidade no HTML. Em index.css , utilizaremos a propriedade opacity que pode ter valores entre 0 a 1, sendo que 0 o elemento estará totalmente oculto. Se quisermos exibir a imagem com opacidade de 30%, ajustaremos o valor da propriedade para 0.3.

.imagem-beneficios {
    width: 60%
    opacity: 0.3;
}

Esse recurso é interessante quando montamos composições visuais com elementos sobrepostos, ou para sugerir interações com o mouse ao utilizarmos o hover. Quando o mouse estiver posicionado sobre a imagem teremos 1 de opacidade.

.imagem-beneficios:hover {
    opacity: 1;
}

Temos ainda o recurso transition, em que podemos estabelecer uma transição da opacidade em determinados milissegundos.

.imagem-beneficios {
    width: 60%
    opacity: 0.3;
    transition: 400ms;
}

Em nosso site, faremos com o que o comportamento padrão da imagem seja de opacidade 1, e no momento em que mouse estiver sobre ela a opacidade será de 0.3, o que irá gerar um belo efeito visual.

Atualmente, podemos utilizar opacidade em todos os elementos e em cores, vamos entender melhor como isso ocorre.

A cor de titulo-principal possui a cor padrão #00000, preto. Como podemos fazer com que essa cor que está em hexadecimal? se torne RGB? Isto é, a mesma cor escrita em outra linguagem? Do seguinte modo:

.titulo-principal {
    text-align: center;
    font-size: 2em;
    margin: 0 0 1em;
    clear: left;
    color: rgb(0,0,0);
}

Com CSS 3, podemos utilizar mais uma camada - a de opacidade, chamada alfa - nas cores em RGB. Para tanto, utilizamos o rgbae então definir os valores que quisermos.

.titulo-principal {
    text-align: center;
    font-size: 2em;
    margin: 0 0 1em;
    clear: left;
    color: rgb(0,0,0,0.3);
}

Esse recurso pode ser utilizado em todas as cores: de fundo, texto, borda e assim por diante.

Sombra nos elementos

as sombras, uma outra novidade que CCS 3 inseriu. Fazer sombras em elementos sempre foi muito difícil nas versões anteriores, hoje em dia, trata-se de algo trivial.

Continuaremos a usar a imagem da sessão de "Benefícios". A sombra é resultado de um efeito de "luz" que lançaremos sobre o elemento. O nome da propriedade que utilizaremos para gerar esse efeito é box-shadow, que possui a propriedade do eixo X, T e uma cor. Queremos deslocar 10px no eixo X e Y, a cor que utilizaremos será preto.

.imagem-beneficios {
    width: 60%
    opacity: 1;
    transition: 400ms;
    box-shadow: 10px 10px #000000;
}

Ao recarregarmos a página, teremos uma sombra projetada, quadrada.

sombra

(referencia de imagem está no 5_2_1_sombra.png)

Podemos melhorar a qualidade estética dessa sombra ao adicionarmos uma terceira propriedade chamada blur, em que podemos aplicar um nível de desfoque específico, no caso, inseriremos um valor de 5px. Quanto maior a quantidade de pixels que inserirmos, mais claro sera o efeito de desfoque.

.imagem-beneficios {
    width: 60%
    opacity: 1;
    transition: 400ms;
    box-shadow: 10px 10px 5px #000000;
}

Ao recarregarmos a página, veremos o efeito aplicado na sombra da imagem.

blur

(referencia de imagem está no 5_2_2_blur.png)

Temos ainda uma quarta propriedade que configura a intensidade da borda a partir do tamanho do elemento, isto é, o tamanho da sombra projetada. Neste caso, inseriremos 20px:

.imagem-beneficios {
    width: 60%
    opacity: 1;
    transition: 400ms;
    box-shadow: 10px 10px 5px 20px #000000;

}

No navegador, a sombra sugirá expandida.

sombragrande

(referencia de imagem está no 5_2_3_sombragrande.png)

Podemos adicionar várias sombras em um mesmo elemento, basta que o conteúdo esteja separado por uma vírgula. Essa nova sombra terá valores negativos e terá a cor amarela.

.imagem-beneficios {
    width: 60%
    opacity: 1;
    transition: 400ms;
    box-shadow: 10px 10px 5px 20px #00000, -10px -10px yellow;

}

Será projetada uma sombra por debaixo da anterior.

Podemos, ainda, inserir uma terceira sombra com a cor rgba() com a camada de opacidade e borda vermelha.

.imagem-beneficios {
    width: 60%
    opacity: 1;
    transition: 400ms;
    box-shadow: 10px 10px 5px 20px #00000, -10px -10px yellow, -20px 20px rgba(255,0,0,0.5);

}

Ao recarregarmos a página teremos três sombras.

sombras

(referencia de imagem está no 5_2_5_sombra.png)

Outra possibilidade no CSS 3 é criar sombras internas. Utilizaremos a própria sessão de benefícios para exempliciar esse efeito, que será utilizado em box-shadowe se chama inset. Seu posicionamento será a partir do centro do elemento e terá a cor vermelha.

.beneficios {
    padding: 3em 0;
    background: #888888;
    box-shadow: inset 0 0 #FF0000;
}

Ao carregarmos a página, não notaremos qualquer mudança. Isso se deve pelo fato de que a sombra possui o mesmo tamanho do elemento. Para que ela se torne perceptível, criaremos um espaçamento de 30px.

.beneficios {
    padding: 3em 0;
    background: #888888;
    box-shadow: inset 0 0 30px #FF0000;
}

Feito isso, a sombra será interna em toda a sessão de benefícios.

sombra

(referencia de imagem está no 5_2_5_sombras.png)

Apagaremos todas as sombras coloridas e manteremos apenas a sombra leve em imagem-beneficios.

.imagem-beneficios {
    width: 60%
    opacity: 1;
    transition: 400ms;
    box-shadow: 10px 10px 10px 0 #000000;
}

Para fechar o tópico de sombras, por último aprenderemos a inserir sombras em textos. Em titulo-principal, utilizaremos a propriedade text-shadow, que recebem os valores que já conhecemos.

.titulo-principal {
    text-align: center;
    font-size: em;
    margin: 0 0 1em;
    clear: left;
    text-shadow: 2px 2px #FF0000; 
}

Será criada uma sombra para o título.

texto vermelho

(referencia de imagem está no 5_2_6_texto+vermelho.png)
