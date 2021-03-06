Nervous-bulldozer

marco.mangan@gmail.com

mflashbr@gmail.com

abril de 2013


Introdução
==========
O projeto Nervous Bulldozer é uma investigação sobre o desenvolvimento de extensões para o sistema Moodle.
A principal extensão prevista é a integração do código do Sistema de Alocação de Recursos Computacionais (OpenSARC).

O repositório do projeto está no GitHub (http://mflash.github.io/nervous-bulldozer/). 
No momento, não há apoio ou patrocínio, o que permite maior liberdade para tomar decisões e um ritmo de 
trabalho menor. 

No futuro, essa situação pode mudar, sendo a PUCRS a principal candidata a fornecer patrocínio. 
A investigação permite obter experiência na plataforma Moodle e gerar um contexto para orientação de 
trabalhos de conclusão e projetos de pesquisa.

O esforço para iniciar o desenvolvimento na plataforma Moodle é alto. Uma estratégia de reutilização de 
software planejada deve ser utilizada para reduzir o custo, reduzir erros e aumentar a produtividade da 
equipe do projeto.
Inicialmente, adotaremos o conceito de linha de produtos. A estratégia é identificar ativos e planejar 
diferentes produtos que possam compartilhar esse ativos.

Linha de Produtos
=================

Dentro da plataforma Moodle, aplicada em disciplinas de semestres iniciais da FACIN e FENG, podemos identificar: 
(a) um domínio de aplicação que trata da administração do processo de ensino e aprendizado e 
(b) outro domínio que trata do processo de ensino e aprendizado de programação de computadores para iniciantes.

No primeiro domínio, o principal ativo disponível é o OpenSARC. Houve uma investigação da integração entre o Moodle e 
o OpenSARC (KUAMOTO, SILVEIRA JUNIOR e MANGAN, 2012; KUAMOTO e SILVEIRA JUNIOR, 2012) que acabou por indicar que 
os dois sistemas apresentam componentes comuns: autenticação e autorização, cadastros de usuários, cadastros de turmas e disciplina e agendas. 

A investigação indica que seria possível transferir os ativos exclusivos do OpenSARC para a plataforma Moodle. São ativos exclusivos: cadastro de recursos e cadastro de alocações de recursos.
A reescrita do OpenSARC como módulo do Moodle amplia a base potencial de usuários, evita a sobreposição dos sistemas
e oferece a oportunidade de refatorar e atualizar a implementação do OpenSARC.

A rotina de cadastro de turmas e disciplinas realizada com o apoio do SPA seria, provavelmente alterada. As turmas e disciplinas seriam cadastradas diretamente no Moodle.

No segundo domínio, os principais ativos são: MOSS, BlueJ, Eclipse e módulos de Laboratório de Avaliação e
Tarefas do Moodle. O aprendizado da programação demanda prática e existe um potencial para integração de 
ambientes de programação e também para a avaliação automática e semi-automática de exercícios.

A avaliação automática de exercícios é utilizada em concursos de programação e a verificação de 
similaridade de código serve para: (a) reduzir fraudes e plágio quando compara código entre submissões de 
alunos e (b) avaliar a qualidade do código, quando compara código do professor e de alunos.

Os sistemas desenvolvidos por terceiros são outra fonte de ativos. O Moodle.org indica a existência de 
mais de 50 "Moodle partners" e mais de 400 módulos, desenvolvidos pelo Moodle.org e pelos parceiros.

O Moodle possui duas identidades distintas: (a) uma comunidade de professores e desenvolvedores em software livre (Moodle.org) e (b) uma associação de empresas privadas (Moodle.com). É provável que os ativos da segunda identidade não estejam disponíveis. Na primeira identidade, os ativos estão registrados com a licença GPL. A GPL impede o desenvolvimento de sistemas derivados com código fechado. Para contribuir (registrar) um plugin é necessário adotar a GPL.


Trabalhos Relacionados
======================

Experências anteriores (CHARCZUK e SILVA, 2007; MAZONI e ZANLUCHI,2009) indicaram que a integração
com o Moodle é um fator de risco no desenvolvimento de trabalhos de conclusão de curso. O mesmo acontece com
a integração com outros sistemas, como o Eclipse IDE ou o Google Calendar. O principal problema com a integração
com o Moodle esta na fragmentação da documentação, por conta de versões sucessivas da plataforma. Existe a dúvida 
constante se estamos desenvolvendo do "jeito certo".

Fraga e Giraffa (2008) indicam a existência de normas e de um padrão de desenvolvimento para o Moodle e um
"relatório de cuidados e requisitos necessários para programação/adaptação de funcionalidades" utilizados
pelo Núcleo de Informática da PUCRS Virtual. Porfiro (2007) relata a experiência de desenvolvimento de
um módulo no contexto de um trabalho de conclusão. 

Uma arquitetura modular é adotada em vários sistemas, por exemplo, no Eclipse IDE e no Linux. O desenvolvimento no Moodle, por mais interessante e relevante, não apresenta contribuições à Engenharia de Software. A  complexidade do desenvolvimento relatada em Fraga e Giraffa (2008) e Porfiro (2007) resulta, provavelmente, de falta de formação específica em desenvolvimento de software e de experiência no desenvolvimento no contexto de outros sistemas modulares. O mesmo acontece em relação às atividades, aos papéis e aos artefatos que constam na documentação do Moodle. O Moodle adapta e adota práticas normais no desenvolvimento de software. 


Módulos para Administração
==========================

OpenSARC no Moodle
--------------

O OpenSARC é utilizado para aulas presenciais e semi-presenciais. O sistema inclui planejamento de aulas e 
alocação de recursos. O Moodle é utilizado também em EAD, neste caso, os recursos alocados seriam 
diferentes e, talvez, apenas tarefas síncronas e de avaliação presencial utilizem os recursos do OpenSARC.
Em EAD, os recursos incluem conexão de satélite, salas remotas, salas de videoconferência, salas 
presenciais para para avaliação e bancas de trabalho de conclusão. Os recursos atualmente controlados 
pelo OpenSARC incluem laboratórios, projetores e computadores portáteis.

O OpenSARC seria integrado como (a) uma ferramenta administrativa (http://docs.moodle.org/dev/Admin_tools) ou (b) como uma aplicação com apresentação independente, porém com compartilhamento do banco de dados e das bibliotecas do Moodle. A vantagem da primeira opção é aproveitar as facilidades da interface de usuário do Moodle, simplicidade de instalação e fornecer uma interface compatível com os demais módulos do Moodle.

### Ferramenta Administrativa
No menu de Administração do Moodle seriam acrescentados: (a) recursos,  (b) horários, (c) alocação e (d) distribuição de recursos. Um segundo módulo permitiria ao professor consultar e alterar alocação de recursos.

Chamada virtual
---------------
- impressão de caderno (ex.: planilha no Excel utilizada por alguns professores da FACIN)
- integração com iOS, Android para chamada em sala presencial
- avaliação de contribuição em salas virtuais e entrega de trabalhos

Gravação de aulas
-----------------
- ver produto da Adobe e Camtasia

Área Moodle para TCC
--------------------
- automatizar fluxo de trabalho
- detectar plágio
- alocar salas para bancas
- alocar orientadores, revisores
- emitir alertas sobre prazos ANTES que vençam
- registrar presença em aulas
- apresentar regimento/normas em formato organizado e que permita comentários: ex. manuais do MySQL, blogs

Relógio PUCRS
-------------
- apresentar codificação de dia da semana e horário da PUCRS


Módulos para Programação de Computadores
========================================

Auto-correção de exercícios
---------------------------
- testes unitários criados pelo professor
- cucumber para especificação

Correção de código fonte
------------------------
- listas pré-definidas de erros mais comuns
- verificação de padrões de codificação

Verificação de similaridade
---------------------------
- fontes não citadas na Internet
- cópia entre alunos
- erros de sintaxe e ortografia (ex.: variável maim(), int rais; em mais de um programa entregue)
- variações nos valores dos enunciados  (ex.: cada enunciado inclui dados variáveis: valores de entrada e constantes, cada aluno recebe uma versão diferente)

Maratona de programação
-----------------------
- Cada aluno recebe um exercício diferente. As respostas e comentários ficam em um fórum.

http://www.packtpub.com/moodle-1-9-testing-and-assessment/book

Badges
--------
- Indicar as competências demonstradas nos exercícios. Por exemplo, "margem esquerda", "nomes de variáveis".
- Ver 4square e openbadges
- https://moodle.org/mod/forum/discuss.php?d=183337
- http://www.scoop.it/t/moodle-and-mahara/p/2097950220/gamification-of-learning-via-moodle
- http://www.iteachwithmoodle.com/tag/gamification/
- http://englishsafari.org/?p=102
- http://drcheckers.wordpress.com/tag/gamification/
- http://digiteacher.wordpress.com/category/gamification/
- https://github.com/drcheckers/moodle-block_badger
- alunos do prof. Julio Machado estão iniciado TCC sobre o assunto em 2013/1

Módulos Relacionados
====================

SIM-Plagiarism
https://moodle.org/plugins/view.php?plugin=assignment_uploadcode

Moodle plagiarism plugins
https://moodle.org/plugins/browse.php?list=category&id=35

Virtual Programming Lab
http://vpl.dis.ulpgc.es

Moodle Workshop Module
http://docs.moodle.org/23/en/Workshop_module

Instalado no Moodle PUCRS como "Laboratório de Avaliação".  Já foi utilizado na Esp. Jogos para avaliação
de monografias - funciona bem.

Produtos Relacionados
====

Planbook - Mac Store App

Integrações já existentes
=========================

JOOMLA + Moodle => Joomdle
http://www.joomdle.com/en/ - Investigar como se dá a integração de CMS e LMS

Desenvolvimento no Moodle
=========================

Instalação do Moodle
--------------------

BitNami com PostGRESQL e Moodle4Mac MAMP com MySQL. Alterar configurações de segurança e privacidade.
Instalar na pasta Applications do usuário não funciona. Dois usuários: admin e test. Associar test como professor em curso Moodle4Mac (About).

Transferir SODA como zip a partir do gitHub. Copiar soda-master como soda para /Applications/MAMP/htdocs/moodle24/local.

Nas notificações do administrador do Moodle, localizar o addon e solicitar a atualização da base.
Em plugins, plugins overview, consta soda como local plugin.

Validação
---------

http://docs.moodle.org/dev/Plugin_validation

GPL version 2+ for Moodle 1.x software
**GPL version 3+ for Moodle 2.x**

https://moodle.org/plugins/registerplugin.php
http://docs.moodle.org/dev/Plugins

Moodle.org e Moodle.com.

Moodle e SCORM.

Segundo o Moodle Dev Overview, o Nervous Bulldozer seria um Moodle Partner.
Versão 2.0 mudou a estrutura do Moodle.
Livros da Amazon tratam do desenvolvimento no Moodle 1.9.

SODA MVC com Moodle (qual versão?)
http://tech.solin.eu/doku.php?id=moodle:using_soda_to_create_new_moodle_modules

Existe um curso no Moodle.org. http://dev.moodle.org/course/view.php?id=2
Necessita login em Moodle.org ou senha de visitante.

Desenvolvimento com Frameworks
------------------------------

Mangan: MVC, RoR -like

http://www.phpframeworks.com/

http://cakephp.org/

http://ellislab.com/codeigniter

Dúvida sobre a interferência entre o código do Moodle e o de outros frameworks.

Moodle usa:

- PHP puro, orientado a objetos
- YUI3 (Yahoo User Interface) para componentes de interface com usuário
- Outras possibilidades: jQuery (já integrado, funciona sem problemaS)

**Dúvida: possível integrar com outros frameworks?**


D2L
Blackboard

Novo ambiante com tecnologia atual.


Análise de Frameworks para PHP
-------------------------------

Critérios:
- atividade recente: atividade nos últimos 12 meses
- software aberto: pode ser inspecionado e alterado
- PHP 5: orientado a objetos
- licença GPL: compatível com licença do Moodle
- organização .org: evita aquisição de produto
- documentação:
- arquitetura MVC: na lista abaixo, todos são.
- influência de Rails:
- testes
- scaffolding

Zend
Fevereiro 2013
Open source
PHP5
New BSD
framework.zend.com

CakePHP
Abril de 2013
Open source
PHP
MIT
cakephp.org

CodeIgniter
Outubro de 2012
Open source
PHP
OSL
codeigniter.com

Doo

Fat-Free
Março de 2013
GPL
PHP5
GPL
fatfree.sf.net

Kohana (derivado do CodeIgniter)

http://www.developer.com/lang/php/article.php/3878476/Top-10-Lightweight-Frameworks-for-PHP-Development.htm

http://en.wikipedia.org/wiki/Comparison_of_web_application_frameworks#PHP

Alguns frameworks são criados por dissidências. O código do framework pode ser pequeno (aprox. 100 kb). Alguns serviços do framework se sobrepõe aos do Moodle: autenticação, persistência. O Moodle já é um framework. Sinatra e Rails são incluências de Ruby no PHP. Joomla, Fat-Free e AppFlower utilizam a mesma licença do Moodle. Não sei da compatibilidade entre licenças.

Recomendação: comparar o código de frameworks comerciais com o SODA MVC.


Cronograma
==========

- estudo de php
- estudo do Dev Moodle
- recuperar código de plugins similares
- recuperar trabalho da Mika/Paulo
- dividir o OpenSARC em componentes: algoritmo de carga, cadastros, reservar, alteração, calendários.
- identificar componentes do OpenSARC existentes no Moodle

Desdobramentos
==============
- Horas de pesquisa na PUCRS: FACIN, PUCRS Virtual, LAPREN.
- Centro de Pesquisa em Ensino de Programação (similar ao da Física, ver anuário da PUCRS)
- Publicação no FISL e Moodle Moot em 2014
- Customização para outras instituições e faculdades
- Orientações de TCC
- Livro sobre como desenvolver no Moodle
- Cursos sobre como desenvolver no Moodle
- Publicação em Engenharia de Software e Educação
- Empresa/Organização privada sobre consultoria com Moodle e hospedagem de Moodle
- Orientação de bolsistas de IC, projetos FAPERGS etc
- Curso em EAD da PUCRS Virtual para ensino de programação


Consultas
=========
As consultas utilizadas em pesquisas são armazenadas neste capítulo para evitar buscas redundantes e para permitir a atualização periódica de resultados e revisão.

- "how to create a Moodle plugin" (Google): SODA
- "learn to program PHP" (Google): PHP Manual
- "moodle plugin pucrs" (Google): Fraga e Giraffa (2008), Porfiro (2007).
- "Uma ferramenta para gestão de grupos por perfil de alunos no ambiente Moodle" (Google): citações para Porfiro (2007).
- "moodle partners" (Google): partners não podem ser ONGs e Universidades.
- "moodle mac" (Google): 
- "admin tool" (Moodle.org): 
- "php mvc framework" (Google):
- "scorm" (Google):
- "scorm moodle" (Google):
- "codeigniter" (Alternativeto.net): Symfony, Symfony2, Agile Toolkit, Django, Yii, Kohana, Fat-Free phunction, fuel

Referências
===========

SODA http://tech.solin.eu/doku.php?id=moodle:using_soda_to_create_new_moodle_modules

OpenSARC https://github.com/mflash/opensarc

NERVOUS BULLDOZER http://mflash.github.io/nervous-bulldozer/

MOODLE Introduction to Moodle Programming. http://dev.moodle.org/course/view.php?id=2

MOODLE Core APIs. http://docs.moodle.org/dev/Core_APIs

MOODLE Desenvolvimento. http://docs.moodle.org/dev/Developer_documentation?rdfrom=http%3A%2F%2Fdocs.moodle.org%2F24%2Fen%2Findex.php%3Ftitle%3DDevelopment%26redirect%3Dno

MOODLE Dev Overview http://docs.moodle.org/dev/Overview

Mika Kuamoto ; Paulo Silveira Junior ; MANGAN, M. A. S. . ISMA um Plug-in Moodle de Integração com Sistemas de Planejamento Acadêmico e Agendas Utilizando XML-RPC. In: MoodleMoot Brasil 2012, 2012, São Paulo. MoodleMoot Brasil 2012, 2012.

Mika Kuamoto ; Paulo Silveira Junior. ISMA: Um Plug-in Moodle de Integração com Sistemas de Planejamento Acadêmico e Agendas Utilizando XML-RPC. 2012. Trabalho de Conclusão de Curso. (Graduação em Sistemas de Informação) - Pontifícia Universidade Católica do Rio Grande do Sul. Orientador: Marco Aurelio Souza Mangan.

Luís Felipe Mazoni; Raphael Bernardi Zanluchi. Caderno Virtual de Acompanhamento de Cursos em Plataforma Tablet. 2011. Trabalho de Conclusão de Curso. (Graduação em Ciência da Computação) - Pontifícia Universidade Católica do Rio Grande do Sul. Orientador: Marco Aurelio Souza Mangan.

J. B. Charczuk/T. B. Silva. Ferramenta de comunicação síncrona e assíncrona baseada em Web 2.0 e integrada a um ambiente de Educação a Distância. 2007. Trabalho de Conclusão de Curso. (Graduação em Bacharelado em Ciência da Computação) - Pontifícia Universidade Católica do Rio Grande do Sul. Orientador: Marco Aurelio Souza Mangan.

PHP Manual http://www.php.net/manual/en/

Fraga e Giraffa. http://www.pucrs.br/research/salao/2008-IXSalaoIC/index_files/main_files/trabalhos_sic/ciencias_exatas/ciencia_computacao/61826.pdf

Porfiro, R. M. “Uma ferramenta para gestão de grupos por perfil de alunos no ambiente Moodle”. Trabalho
de Conclusão. Faculdade de Informática da Pontifícia Universidade Católica do Rio Grande do Sul. Porto
Alegre: 2007. http://pt.scribd.com/doc/4605923/Estudando-o-moodle

Gabriel Reis de Souza; Vanderson Soares Porto. "Criação de plugins para a plataforma Moodle" 2010. 
Universidade Católica de Brasília. Orientador: Wilson Carlos Hartmann. http://pt.scribd.com/doc/35616639/Criacao-de-Modulos-para-o-Moodle

ADOBE LMS. http://www.adobe.com/resources/elearning/lms_integration.html

Bertagnolli. Formação docente aliada aos novos recursos das TICs

MOODLE.COM http://moodle.com/partners/about/

SOLIN http://tech.solin.eu/doku.php?id=moodle:moodle

Moodle 4 Mac MAMP http://download.moodle.org/macosx/
