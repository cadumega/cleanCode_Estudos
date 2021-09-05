# cleanCode_Estudos
Estudos do Livro Clean Code e da Playlist sobre o assunto - Felipe Deschamps.


# Organizar em partes iniciais, pois fica algo fácil de extratificar e corrigir.
-O que o meu programa gostaria de fazer?
-Como esta fazendo? (implementações)

# Books: Refactoring e Clean Code
## Resumo Clean Code da Playlist Felipe Deschamps:

1- Controle de qualidade na manutençao e não na produçao como é feito na maioria das vezes.
2- Ordenação nomear arquivos, variaveis,funcoes.
3- Sistematizar cada coisa no seu lugar, o pedaço de código estar onde precisa estar.
4- Limpeza , facilitação do seu código, nao manter código de blocos comentados.
5- Padronização
6- Faça programas fácil de refatorar. código legível mais fácil de manutencao

___
Parte 2
Previsibilidade do que você irá encontrar, detalhes da implementação. 

O por que do codigo sujo?
Entregar coisas rápidas demais, deadline curto, querer partir para a proxima implementacao ou feature.

Se atentar ao consertar as features , mas que geram novos bugs.

Se afasta ou se aproxima do design desejado do projeto.

A pessoa realmente se importou em fazer.

Importancia de colocar os nomes em arquivos,branches,variaveis,funcoes...
___
Parte 3
Precisão para passar a mensagem no código, dar nomes bom leva tempo mas economiza na interpretação.
Nomes que não revelam nada. " let t; " Sugestão melhor let tempoDaVoltaEmSegundos;  let segundosDaVolta;   let voltaEmSegundos;  "

Fica mais intuitivo.

var pista = new Pista ('interlagos');

pista.on('evento', function(data) {
  if (data.t < pista.r) {
    pista.r = data.t;
    pista.save( );
    }
})

Deduzir que carrega instancia de uma pista.. explicacoes que poderiam estar no codigo ex:

var pista = new Pista ('interlagos');

pista.on('evento', function(data) {
  if (volta.tempoEmSegundos < pista.recordeEmSegundos) {
    pista.recordeEmSegundos = volta.tempoEmSegundos
    pista.save( );
    }
})

Codigo com mesma quantidade de linhas,var, mesma complexidade. Só mudou em deixar as informações mais explícitas.

Cuidado em colocar nome ou tipo de variavel mas sendo uma string, e não uma array. Ex:
console.log(listaDePistas)
console.log(typeof listaDePistas)

Cuidado em abreviar variaveis. Ira gastar tempo em explicar o codigo.

address.zc;
address.zipc;
address.zcode;

Não escreva codigos para agradar outros humanos, e não agradar o computador ou interpretador.
p1 ,p2, p3 , a, info,table,

Nomes fáceis de encontrar, "a" você irá esbarrar em arquivos ou outras inconsistênias.

Cuidado com nomes longos, focar na leitura dinâmica.

_____
parte 4 - Funcoes.
Alguns códigos sao mais rapidos de ler , ou de isolar e encontrar os bugs.
Leitura escaneando.
Tamanhos de funcoes menores.

Maiores logicas, mais dificil de ler o codigo. 
Mais fragmentacoes, para encontrar os detalhes das implementacoes.

Funcao pequena, se torna especialista no assunto, escopo delimitado.

Funcao esta fazendo mais de uma ação. Níveis de abstração que facilitem o escopo delimitado da função e não de forma abstraida.

Níveis de identação cada vez mais níveis de implementações. 

A vida é um pêndulo, experimentar o oposto do que você faz, testar o outro extremo.

____
parte-5 Comentários
Comentários redudantes ou longos,podem criar ruídos. 
Precisou colocar comentario sobre determinado código, significa que o código não esta legível, incapacidade de se conectar ao humano.
Ter o mindset para saber se expressar. 

Amplificar algo.
Explicar o porque foi feito daquela forma, regras de negócios.


Outros tópicos:
Fazer tratamentos de erros
Testes unitários
Classes
