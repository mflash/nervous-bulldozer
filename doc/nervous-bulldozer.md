Nervous-bulldozer

marco.mangan@gmail.com

mflashbr@gmail.com


Introdução
==========
O projeto Nervous Bulldozer é uma investigação sobre o desenvolvimento de extensões para o sistema Moodle. A principal extensão prevista é a integração do código do Sistema de Alocação de Recursos Computacionais (SARC).

O repositório do projeto está no GitHub (http://mflash.github.io/nervous-bulldozer/). No momento, não há apoio ou patrocínio, o que permite maior liberdade para tomar decisões e um ritmo de trabalho menor. 

No futuro, essa situação pode mudar, sendo a PUCRS a principal candidata a fornecer patrocínio. A investigação permite obter experiência na plataforma Moodle e gerar um contexto para orientação de trabalhos de conclusão e projetos de pesquisa.

O esforço para iniciar o desenvolvimento na plataforma Moodle é alto. Uma estratégia de reutilização de software planejada deve ser utilizada para reduzir o custo, reduzir erros e aumentar a produtividade da equipe do projeto.
Inicialmente, adotaremos o conceito de linha de produtos. A estratégia é identificar ativos e planejar diferentes produtos que possam compartilhar esse ativos.

Linha de Produtos
=================

Dentro da plataforma Moodle, aplicada em disciplinas de semestres iniciais da FACIN e FENG, podemos identificar: (a) um domínio de aplicação que trata da administração do processo de ensino e aprendizado e (b) outro domínio que trata do processo de ensino e aprendizado de programação de computadores para iniciantes.

No primeiro domínio, o principal ativo disponível é o SARC. Houve uma investigação da integração entre o Moodle e o SARC (KUAMOTO, SILVEIRA JUNIOR e MANGAN, 2012; KUAMOTO e SILVEIRA JUNIOR, 2012) que acabou por indicar que os dois sistemas apresentam componentes comuns: autenticação e autorização, cadastros de usuários e agendas. 

A investigação indica que seria possível transferir os ativos exclusivos do SARC para a plataforma Moodle. A reescrita do SARC como módulo do Moodle amplia a base potencial de usuários, evita a sobreposição dos sistemas e oferece a oportunidade de refatorar e atualizar a implementação do SARC.

No segundo domínio, o principal ativo são: MOSS, BlueJ, Eclipse e módulos de Laboratório de Avaliação e Tarefas do Moodle. O aprendizado da programação demanda prática e existe um potencial para integração de ambientes de programação e também para a avaliação automática e semi-automática de exercícios.

A avaliação automática de exercícios é utilizada em concursos de programação e a verificação de similaridade de código serve para: (a) reduzir fraudes e plágio quando compara código entre submissões de alunos e (b) avaliar a qualidade do código, quando compara código do professor e de alunos.

Os sistemas desenvolvidos por terceiros são outra fonte de ativos. O Moodle.org indica a existência de mais de 50 "Moodle partners" e mais de 100 módulos, desenvolvidos pelo Moodle.org e pelos parceiros.

Experências anteriores (Charczuk e Silva, 2007; Mazoni e Zanluchi,2009) indicaram que a integração
com o Moodle é um fator de risco no desenvolvimento de trabalhos de conclusão de curso. O mesmo acontece com
a integração com outros sistemas, como o Eclipse IDE ou o Google Calendar. O principal problema com a integração
com o Moodle esta na fragmentação da documentação, por conta de versões sucessivas da plataforma. Existe a dúvida 
constante se estamos desenvolvendo do "jeito certo".

Fraga e Giraffa (2008) indicam a existência de normas e de um padrão de desenvolvimento para o Moodle e um
"relatório de cuidados e requisitos necessários para programação/adaptação de funcionalidades" utilizados
pelo Núcleo de Informática da PUCRS Virtual. Porfiro (2007)

Módulos para Administração
==========================

SARC no Moodle
--------------

O SARC é utilizado para aulas presenciais e semi-presenciais. O sistema inclui planejamento de aulas e alocação de recursos. O Moodle é utilizado também em EAD, neste caso, os recursos alocados seriam diferentes e, talvez, apenas tarefas síncronas e de avaliação presencial utilizem os recursos do SARC.
Em EAD, os recursos incluem conexão de satélite, salas remotas, salas de videoconferência, salas presenciais para para avaliação e bancas de trabalho de conclusão. Os recursos atualmente controlados pelo SARC incluem laboratórios, projetores e computadores portáteis.

Chamada virtual
---------------
- impressão de caderno (ex.: planilha no Excel
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
- apresentar regimento em formato organizado e que permita comentários: ex. manuais do MySQL, blogs

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
Cada aluno recebe um exercício diferente. As respostas e comentários ficam em um fórum.


Módulos Relacionados
====================

SIM-Plagiarism
https://moodle.org/plugins/view.php?plugin=assignment_uploadcode

http://vpl.dis.ulpgc.es

Já existe algo que pode ser usado:

http://docs.moodle.org/23/en/Workshop_module

Instalado no nosso como "Laboratório de Avaliação".

Usei na Especialização, funciona bem.


JOOMLA é o CMS...
Vi que tem um módulo para integrar o Moodle com Joomla (Joomdle), então por que é tão impossível
integrar com outros?
Mudando de assunto
https://moodle.org/plugins/browse.php?list=category&id=35

Desenvolvimento no Moodle
=========================

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

Cohen
Não necessariamente... O Moodle não tem um "framework", ele usa um PHP bem padrão, a maior
parte só lê o config e algumas libs próprias. A maior integração que tem é com o YUI3 da Yahoo,
para a interface com o usuário. Mas como já te comentei, usei jQuery sem problemas.


Marco Mangan wrote:
Pois é, monstro, foi isso que falei...
Frameworks não se dão bem, por causa do fluxo de controle!

é que o que queremos é bem mais que um plugin
eu diria que não dá para classificar nem como módulo para o Moodle
não sei bem ao certo como integrar do jeito "correto"
se é que tem um!

por exemplo, para o sistema de pedido de áreas, que a secretaria acessa e cria as áreas de cada disciplina
utilizamos apenas a API disponibilizada pelo Moodle

e parte da YUI


Cronograma
==========

- estudo de php
- estudo do Dev Moodle
- recuperar código de plugins similares
- recuperar trabalho da Mika/Paulo
- dividir o SARC em componentes: algoritmo de carga, cadastros, reservar, alteração, calendários.
- identificar componentes do SARC existentes no Moodle

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
As consulta utilizadas em pesquisas são armazenadas neste capítulo para evitar buscas redundantes e para permitir a atualização periódica de resultados e revisão.
- "how to create a Moodle plugin" (Google): SODA
- "learn to program PHP" (Google): PHP Manual
- "moodle plugin pucrs" (Google): Fraga e Giraffa (2008), Porfiro (2007).
- "Uma ferramenta para gestão de grupos por perfil de alunos no ambiente Moodle" (Google):

Referências
===========
SODA http://tech.solin.eu/doku.php?id=moodle:using_soda_to_create_new_moodle_modules

SARC 

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
Alegre: 2007. pp 23-34. http://pt.scribd.com/doc/4605923/Estudando-o-moodle
