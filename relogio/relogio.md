Relógio

marco.mangan@gmail.com

# Introdução

O relógio é um componente simples, para testes de integração com o Moodle 2.0 utilizando o framework SODA. O componente apresenta hora e minuto conforme o relógio do computador servidor.

A modelagem deste componente iniciou em 2007 e foi retomada em 2009. A lista de requisitos foi desenvolvida como exercício na disciplina de Modelagem de Sistemas.

O módulo tem que funcionar, mesmo sem JavaScript, segundo a orientação do Moodle.org aos desenvolvedores. Para apresentar o horário correto, o componente necessita de um script no lado cliente ou outra forma de animação. O relógio deixa de ser atualizado em tempo real, caso o navegador não permita o uso de JavaScript ou outra forma de animação, como CSS3. 


# Requisitos

- R1	Considerar como referência o horário do servidor na PUCRS.
- R2	O horário apresentado é o mesmo que regula a entrega de trabalhos via Moodle.
- R3	Apresentar o código alfanumérico de dias da semana da PUCRS correspondente ao horário.
- R4	Não sobrecarregar o processamento no computador cliente.
- R5	Não sobrecarregar o processamento no computador servidor.
- R6	Não sobrecarregar a conexão de rede.
- R7	Sempre que possível, operar sem a necessidade de conexão de rede.
- R8	Tratar eventos do ambiente Moodle (ex. troca de tela).
- R9	Tratar eventos do navegador da Web (ex. navegação, atualização).
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


#Desenvolvimento

O componente será criada com o SODA. A pasta utilizada na sincronização com o repositório será associada com uma pasta do servidor através de um atalho. 

A primeira versão do componente deve apresentar um bloco com a data e hora do servidor no momento da criação do bloco. 

# Buscas

"javascript moodle" (Google):

"javascript clock" (Google):

"no javascript clock" (Google):

"without javascript clock" (Google):


# Referências

http://docs.moodle.org/dev/JavaScript_guidelines

http://aprilzero.com/

http://drupal.org/project/jstimer
