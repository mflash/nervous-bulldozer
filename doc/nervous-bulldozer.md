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

Dentro da plataforma Moodle, podemos identificar: (a) um domínio de aplicação que trata da administração do processo de ensino e aprendizado e (b) outro domínio que trata do processo de ensino e aprendizado de programação de computadores para iniciantes.

No primeiro domínio, o principal ativo disponível é o SARC. Houve uma investigação da integração entre o Moodle e o SARC (KUAMOTO, SILVEIRA JUNIOR e MANGAN, 2012; KUAMOTO e SILVEIRA JUNIOR, 2012) que acabou por indicar que os dois sistemas apresentam componentes comuns: autenticação e autorização, cadastros de usuários e agendas. 

A investigação indica que seria possível transferir os ativos exclusivos do SARC para a plataforma Moodle. A reescrita do SARC como módulo do Moodle amplia a base potencial de usuários, evita a sobreposição dos sistemas e oferece a oportunidade de refatorar e atualizar a implementação do SARC.

No segundo domínio, o principal ativo são: MOSS, BlueJ, Eclipse e módulos de Laboratório de Avaliação e Tarefas do Moodle. O aprendizado da programação demanda prática e existe um potencial para integração de ambientes de programação e também para a avaliação automática e semi-automática de exercícios.

A avaliação automática de exercícios é utilizada em concursos de programação e a verificação de similaridade de código serve para: (a) reduzir fraudes e plágio quando compara código entre submissões de alunos e (b) avaliar a qualidade do código, quando compara código do professor e de alunos.

SARC no Moodle:
Recursos
- EAD: satélite, salas remotas, videoconferência, salas para avaliação, bancas (ex.: agendamento na PUCRS Virtual)
- presencial e semi-presencial: salas, laboratórios, projetores

Chamada virtual:
- impressão de caderno (ex.: planilha no Excel
- integração com iOS, Android para chamada em sala presencial
- avaliação de contribuição em salas virtuais e entrega de trabalhos

Gravação de aulas
- ver produto da Adobe e Camtasia

Área Moodle para TCC
- automatizar fluxo de trabalho
- detectar plágio
- alocar salas para bancas
- alocar orientadores, revisores
- emitir alertas sobre prazos ANTES que vençam
- registrar presença em aulas
- apresentar regimento em formato organizado e que permita comentários: ex. manuais do MySQL, blogs

Correção de exercícios de programação básica
- testes unitários criados pelo professor
- cucumber para especificação
- listas prédefinidas de erros mais comuns
- verificação de padrões de codificação
- Java e C
- destaque de sintaxe

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

Versão 2.0 mudou a estrutura do Moodle.
Livros da Amazon tratam do desenvolvimento no Moodle 1.9.

Documentação online
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

Referências
===========
- SARC
- NERVOUS BULLDOZER
- MOODLE Desenvolvimento
- Mika Kuamoto ; Paulo Silveira Junior ; MANGAN, M. A. S. . ISMA um Plug-in Moodle de Integração com Sistemas de Planejamento Acadêmico e Agendas Utilizando XML-RPC. In: MoodleMoot Brasil 2012, 2012, São Paulo. MoodleMoot Brasil 2012, 2012.
- Mika Kuamoto ; Paulo Silveira Junior. ISMA: Um Plug-in Moodle de Integração com Sistemas de Planejamento Acadêmico e Agendas Utilizando XML-RPC. 2012. Trabalho de Conclusão de Curso. (Graduação em Sistemas de Informação) - Pontifícia Universidade Católica do Rio Grande do Sul. Orientador: Marco Aurelio Souza Mangan.
