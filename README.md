# 2020.2-SPC-CAD-POSITIVO
Implementations PI-2020.2
Disciplinas:
•	ESTATÍSTICA DESCRITIVA – Prof. NANCI DE OLIVEIRA.
•	ESTRUTURA DE DADOS – Prof. EDUARDO SAKAUE.
•	FUNDAMENTOS DE GESTÃO DE TECNOLOGIA DA INFORMAÇÃO – Prof. FABIANO SABHA.
•	FUNDAMENTOS DE REDES DE COMPUTADORES – Prof. ANTONIO WELLINGTON SALLES RIOS.
•	LABORATÓRIO DE DESENVOLVIMENTO DE BANCO DE DADOS - Prof GIULIANO BERTOTTI.
•	LINGUAGEM DE PROGRAMAÇÃO II – Prof. LUCAS GONÇALVES NADALETE.
•	PROGRAMAÇÃO DE BANCO DE DADOS – Prof. JULIANA FORIN PASQUINI MARTINEZ.
Integrantes:
•	Caroline Paz de Sousa, RA: 1460281923049
•	Daniel Delgado, RA: _
•	Jessica Isri, RA: 
•	Fabio Odaguiri, RA: 1460281923008
•	Nathan ____, RA: ____
•	Wilson Amore Vieira Filho, RA: 1460281923041
{Incluir Vídeo da Entrega 01 – 27/09/2020}
Introdução:
O presente documento visa apresentar a solução tecnológica proposta pela equipe para apresentar uma aplicação que gere valor aos usuários do Cadastro Positivo, clientes da empresa SPC BRASIL.
Utilizando a base de dados do Cadastro Positivo (Lei nº 12.414/2011 c/c LC nº 166/2019), a aplicação gerará valor pelo fato de:
a)	conseguir manter seus usuários em sua plataforma, haja vista a presença de 4 concorrentes/players detentores da mesma base de dados;
b)	ser “monetizável”;
c)	conciliar-se com as características dos dados, agrupados em:
i.	geolocalização;
ii.	“Score” de Crédito;
iii.	Investigação de CPF;
iv.	Controle de Fraudes
Aqui, serão identificados e classificados o objeto, “story cards”, requisitos, proposta da solução, destacando a usabilidade e mantendo backlog.
A aplicação consiste num ambiente onde o usuário possa ter acesso aos seus dados do C.P., porém, agregando valor adicional por algum atrativo adicional.
A GUI (Graphical User Interface) ou VIEW permitirá a interação do usuário com a aplicação.
Elicitação, Story Cards e Identificação de Requisitos
Declaração do Problema.
Nossa cliente fornece dados cruciais à existência da própria Economia, vez que servem para a concessão ou negação de crédito. 
A partir de uma base de dados compartilhada com outros três concorrentes – o Cadastro Positivo, seus usuários podem saber como estão posicionados no mercado para pedir crédito ou, qual o risco de conceder-se crédito a quem lhes peça.
Os referidos dados são capturados de diversas fontes públicas e de caráter público, sobre histórico de crédito, definido na lei como “conjunto de dados financeiros e de pagamentos, relativos às operações de crédito e obrigações de pagamento adimplidas ou em andamento por pessoa natural ou jurídica.”
Nesse passo, nossa cliente busca a distinção da concorrência através de diferenciais para tais usuários.
A aplicação pode gerar valor tanto para quem pede, quanto para quem dá o crédito, v.g. no ato de uma compra parcelada, o comprador é o requerente; o vendedor é o concedente. Destaque-se que os usuários podem ser pessoas físicas ou jurídicas, eis que ambas podem estar em qualquer das posições.
Por fim, note-se que há uma massa de pessoas que raramente constava na base de dados, por não participar de aquisições suscetíveis às consultas de crédito: os chamados “desbancarizados”. Sem conta bancária, são pessoas que participam anonimamente da Macroeconomia, por terem renda extremamente reduzida e utilizarem dinheiro em espécie (sem cartão de crédito, sem conta bancária, sem fintech de meios de pagamento eletrônico, sem salário formal). Agora, com a inserção de dados de contas de serviços públicos (utilities), pessoas cadastradas em empresas de energia elétrica, água, gás, telefonia dentre outros constam na referida base de dados.
Logo, a aplicação deverá trabalhar seus dados e gerar informação que, por sua vez, há de transformar-se em conhecimento, aplicável no cotidiano dos usuários.
Nossa cliente declarou que a mera apresentação de dados na tela da aplicação não será considerada geração de valor; pode-se utilizar outras fontes públicas de dados; Ainda não houve o fornecimento de amostra da base de dados (dataset) e o primeiro passo é problematizar e sugerir soluções.
Questões da Equipe.
Diante deste cenário, são perguntas plausíveis:
a)	O usuário que paga contas e parcelas maiores pode ser negativado por contas menores?
b)	O chamado “bom pagador” que está num mal momento econômico, com estabilidade financeira, não mereceria uma classificação melhor do que aquele que já perdeu os meios de recuperar-se?
c)	A massa de pessoas desbancarizadas é economicamente significativa?
d)	O desbancarizado pode comprar parcelado?
e)	Quais recortes estatísticos agregam valor aos usuários?
f)	Quais ferramentas de Ciência de Dados, Aprendizado de Máquina ou Inteligência Artificial podem transformar os dados?
g)	Quais dados/débitos são considerados para o cálculo do “Score”, investigação de CPF e Prevenção de Fraudes?
h)	É possível automatizar consultar do CPF do indivíduo em bancos de dados tais quais CAGED, INSS e outros órgãos ou entes?
Brainstorming.
Soluções parecem ser bidirecionais, eis que podem ser consumidas tanto pelo concedente quanto pelo requerente.
Lista de ideias apresentadas pela equipe (o que pode ser utilizado):
- Dados brutos: Nome, CPF, Endereço, local de consumo (georreferenciado e endereço), data, hora, valor, nome e ramo de negócio do estabelecimento.
- Dados históricos: histórico e frequência de consumo, horários e locais mais frequentes, tipos de consumo, quebra por categoria/período/local/valor, consumo mensal; renda presumida (somatória do quanto gasta e de quanto investe);
- Dados de contrato de trabalho (CAGED) ou de previdência social (INSS e outros órgãos ou entes públicos) (usuário está pensionista, aposentado, (des)empregado?
Lista de ideias apresentadas pela equipe (o que pode ser apresentado):
a)	Nova quebra de faixas de risco para o crédito em oposição à classificação binária:
i.	bom pagador sem negativações c/c consumo e renda altas;
ii.	bom pagador de grandes débitos com pequenas moras;
iii.	bom pagador por faixas de valores;
iv.	bom pagador que está em má fase (ver CAGED/INSS);
v.	desbancarizados que já consomem baseado em crédito informal / crediário próprio;
vi.	mal pagador c/c fonte de renda insuficiente;

b)	Serviços que podem ser oferecidos aos desbancarizados:
i.	Onde podem comprar parcelado / microcrédito (ato voluntário do comércio ou fintech dedicada – mercado: 23 milhões de pessoas*)?
ii.	Análise de risco para microcrédito;
iii.	Microcrédito/milhagens/pontos como impulso inicial no histórico de crédito;

c)	Gamificação:
i.	Classificação do usuário por:
i.i níveis de Score;
i.ii. progressão de fases;
i.iii. pontos;
i.iv. colocação do usuário num determinado grupo (Os 20 melhores);
i.v. Menu “Helper” ou Assistente com dicas para melhorar sua classificação;
i.vi. Utilizar o Score para transformá-lo e mostrar progressão no gráfico;
i.vii. Linha do tempo x gastos;

ii.	Classificação dos gastos:
ii.i. Top 10 gastos do mês (moradia, educação, alimentação, telefonia, vestuário, transporte);
ii.ii. O que estou comendo muito?

iii.	Informações Básicas: Para que serve o Score e outras funções educativas

d)	Itinerário do Consumo: Gráfico de “onde eu consumo ao longo do dia ou do mês” para requerentes e “qual o fluxo de consumidores em determinado local” para concedentes;

e)	Proposta de Negociação dos Débitos: Acompanhamento da flutuação do Score com sugestão do momento para oferecer acordo e evitar a judicialização (bilateral);

(Soluções parecem ser bidirecionais, eis que podem ser consumidas tanto pelo concedente quanto pelo requerente).
Story Cards:
•	Cadastrar Tarefa: Clicar na tela, abrir caixa de diálogo, digitar nome do projeto e, abrir caixa de diálogo com dropdown list para escolher:
o	dia inicial;
o	dia final;
o	pessoa;
o	indicar dependência com outra(s) tarefa(s).
•	Arrastar Tarefa: Ao clicar na tarefa, pode-se aumentar/diminuir o tempo e assistir as alterações dos quadrantes de controle. Quadrantes de Controle: Pela manipulação das barras de tarefas sob projetos, alterar-se-á as informações de:
o	horas alocadas por pessoa;
o	horas disponíveis por pessoa;
o	Porcentagem de ocupação;
o	Horas da equipe alocadas por dia;
o	Horas da equipe alocadas por semana;
o	Horas da equipe alocadas por mês;
o	Lista tarefa-início-pessoa-duração;
•	Código de Cores: Para melhor usabilidade e distinção das diversas informações, pessoas/dias/semanas/meses poderão sofrer alteração de cor para permitir a identificação instantâneas de sobrecarga e possibilitar mudanças pelo gestor do(s) projeto(s);
•	Métricas: Tempo x pessoas/dias/semanas/meses;
•	Deletar Tarefa: Perguntar se tem certeza e confirmar.
Especificação de Requisitos (EM ORDEM DE PRIORIDADE):
Funcionais:
•	Bloquear determinado usuário concedente;
•	Gerar Relatórios;
•	Buscar dados de outras fontes;
•	
•	Cadastrar tarefas e projetos;
•	Cadastrar colaboradores e realizar autenticação dos usuários (administrador,operador,etc);
•	Calcular as horas totais do projeto com base na carga horária das tarefas (tasks);
•	Calcular/Mostrar métricas de tempo x receita nos projetos com quantidade de horas/valor alocados em cada projeto, por dia. por semana, por mês e um "Grand Total";
•	Armazenar dados (busca-se autosalvamento e versionamento de arquivo);
•	Dispor da informação sobre prazos reais e líquidos, contemplando calendário com dias úteis, finais de semana, feriados, férias e ausências, entre outros.
•	Criar interdependência entre tarefas;
•	Manipular a GUI na forma de diagrama interativo;
•	Gerar relatórios por desenvolvedor, por período;
NOME	Cod	Descrição
Cadastro de Tarefas	R1	O sistema deve permitir inserir novos projetos e tarefas relacionadas aos mesmos
Cadastro de Colaboradores	R2	O sistema deve permitir a inserção de colaboradores e também a distribuição dos mesmos, em projetos e tarefas, baseado nas horas/recurso humanos.
Horas	R3	O sistema deve mostrar a quantidade de horas/custo alocados em cada projeto.
Cálculo de horas	R4	O sistema deve calcular as horas totais do projeto com base na carga horária das tarefas, de modo que, de acordo com situações que possam alongar ou adiantar as mesmas, os gestores tenham controle do prazo final do projeto.
Calendário	R5	O sistema deve controlar o calendário a fim de monitorar: dias úteis, finais de semana, feriados, férias, e outras ausências.
Relatórios	R6	Gerar relatórios.
Diagrama Interativo	R7	Gerar gráficos de Gantt responsivos que ao ter a barra arrastada, calcule os prazos dos projetos, para melhor controle dos gestores.
Importação	R8	O sistema poderá importar planilha (desnecessária a sua exportação).
DIAGRAMA DE CASO DE USO  
Não funcionais:
•	Dashboard visualmente agradável, colorido;
•	Web* (verificar se o usuário consumidor/requerente não ficaria mais fiel em app mobile);
•	Ciência de Dados;
•	Aprendizado de Máquina;
•	Inteligência Artificial;
•	Gerencialmente Inteligível;
•	Rodar no dispositivo
•	multiplataforma;
Proposta
A seguinte proposta visa entregar um sistema que gere diagrama interativo (Gráfico de Gantt) de controle de tarefas, projetos e carga horária de cada recurso, trazendo uma interface intuitiva e amigável ao usuário.



Visão:
Pesquisa das melhores tecnologias para o caso concreto, conjugando facilidade de desenvolvimento e estabilidade da aplicação em face da capacidade de entrega do grupo Pydevs, dentro do tempo disponível.
Usabilidade:
HEURISTICAS
•	Correspondência entre o sistema e o mundo real
O sistema possuirá uma interface intuitiva com menus e botões de ações de fácil entendimento, utilizando um nomenclatura familiar aos seus usuários. As ações tais quais exclusão ou criação de nova tarefa/projeto serão realizadas por meio de botões/opções de menu sinalizados por "deletar" ou simplesmente "X", tanto quanto "adicionar" ou "+". O calendário de acompanhamento de atividades do projeto será em português. Busca-se uma interface clique-e-arraste, induzindo os caminhos para que a utilização seja fluída.
•	Controle do usuário e liberdade
Com o sistema intuitivo, o usuário possuirá uma certa liberdade no sistema, minimizando o número de cliques e de erros, pois conseguirá identificar claramente as funcionalidades e comandos disponíveis, sem precisar decorar procedimento algum. Sendo a facilidade em identificar cada etapa do projeto e sua evolução devido o calendário de acompanhamento do projeto e as cores do gráfico de Gantt, ao acessar o sistema com capslock ligado o sistema avisará o usuário (campo de senha é CASE SENSITIVE), almeja-se que tenha autosalvamento, controle de versões, permitindo simulações (usabilidade do sistema).
•	Design estético e minimalista
Com design intuitivo o sistema exibirá informações precisas e de fácil interpretação, com calendários e gráficos de barras coloridos, ícones familiares. O sistema deve utilizar cores na construção do gráfico para melhor identificação dos projetos/tarefas/pessoas em andamento e identificação de interdependência das atividades.
•	Ajuda e documentação
A interface será intuitiva para que o usuário tenha uma melhor experiência e liberdade em usar o sistema, o sistema será de fácil usabilidade sendo opcional a leitura de manual e documentação. Para os usuários que precisam desse documento na própria plataforma poderá conter um arquivo digital para ser baixado com as instruções de utilização objetiva.
Instalação:
Após os primeiros testes com nosso código, será possível decidir entre hospedagem em um endereço para acesso por meio de um navegador ou, se será necessária a instalação local nos computadores, com arquivo executável.
A princípio, será compatível nas plataformas Windows, Linux e Mac OS.
Tecnologias e Metodologias aplicadas
•	Java
•	Java Script;
•	Oracle;
•	Método Scrum;
Entrega 01 (27 de setembro de 2020).
•	MOCKUP da aplicação, a partir das solicitações do cliente: vide arquivo "200318-Primeira-Entrega-PI-Pydevs(PDF-version-PRESS-F11).pdf"
Entrega 02 (15 de maio de 2020).
 <img align="left" width="100" height="100" src=https://user-images.githubusercontent.com/54047352/83085242-bfe5c600-a061-11ea-8aaf-9350cc7e52bd.png">

Entrega 03 (29 de maio de 2020) + BACKLOG (COM DATAS E EXPECTATIVA DE ENTREGAS ABAIXO).
Seguindo as camadas do desenvolvimento, temos:
i) VISUAL (Tela vista pelo usuário - Entrada e Saída de Dados - Entrada: Projeto, Tarefa, Data de Início, Data Final, Pessoa)
•	Quadrante 1 de 4 da Tela (GANTT-NECTO) - em desenvolvimento;
•	Quadrante 2 de 4 da Tela (GANTT-NECTO) - Entregue em 15/05/2020;
•	Quadrante 3 de 4 da Tela (GANTT-NECTO) - Entrega hoje, em 29/05/2020, mostra: Tarefa, Data de Início, PEssoa, Duração;
•	Quadrante 4 de 4 da Tela (GANTT-NECTO)- em desenvolvimento;
ii) CONTROLER - em desenvolvimento;
iii) MODEL - Entrega hoje, em 29/05/2020 ; (a partir de dados obtidos da camada VISUAL, serão processados novos dados: Duração, % de ocupação da pessoa + do dia + da semana + mês, horas totais da pessoa, horas disponíveis);
iv) BANCO DE DADOS - em desenvolvimento;
(CLIQUE NO VIDEO ABAIXO E ASSISTA A APRESENTAÇÃO)

Entrega 04 (12 de junho de 2020).
•	Quadrante 1 de 4 da Tela (GANTT-NECTO);
•	BANCO DE DADOS;
•	Tela de Login;
Entrega 05 (26 de junho de 2020).
•	Quadrante 4 de 4 da Tela (GANTT-NECTO);
•	MODEL;
•	Exclusão de Tarefas, Projetos, Usuários;
Entrega 06 (10 de juLho de 2020).
•	Interações entre as 4 camadas;
•	Uniformização de variáveis;
•	Relatórios;
Entrega 07 (24 de juLho de 2020).
•	Interações entre as 4 camadas;
•	Versionamento ou Usabilidade;

