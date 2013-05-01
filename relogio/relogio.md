Relógio

marco.mangan@gmail.com

# Introdução

O relógio é um componente simples, para testes de integração com o Moodle 2.0 utilizando o framework SODA. O componente apresenta hora e minuto conforme o relógio do computador servidor. Para relacionar o componente com o SARC, o relógio comunica o horário oficial da PUCRS e o código alfanumérico que a universidade associa a este horário. Além disso, a atualização periódica de telas é uma função utilizada no SARC para apresentar as alocações.

O módulo tem que funcionar mesmo sem JavaScript, segundo a orientação do Moodle.org aos desenvolvedores. Para apresentar o horário correto, o componente necessita de um script no lado cliente ou de alguma outra forma de animação. O relógio deixa de ser atualizado em tempo real, caso o navegador não permita o uso de JavaScript ou CSS3. 


# Requisitos

A modelagem deste componente iniciou em 2007 e foi retomada em 2009 e em 2013. A lista de requisitos foi desenvolvida como exercício na disciplina de Modelagem de Sistemas. 

- R01	Considerar como referência o horário do servidor na PUCRS.
- R02	O horário apresentado é o mesmo que regula a entrega de trabalhos via Moodle.
- R03	Apresentar o código alfanumérico de dias da semana da PUCRS correspondente ao horário.
- R04	Não sobrecarregar o processamento no computador cliente.
- R05	Não sobrecarregar o processamento no computador servidor.
- R06	Não sobrecarregar a conexão de rede.
- R07	Sempre que possível, operar sem a necessidade de conexão de rede.
- R08	Tratar eventos do ambiente Moodle (ex. troca de tela).
- R09	Tratar eventos do navegador da Web (ex. navegação, atualização).
- R10	Permanecer em execução contínua por longos períodos de tempo
- R11	Integrado com o núcleo Moodle (plug-in)
- R12	Integrado com a interface do Moodle (box)
- R13	Respeitar o padrão da interface do Moodle.
- R14	Respeitar o estilo da interface do Moodle.
- R15	Apresentar o nome da PUCRS
- R16	Apresentar o logotipo da PUCRS
- R17	Apresentar cores da PUCRS
- R18	Tratar mudança de horário de verão
- R19	Ignorar mudança de horário no computador cliente
- R20	Tratar mudança de horário no computador servidor
- R21	Funcionar com o Internet Explorer e o com o Mozilla e com Safari.
- R22	Tratar a acessibilidade.
- R23	Tratar a conformidade com especificações de hiperdocumentos (ex. XHTML válido)
- R24	Apresentar lista completa de código de horários da PUCRS
- R25	Apresentar código do horário anterior
- R26	Apresentar código do horário posterior
- R27	Apresentar limite com horário anterior
- R28	Apresentar limite com horário posterior
- R29	Respeitar normas para apresentação da informação de data
- R30	Respeitar normas para apresentação da informação de horário
- R31	Apresentar a data correta
- R32	Apresentar o dia da semana correto
- R33	Respeitar gramática e ortografia
- R34	Operar corretamente em dias não letivos
- R35	Operar corretamente em horários não letivos
- R36	Respeitar o calendário da PUCRS
- R37	Apresentar mostrador digital
- R38	Apresentar mostrador analógico
- R39	Apresentar mostrador analógico-digital
- R40	Apresentar configuração de omissão/apresentação de informações para o módulo (não por usuário)

# Maquete

13h01
    5E |                  | 5FG
11h30  |   11h35 - 12h25  |   14h00
ooooo.........
quinta-feira, 6 de dezembro de 2007

#Desenvolvimento

O componente será criado manualmente e também com o SODA. 

Manter o código do plugin sob versionamento pode ser um problema.
A pasta utilizada na sincronização com o repositório poderia ser associada com uma pasta do servidor através de um atalho. 

A segunda versão do componente deve apresentar um bloco com a data e hora do servidor no momento da criação do bloco. 

A versão final deve atender todos os requisitos e apresentar data, horário e a codificação correspondente utilizada pela PUCRS.

Serviço cron no Moodle.

#Críticas à documentação sobre blocos

A documentação sobre blocos (1) omite o início do bloco de script PHP (<\?php) no código fonte apresentado. O Moodle 2.4 não aceita o código da forma que aparece na documentação: os arquivos version.php e block_simplehtml.php necessitam do bloco de início. Foi possível descobrir o problema pelas mensagens de depuração do Moodle e pela comparação com o exemplo de código de um bloco básico (11).

A documentação foi atualizada por funcionário da empresa Blackboard.com. Isso levanta suspeitas sobre a criação de uma linha de produtos, que posiciona o Moodle como uma forma de inibir a formação de empresas concorrentes. A documentação é um hipertexto com edição colaborativa, mas a página contém comentários abertos desde 2011 e parece ser alterada por funcionários, em oposição à contribuição de voluntários.

A omissão da configuração da depuração no Moodle, da instalação de blocos e do bloco de início em PHP foram os maiores problemas. Essas incorreções possivelmente atrapalhariam um usuário iniciante, que é o público alvo da documentação.


Alguns dos trechos da documentação que causaram problemas:

- "The guide is written as an interactive course " interativo? como assim? Tutorial, prático, mas iterativo?
- "little experience with Moodle or programming" ? explicar com mais detalhes os passos da configuração (DEBUG Mode, Inserir bloco, instalar bloco).
- "because the main guide has", "the guide" -> this guide? parece indicar outro texto.
- "it will always start with a slash." -> indicar relativo ao <MOODLE DIR>/blocks. Não vi isso no texto.
- "just four PHP files." -> citar quais são.
- "block called 'simplehtml'" -> usar newblock do template.
- member variables that need instantiating.  -> initializing 
- (ie, your applicable_formats function (discussed later) has 'my' set to false.) t -> false?
- In this very basic example, we only want to set  -> discuta em Eye Candy. Evitar indicar outra seções e antecipar problemas que ainda não são relevantes, este é um tutorial. Manter apenas um fluxo de informação.
- Indicar documentação de 'My Moodle page
- se vai mostrar um arquivo, mostre-o completo! block_simplehtml.php
- Indicar o uso de prefixos em identificadores.
- Prior to Moodle 2.0, -> desenvolvedores novos não se beneficiam da comparação.
- First of all, there is a check -> explicar primeiro, depois pedir para criar o bloco
- lazy instantiating? block speak?

#Ativos

Michael de Raadt SimpleClock

Vencislav Dzhambazov AJAX Calendar With Clock, substitui o calendário do Moodle.

Faltaria um SimpleClock com CSS3

https://tracker.moodle.org/browse/CONTRIB-2356
em 2010 Ian Wild 

Alastair Hole Moodle Javascript Cookbook, exemplo de relógio


# Buscas

"javascript moodle" (Google):

"javascript clock" (Google):

"no javascript clock" (Google):

"without javascript clock" (Google):

"git moodle how to" (Google):

"git link symbolic" (Google):

"soda moodle blocks" (Google):


"javascript clock moodle"

# Referências

1 http://dev.moodle.org/course/view.php?id=2

2 http://docs.moodle.org/dev/Blocks

3 http://docs.moodle.org/24/en/Git_for_Administrators

4 http://docs.moodle.org/dev/Git_for_developers

5 http://git-scm.com/book/en/

6 http://www.nathankowald.com/blog/2012/06/using-git-with-moodle/

7 http://stackoverflow.com/questions/954560/what-does-git-do-to-files-that-are-a-symbolic-link

8 http://docs.moodle.org/dev/JavaScript_guidelines

9 http://aprilzero.com/

10 http://drupal.org/project/jstimer

11 https://github.com/danielneis/moodle-block_newblock

https://moodle.org/plugins/view.php?plugin=block_simple_clock

https://moodle.org/plugins/view.php?plugin=block_calendar_month

http://www.packtpub.com/article/enhancing-page-elements-with-moodle-javascript
