
&lt;p align=&quot;left&quot; style=&quot;font-size:28px;&quot;&gt;&lt;strong&gt;&lt;em&gt;Documentação do
PI&lt;/em&gt;&lt;/strong&gt;&lt;/p&gt;
&lt;details&gt;
&lt;summary&gt;&lt;strong&gt;�� Sumário&lt;/strong&gt;&lt;/summary&gt;

- [1. Introdução](#1-introdução)
- [Objetivos](#-objetivos)
- [Metodologia](#-metodologia)
- [2. Requisitos](#2-requisitos)
- [Requisitos funcionais](#-requisitos-funcionais)
- [Requisitos não funcionais](#-requisitos-não-funcionais)
- [3. Modelo de casos de uso](#3-modelo-de-casos-de-uso)
- [4. Modelo do banco de dados](#4-modelo-do-banco-de-dados)
- [5. Banco de dados](#5-banco-de-dados)
- [6. Diagrama de classes](#6-diagrama-de-classes)
- [7. Estudo de viabilidade](#7-estudo-de-viabilidade)
- [8. Regras de negócio (Modelo canvas)](#8-regras-de-negócio-modelo-canvas)
- [9. Design](#9-design)
- [10. Protótipo](#10-protótipo)
- [11. Aplicação](#11-aplicação)
- [12. Considerações finais](#12-considerações-finais)
- [13. Referências](#13-referências)

&lt;/details&gt;

Para cada semestre, do 1º ao 6º, iremos utilizar este template para documentar o PI -
incrementalmente.

# 1. Introdução
O projeto propõe o desenvolvimento de um protótipo de aplicação Web para auxiliar
na gestão das ocorrências, manutenções e equipamentos da unidade da FATEC.
Atualmente, problemas relacionados a computadores, periféricos, cabos, notebooks
e infraestrutura, como televisores, aparelhos de ar-condicionado, cadeiras e outros
recursos das salas e laboratórios, podem apresentar dificuldades de comunicação,
organização e acompanhamento entre professores, alunos e a equipe responsável
pelo atendimento.

Outro problema identificado está relacionado aos carrinhos de notebooks presentes
em algumas salas e laboratórios. Cada carrinho possui aproximadamente 20
notebooks, que precisam ser conferidos pelos professores no início e no final das
aulas. Atualmente, esse controle é realizado manualmente por meio de folhas de
registro, o que pode resultar em esquecimentos, falta de preenchimento e dificuldade
para identificar possíveis divergências.

Diante desse cenário, a aplicação proposta busca centralizar e organizar essas
informações, permitindo uma visualização mais clara das ocorrências e dos recursos
da instituição. Entre as funcionalidades planejadas estão o gerenciamento de
ocorrências, controle dos carrinhos de notebooks, cadastro de equipamentos,
acompanhamento de manutenção preventiva, dashboard de informações, relatórios
e controle de materiais e peças utilizados nas manutenções.

A motivação para o desenvolvimento do projeto surgiu a partir da observação de
necessidades reais da instituição e da busca por uma solução que possa contribuir
para melhorar a comunicação, a organização dos atendimentos e o controle dos
recursos disponíveis nos ambientes acadêmicos. Neste semestre, será desenvolvido
um protótipo estático da aplicação Web, com foco na estrutura e na experiência visual
das principais telas e funcionalidades do sistema.

## • Objetivos
O objetivo da aplicação Web é propor uma solução centralizada para auxiliar na
organização e no acompanhamento das ocorrências, manutenções e equipamentos
da FATEC, facilitando a comunicação entre alunos, professores, auxiliares docentes
e demais responsáveis pela infraestrutura da instituição.

Como objetivos específicos, o projeto busca:

• Organizar e centralizar o registro de ocorrências relacionadas à tecnologia e à
infraestrutura;

• Facilitar o acompanhamento do status e do atendimento das ocorrências;

• Melhorar a comunicação entre os usuários e a equipe responsável pela
manutenção;

• Propor uma forma digital de controle e conferência dos carrinhos de notebooks;
• Organizar informações sobre os equipamentos existentes nas salas e
laboratórios;

• Apoiar o controle e o planejamento de manutenções preventivas;

• Apresentar informações relevantes por meio de dashboards e relatórios;

• Propor uma interface intuitiva e de fácil utilização pelos diferentes usuários da
instituição.

Neste semestre, o objetivo prático é desenvolver um protótipo estático e navegável
da aplicação Web, demonstrando a estrutura, os fluxos de utilização e a interface das
principais funcionalidades propostas.

## • Metodologia
Para o desenvolvimento do projeto será utilizada uma abordagem de pesquisa
aplicada, buscando compreender as necessidades relacionadas à gestão de
ocorrências, manutenção e controle de equipamentos no ambiente acadêmico.

Inicialmente, será realizada a observação do funcionamento das atividades dos
auxiliares docentes e o levantamento dos principais problemas enfrentados no
atendimento de ocorrências, na comunicação entre as equipes e no controle dos
equipamentos e carrinhos de notebooks.

A partir dos problemas identificados, foram levantados os requisitos e definidas as
principais funcionalidades da aplicação. Serão elaborados os fluxos de navegação, a
estrutura das telas e o protótipo da interface utilizando tecnologias de
desenvolvimento Web, como HTML, CSS e Javascript.

A pesquisa e o desenvolvimento serão realizados durante o semestre letivo, tendo
como ambiente de estudo a unidade da FATEC envolvida no projeto. Nesta primeira
etapa, o resultado será um protótipo estático e navegável, desenvolvido com foco na
representação visual da solução e na experiência de uso, servindo como base para
uma implementação funcional em etapas futura.

# 2. Requisitos

## • Requisitos funcionais
RF01 — Gerenciar ocorrências

O sistema deve permitir o registro de ocorrências com os seguintes atributos:
1. ID da ocorrência
2. Categoria (Tecnologias ou Infraestrutura)
3. Tipo de problema (hardware, armazenamento, rede, software, televisão, ar-condicionado)
4. Local (sala/laboratório)
5. Prioridade da ocorrência (baixa, média, alta, crítica)
6. Status (Aberta, Em análise, Em andamento, Aguardando peça/material/manutenção
externa, Resolvida, Encerrada)
7. Data e horário de abertura da ocorrência
8. Descrição do problema e/ou observações do professor(a)
9. Equipamento(s) relacionado(s) — pode haver mais de um por ocorrência

RF02 — Controlar carrinhos de notebooks via QR Code ou Link

O sistema deve permitir o registro de controle dos carinhos de notebooks com os seguintes
atributos:
1. Login/identificação do professor responsável
2. Registro de curso, disciplina, turma e sala utilizada
3. Data e horário de abertura
4. Identificação do carrinho

RF03 — Checklist de devolução do carrinho

O sistema deve permitir o checklist de devolução dos carinhos de notebooks com os seguintes
atributos:
1. Conferência dos notebooks do carrinho
2. Pergunta obrigatória: houve ocorrência durante o uso? (Sim/Não)
3. Se "Sim": abertura de formulário de ocorrência (categoria da ocorrência, tipo de problema,
equipamento, descrição)
4. Registro de data/horário de devolução

RF04 — Cadastrar e gerenciar equipamentos

O sistema deve permitir o cadastramento e gerenciamento de equipamentos com os seguintes
atributos:
1. Bloco, sala, patrimônio/ID, tipo, modelo, data de recebimento, status, observações
2. Atualização de localização (movimentação entre salas)
3. Histórico de alterações e ocorrências vinculadas ao equipamento

RF05 — Cadastrar e gerenciar manutenção preventiva

O sistema deve permitir o cadastramento e gerenciamento das manutenções preventivas dos
equipamentos com os seguintes atributos:
1. Separação por Tecnologia (computadores, monitores, cabos, periféricos) e Infraestrutura
(ar-condicionado, TVs, projetores, cadeiras, tomadas, iluminação, estrutura)
2. Checklist com data/horário, auxiliar responsável, sala, itens verificados, observações
3. Geração automática de ocorrência quando um item do checklist for reprovado

RF06 — Exibir dashboard

O sistema deve permitir a visualização do dashboard no sistema com os seguintes atributos:
1. Filtro por data/período
2. Ocorrências por prioridade
3. Tabela de ocorrências abertas (ID, local, problema, prioridade, status, responsável)
4. Histórico de ocorrências resolvidas/encerradas
5. Identificação de manutenção

RF07 — Gerar e exportar relatórios

O sistema deve gerar e exportar relatórios de acordo com as necessidades estabelecidas com os
seguintes atributos:
1. Períodos: semanal, mensal, anual
2. Total de ocorrências, principais problemas, salas com mais ocorrências, manutenções
realizadas, ocorrências com manutenção externa, demandas que exigem recursos/verba
3. Exportação em PDF e/ou Excel

   
RF08 — Gerenciar acesso por perfil de usuário

O sistema deve gerenciar o acesso dos usuários do sistema com os seguintes atributos:
1. Perfis: professor, auxiliar docente, gestor/coordenador
2. Permissões diferentes por tela

RF09 — Autenticar usuários

O sistema deve autenticar o acesso dos usuários do sistema com os seguintes atributos:
1. Login com identificação e senha
2. Diferenciação de perfil

RF10 — Cadastrar usuários

O sistema deve permitir o cadastramento dos usuários do sistema com os seguintes atributos:
1. Nome, e-mail institucional, senha, perfil de acesso
2. Cadastro com aprovação dos Auxiliares Docentes

RF11 — Recuperar senha

O sistema deve permitir a recuperação de senha dos usuários do sistema com os seguintes
atributos:
1. Solicitação de redefinição via e-mail institucional
   
RF12 — Consultar detalhe e histórico da ocorrência

O sistema deve consultar o histórico de ocorrências com os seguintes atributos:
1. Linha do tempo com todas as mudanças de status, data/horário de cada mudança e
responsável dos equipamentos
2. Campo de comentários para comunicação entre quem abriu e quem está atendendo

RF13 — Consultar histórico pessoal (professor)

O sistema deve consultar o histórico pessoal dos professores com os seguintes atributos:
1. Lista de conferência dos carrinhos usados com data/horário, turma, disciplina e sala
utilizada
2. Lista de ocorrências abertas pelo próprio professor

RF14 — Notificar alertas

O sistema deve disparar alertas para os auxiliares docentes em caso de:
1. Carrinho aberto além do tempo esperado
2. Ocorrência crítica sem atendimento

RF15 — Gerenciar perfil do usuário

O sistema deve permitir o gerenciamento dos seguintes dados do perfil dos usuários:
1. Visualizar e editar dados próprios (nome, e-mail, senha)

RF16 — Parametrizar categorias, prioridades e prazos

O sistema deve permitir o gerenciamento dos seguintes dados das ocorrências:
1. Cadastro/edição de categorias e subcategorias de ocorrência
2. Definição de prazo (SLA) esperado por nível de prioridade

## • Requisitos não funcionais
RNF01 — Usabilidade
Interface intuitiva, adequada para uso rápido por professores entre aulas (poucos cliques para
abrir/fechar carrinho).

RNF02 — Compatibilidade
Sistema acessível via navegador em desktop e dispositivos móveis.

RNF03 — Desempenho
Tempo de resposta ao abrir/fechar carrinho não deve ultrapassar poucos segundos.

RNF04 — Segurança
Autenticação obrigatória para qualquer registro no sistema; controle de acesso por perfil.

RNF05 — Disponibilidade
Sistema deve estar acessível durante as 24hrs do dia.

RNF06 — Manutenibilidade
Código organizado em módulos (ocorrências, carrinhos, equipamentos, estoque) para facilitar
futuras expansões.

RNF07 — Portabilidade
Por ser protótipo estático neste semestre, deve rodar sem dependência de servidor/banco de
dados.

RNF08 — Acessibilidade
O sistema precisa ser acessível para todos os usuários, por definição do Wcag (Web Content
Accessibility Guidelines) será utilizado:
• Uso de cor + ícone + texto para indicar status/prioridade, nunca só cor.

• Contraste mínimo adequado entre texto e fundo.

• Labels associados a todos os campos de formulário.

• Área de toque adequada para uso rápido em celular.

• Texto alternativo em imagens anexadas às ocorrências.

• Navegação por teclado nas telas principais.

RNF09 — Proteção de dados pessoais (LGPD)
Dados pessoais (nome, e-mail) tratados apenas para a finalidade do sistema, com acesso restrito
por perfil.

RNF10 — Auditoria e rastreabilidade
Toda ação administrativa relevante (cadastro, edição, exclusão) deve registrar usuário
responsável, data e horário.

RNF11 — Configurabilidade
O gestor deve poder ajustar categorias, prioridades e prazos (SLA) sem depender de alteração de código

HISTÓRIAS DE USUÁRIOS

HU01 – Abrir e devolver o carrinho de notebooks

Como professor, quero ler o QR Code do carrinho com o celular e fazer a conferência dos notebooks ao final da aula, para registrar o uso sem preencher folhas de papel e evitar esquecimentos e divergências. Relacionados: RF02, RF03, RF17.  
Critérios de aceite: O carrinho é identificado pelo QR Code (simulado por seleção no protótipo); A devolução exige a quantidade conferida e a resposta à pergunta "houve ocorrência?"; Os registros de abertura e devolução guardam data e horário. 

HU02 – Acompanhar e atualizar o status de uma ocorrência 

Como auxiliar docente, quero visualizar as ocorrências abertas e atualizar o status de cada uma ao longo do atendimento, para organizar a manutenção e manter professores e gestores informados sobre o andamento. Relacionados: RF01, RF04, RF12.
Critérios de aceite: A lista mostra ID, local, problema, prioridade, status e responsável; Cada mudança de status entra na linha do tempo, com data, horário e responsável.

HU03 – Consultar relatórios de manutenção por período

Como gestor/coordenador, quero gerar relatórios semanais, mensais ou anuais das ocorrências e manutenções, para identificar os problemas mais frequentes e as salas mais afetadas e embasar pedidos de recursos junto à direção. Relacionados: RF06, RF07.
Critérios de aceite: O relatório permite escolher o período (semanal, mensal ou anual); Mostra o total de ocorrências, os principais problemas, as salas mais afetadas e as demandas que exigem recursos; Pode ser exportado em PDF ou Excel. 

HU04 – Abrir uma ocorrência

Como professor, quero registrar um problema informando categoria, tipo, local, prioridade e descrição, para que a equipe responsável seja avisada sem que eu precise procurar um auxiliar. Relacionados: RF01, RF13.  
Critérios de aceite: Categoria, tipo, local e descrição são obrigatórios; A ocorrência nasce com status "Aberta" e sem responsável; O autor consegue acompanhar o andamento em "Meu histórico". 

HU05 – Aprovar cadastros

Como auxiliar docente, quero analisar as solicitações de acesso e aprovar ou recusar cada uma, para garantir que somente pessoas autorizadas usem o sistema. Relacionados: RF08, RF10.  
Critérios de aceite: A lista mostra nome, e-mail institucional e perfil solicitado; O login só é liberado depois da aprovação; A decisão registra quem decidiu e quando. 

HU06 – Registrar vistoria preventiva

Como auxiliar docente, quero preencher um checklist de itens por sala, para registrar o estado dos equipamentos e abrir uma ocorrência automaticamente quando algo for reprovado. Relacionados: RF05. 
Critérios de aceite: Cada item pode ser marcado como aprovado ou reprovado; Ao concluir com item reprovado, uma ocorrência é criada; O checklist registra data, horário, sala e responsável.

HU07 – Ajustar prioridades e prazos 

Como gestor, quero alterar categorias, prioridades e prazos (SLA) sem depender da equipe de desenvolvimento, para adaptar o atendimento à realidade da unidade. Relacionados: RF16, RNF11. 
Critérios de aceite: As categorias e os prazos por prioridade podem ser editados na tela de configurações; A alteração vale para as novas ocorrências. 

HU08 – Receber alertas 

Como auxiliar docente, quero ser avisado quando um carrinho passar de 2 horas aberto ou quando uma ocorrência crítica estiver sem atendimento, para agir antes que o problema se agrave. Relacionados: RF14. 
Critérios de aceite: O contador de alertas aparece no cabeçalho de todas as telas; Cada alerta mostra o motivo e leva à área correspondente. 

# 3. Modelo de casos de uso

# 4. Modelo do banco de dados
(Modelo conceitual, Modelo lógico, Físico)

# 5. Banco de dados

# 6. Diagrama de classes
# 7. Estudo de viabilidade

Este capítulo analisa a viabilidade de desenvolvimento e implantação do sistema de gestão de ocorrências, manutenções e equipamentos para a unidade da FATEC de Jaú, a partir dos requisitos funcionais (RF01 a RF17), dos requisitos não funcionais (RNF01 a RNF11) e das necessidades observadas na instituição.
A análise considera as dimensões técnica, financeira, de mercado e operacional, identifica os principais riscos do projeto e encerra com a conclusão do grupo. 

7.1 VIABILIDADE TÉCNICA 

A equipe possui o conhecimento técnico necessário (HTML, CSS e JavaScript, estudados no curso) para desenvolver o protótipo estático proposto, o que foi confirmado pela construção do protótipo navegável neste semestre. Não há necessidade de equipamentos especiais: um computador para desenvolvimento e um celular com câmera para testar a leitura do QR Code já atendem. A hospedagem pode ser feita gratuitamente (por exemplo, no GitHub Pages), e a complexidade do escopo deste semestre (protótipo navegável, sem banco de dados funcional) é compatível com o tempo e o conhecimento técnico disponíveis. Para a versão funcional, prevista para o próximo semestre, será necessário acrescentar banco de dados e back-end. A modelagem inicial dos dados, apresentada no capítulo 6, reduz esse esforço, e o conteúdo do curso nas disciplinas de banco de dados e programação acompanha essa etapa. 

7.2 VIABILIDADE FINANCEIRA

Não há investimento financeiro relevante: o desenvolvimento é realizado pela própria equipe como trabalho acadêmico, sem custo de mão de obra contratada, e a hospedagem do protótipo é gratuita. O único custo possível seria a aquisição de etiquetas de QR Code para os carrinhos. O benefício não é financeiro, mas operacional: a redução do tempo e do retrabalho hoje gastos com o controle manual por folhas de registro, além de gerar dados que podem subsidiar pedidos de verba junto à direção da FATEC. O risco financeiro do projeto, portanto, é baixo. Na versão funcional, poderá haver custo de hospedagem do servidor e do banco de dados, a ser avaliado com a coordenação (por exemplo, uso da infraestrutura da própria instituição). 

7.3 VIABILIDADE DE MERCADO

Como o sistema é de uso interno institucional, não há concorrência direta no sentido comercial. A solução hoje em uso é informal: o controle manual por folhas de registro e a comunicação direta com os auxiliares docentes. Embora existam sistemas genéricos de gestão de chamados, eles tendem a não contemplar o controle dos carrinhos de notebooks nem o fluxo de trabalho específico dos auxiliares docentes da unidade. O sistema proposto tende a ter boa aceitação porque resolve um problema real, observado na rotina da instituição, e porque o fluxo principal foi desenhado para ser simples e rápido, reduzindo a resistência de adoção. 

7.4 VIABILIDADE OPERACIONAL

A equipe do grupo tem a força de trabalho necessária para o escopo deste semestre, com apoio da orientação da professora Cida Zen. A estrutura organizacional da FATEC já conta com os Auxiliares Docentes como futuros operadores do sistema, o que facilita a validação contínua. Em relação aos requisitos legais, o sistema trata dados pessoais (nome e e-mail institucional dos usuários), o que exige atenção à Lei Geral de Proteção de Dados (LGPD), ponto que deve ser observado mesmo em fase de protótipo. Por isso, o acesso aos dados é restrito por perfil e limitado à finalidade do sistema (RNF04 e RNF09). 

7.5 CONCLUSÃO

Com base na análise das quatro dimensões, conclui-se que o projeto é viável para o escopo proposto. Tecnicamente, a equipe dispõe do conhecimento e das ferramentas necessárias, com hospedagem gratuita para o protótipo. Financeiramente, o custo é praticamente nulo e o retorno esperado é operacional, com menos retrabalho e mais organização no controle de ocorrências, equipamentos e carrinhos de notebooks. Quanto ao mercado, a adoção tende a ser favorável por atender a uma necessidade real da instituição. Operacionalmente, a equipe e a estrutura da FATEC comportam o desenvolvimento, desde que o tratamento de dados pessoais respeite a LGPD e que os riscos identificados sejam acompanhados. Assim, recomenda-se dar continuidade ao projeto, evoluindo o protótipo estático e navegável para uma versão funcional, com banco de dados, no próximo semestre. 

# 8. Regras de negócio (Modelo canvas)

As regras de negócio descrevem o propósito do sistema, a forma como ele foi construído, o público que atenderá e os custos envolvidos, além de apresentar o modelo de negócio do projeto. Neste capítulo, as informações levantadas a partir das necessidades observadas na unidade da FATEC de Jaú são organizadas de modo a responder, em sequência, às perguntas: o que será realizado, como será realizado, para quem será realizado e quanto custará. Ao final, o Modelo Business Canvas resume esses pontos em uma visão única do projeto.

8.1 O QUE SERÁ REALIZADO?

Será desenvolvido um sistema Web para centralizar o registro e o acompanhamento de ocorrências de tecnologia e infraestrutura da unidade da FATEC de Jaú. O sistema também reúne o controle digital dos carrinhos de notebooks, o cadastro de equipamentos, a manutenção preventiva, além de dashboard e relatórios gerenciais. Neste semestre, foram entregues o design das telas, a modelagem inicial dos dados e um protótipo estático e navegável, que demonstra a estrutura, os fluxos de utilização e a interface das principais funcionalidades, sem implementar ainda o banco de dados e as regras de negócio completas. A versão funcional está prevista para o próximo semestre. 

8.2 COMO SERÁ REALIZADO?

O desenvolvimento ocorreu ao longo do semestre, em etapas organizadas pelos grupos de requisitos funcionais: ocorrências, carrinhos de notebooks, equipamentos, manutenção preventiva, dashboard e relatórios. As principais atividades são o levantamento e a validação de requisitos com os Auxiliares Docentes, a elaboração do design (identidade visual e wireframes), a construção das telas do protótipo, a modelagem dos dados e os testes de usabilidade com professores e auxiliares. Para isso, o grupo conta com seus próprios conhecimentos técnicos, com a orientação acadêmica da professora Cida Zen e com hospedagem estática gratuita (GitHub Pages) para publicar o protótipo. O fluxo de uso dos carrinhos parte de um QR Code físico fixado em cada carrinho, lido pelo celular do professor (simulado no protótipo deste semestre).

8.3 PARA QUEM SERÁ REALIZADO?

O sistema atende a quatro públicos da FATEC: • Professores: usuários do dia a dia, que abrem e devolvem os carrinhos de notebooks e registram ocorrências. • Auxiliares Docentes: responsáveis pela gestão operacional de ocorrências, equipamentos e manutenção, e pela aprovação de novos cadastros. • Gestores e coordenação: acompanham a situação da unidade por meio do dashboard e dos relatórios e definem os parâmetros do sistema. • Alunos: beneficiários indiretos, que se favorecem de equipamentos e salas em melhor estado. A abertura de ocorrências pelos próprios alunos está prevista para uma etapa futura, com a criação de um perfil específico. 

8.4 QUANTO CUSTARÁ?

O custo direto do projeto é praticamente nulo. O desenvolvimento é feito pela própria equipe como trabalho acadêmico, sem contratação de mão de obra, e a hospedagem do protótipo é gratuita. Os custos envolvidos são o tempo da equipe (desenvolvimento, design e documentação) e, eventualmente, materiais físicos de baixo valor, como as etiquetas de QR Code para os carrinhos.

8.5 MODELO BUSINESS CANVAS

Business Model Canvas do projeto, apresentado na Figura 1, resume em uma única visão como o sistema gera valor para a unidade da FATEC de Jaú. Como se trata de um sistema de uso interno institucional, o modelo foi adaptado: não há venda do produto, e o retorno esperado é institucional, como dito anteriormente.
A proposta de valor reúne quatro pontos: a centralização do registro e do acompanhamento das ocorrências de tecnologia e infraestrutura; a digitalização do controle dos carrinhos de notebooks, reduzindo esquecimentos e divergências; a visibilidade gerencial por meio de dashboard e relatórios, que apoia a tomada de decisão; e a rastreabilidade de equipamentos e manutenções em um único sistema. 
O segmento de mercado é formado por quatro públicos: os professores, usuários do dia a dia dos carrinhos e da abertura de ocorrências; os auxiliares docentes, responsáveis pela gestão operacional de ocorrências, equipamentos e manutenção; os gestores e a coordenação, que acompanham a unidade por dashboard e relatórios; e os alunos, beneficiários indiretos, com abertura de ocorrências prevista para uma etapa futura. 
Os canais são o acesso via navegador, em computador e celular, o QR Code físico fixado nos carrinhos como ponto de entrada do fluxo e a apresentação do protótipo. Nas relações com clientes, o modelo prevê o uso direto e assistido pelos professores entre as aulas, a validação contínua com a equipe de auxiliares docentes e a coleta de feedback. 
As atividades-chave são o desenvolvimento do protótipo estático e navegável, o levantamento e a validação de requisitos com os auxiliares docentes, a modelagem dos dados (modelos conceitual, de classes e lógico) e os testes de usabilidade com professores e auxiliares. Os recursos-chave são a equipe do grupo, o conhecimento técnico, a orientação acadêmica e a hospedagem estática (GitHub Pages) para o protótipo. 
As parcerias-chave são a coordenação da FATEC de Jaú, a professora orientadora e a equipe de auxiliares docentes da unidade. 
Por fim, a estrutura de custo é composta pelo tempo da equipe (desenvolvimento, design e documentação), pela hospedagem estática, que tem custo baixo ou nulo, e por eventuais materiais físicos, como as etiquetas de QR Code dos carrinhos.
A fonte de renda não se aplica em sentido comercial: o retorno é institucional, com redução de retrabalho manual, melhoria da comunicação entre setores e dados estruturados para justificar pedidos de recurso e verba junto à direção. 

Figura 1 – Business Model Canvas do sistema de gestão de ocorrências, manutenções e equipamentos 

Fonte: Elaborado pelos autores (2026). 

# 9. Design
(Paleta de cor, Tipografia, Logo, Wireframes, Modelo de navegação)

Este capítulo apresenta as decisões de design do sistema Diário de Ocorrências, desde a identidade visual até a estrutura das telas. O design foi desenvolvido em duas etapas: primeiro, os wireframes de baixa fidelidade, que definiram a organização das informações e os fluxos de navegação; depois, o protótipo navegável em HTML, CSS e JavaScript, apresentado no capítulo 7.
Como o sistema será usado por professores entre aulas, por auxiliares docentes no atendimento e por gestores na análise de indicadores, as decisões buscaram rapidez de uso, clareza das informações e consistência entre as telas e entre os perfis. 

9.1 IDENTIDADE VISUAL

A identidade visual segue as cores e o logotipo do Centro Paula Souza, para que o sistema seja reconhecido como parte do ambiente institucional da FATEC. Todos os perfis de usuário (professor, auxiliar docente e gestor/coordenação) compartilham a mesma identidade, com o vermelho institucional como cor principal. 

9.1.1 Logotipo

O logotipo do Centro Paula Souza é utilizado em três versões, conforme o fundo em que é aplicado: a versão branca, sobre os fundos vermelhos do menu lateral e do painel de apresentação da tela de acesso; a versão vermelha, sobre fundos claros; e a versão preta, para materiais impressos ou em escala de cinza. 
O logotipo foi mantido sem alterações de proporção ou de cor. 
Figura 2 – Versões do logotipo do Centro Paula Souza utilizadas no sistema: (a) vermelha, (b) preta, (c) branca.


Fonte: Centro Paula Souza. [A versão branca é invisível em fundo claro.] 

9.1.2 Paleta de cores 

A paleta combina o vermelho institucional, aplicado no menu lateral, nos botões principais, nos links e na tela de acesso, com azul-escuro e cinza-azulado nos textos, tons de cinza claro nos fundos e divisórias, e um verde-azulado de apoio nos indicadores. 
Os fundos claros mantêm a leitura confortável e destacam o conteúdo. 

Figura 3 – Paleta de cores do sistema 

Fonte: Elaborado pelos autores (2026). 

Cores de status e prioridade Os selos de status e prioridade usam tons claros de verde, amarelo e vermelho, sempre acompanhados de texto e símbolo (por exemplo, ⚠ Crítica e ✓ Resolvida), para que a informação não dependa apenas da cor (RNF08). 
Como o vermelho é a cor da marca e a cor de alerta, o nível "Crítica" é distinguido pelo ícone e pelo texto, e não apenas pela cor. 

9.1.3 Tipografia

A fonte principal do projeto é a Inter, importada do Google Fonts. É uma fonte sem serifa, desenvolvida para telas, com boa legibilidade em tamanhos pequenos tanto no computador quanto no celular.
A hierarquia visual é feita pelo peso da fonte:

Figura 4 – Tipografia do sistema

Fonte: Elaborado pelos autores (2026). 

9.1.4 Componentes

O sistema reutiliza poucos componentes em todas as telas, o que reduz o tempo de aprendizado:
• botão principal em vermelho, para a ação mais importante da tela (ex.: "Registrar ocorrência"); 
• botão secundário com contorno, para ações auxiliares (ex.: "Detalhes");
• cartões brancos com cantos arredondados, para agrupar informações; 
• tabelas com cabeçalho em letras maiúsculas pequenas, para listas; 
• selos de status e prioridade, com texto e símbolo;
• janelas modais, para ações rápidas como abrir uma ocorrência ou cadastrar um equipamento sem sair da lista.

9.2 MAPA DE NAVEGAÇÃO POR PERFIL

Todas as telas compartilham a mesma estrutura: menu lateral à esquerda, com o logotipo e as seções do sistema, cabeçalho com o nome e o perfil do usuário, contador de alertas e botão de saída, e área de conteúdo à direita. 
O item do menu da tela atual fica destacado. Manter esse padrão faz com que o usuário encontre sempre os mesmos elementos no mesmo lugar, o que atende ao requisito de usabilidade (RNF01). 
O acesso às telas varia conforme o perfil (RF08):

O fluxo de acesso é composto por quatro telas: entrar, criar cadastro (com aprovação de um auxiliar docente antes do primeiro acesso), redefinir senha e verificação em duas etapas, com código de 6 dígitos enviado ao e-mail institucional (RF09 a RF11). 

9.3 WIREFRAMES (BAIXA FIDELIDADE)

Os wireframes foram elaborados no Figma, em tons de cinza, sem cores, imagens ou textos definitivos, com o objetivo de validar a posição dos elementos e o fluxo entre as telas antes da codificação. Essa etapa permitiu discutir em grupo o que cada tela deveria mostrar e em que ordem, sem a influência das decisões visuais. Foram desenhadas 17 telas, que cobrem o acesso ao sistema, as telas principais de cada área e as telas de detalhe:

Figura 5 – Tela de Login

Fonte: Elaborado pelos autores (2026). 

Figura 6 – Tela de Redefinição de Senha

Fonte: Elaborado pelos autores (2026).

Figura 7 – Tela de Cadastro

Fonte: Elaborado pelos autores (2026).

Figura 8 – Visão Geral do Sistema

Fonte: Elaborado pelos autores (2026).

Figura 9 – Tela de Linha do tempo da Ocorrência

Fonte: Elaborado pelos autores (2026).

Figura 10 – Tela de Ocorrências

Fonte: Elaborado pelos autores (2026). 

Figura 11 – Tela de Registrar Ocorrências 

Fonte: Elaborado pelos autores (2026).

Figura 12 – Tela de Acompanhamento dos Carinhos de Notebooks

Fonte: Elaborado pelos autores (2026). 

Figura 13 – Tela de Detalhe do equipamento: movimentações e ocorrências vinculadas 

Fonte: Elaborado pelos autores (2026). 

Figura 14 – Tela de Equipamentos

Fonte: Elaborado pelos autores (2026).

Figura 15 – Tela de Histórico dos Professores

Fonte: Elaborado pelos autores (2026).

Figura 16 – Tela de Manutenção Preventiva 

Fonte: Elaborado pelos autores (2026). 

Figura 17 – Tela de Relatórios

Fonte: Elaborado pelos autores (2026). 

Figura 18 – Tela de Aprovação de Cadastros

Fonte: Elaborado pelos autores (2026). 

Figura 19 – Tela de Usuários e Configurações

Fonte: Elaborado pelos autores (2026).

Figura 20 – Tela de Alertas

Fonte: Elaborado pelos autores (2026). 

Figura 21 – Tela de Perfil do Usuário

Fonte: Elaborado pelos autores (2026). 

Na passagem dos wireframes para o protótipo, a estrutura das telas foi mantida e acrescentaram-se a identidade visual, o conteúdo de demonstração, a tela de verificação em duas etapas (código de 6 dígitos) e a janela modal de cadastro de equipamento, que foram definidas diretamente no protótipo. A adaptação das telas para o celular será validada na etapa seguinte, conforme o requisito RNF02. 

# 10. Protótipo
(Gere um protótipo funcional na ferramenta que se sentir mais confortável (Figma, por
exemplo) e apresente aqui, indicando o link).

# 11. Aplicação

# 12. Considerações finais
Este documento apresentou a descrição, os requisitos, o estudo de viabilidade, as regras de negócio, o design, a modelagem de dados e o protótipo do Diário de Ocorrências, um sistema Web que busca centralizar o registro e o acompanhamento de ocorrências de tecnologia e infraestrutura da FATEC de Jaú, o controle digital dos carrinhos de notebooks, o cadastro de equipamentos e a manutenção preventiva.
Neste primeiro semestre de desenvolvimento, o grupo entregou um protótipo estático e navegável, construído com HTML, CSS e JavaScript e apoiado em 17 wireframes de baixa fidelidade, que cobre os fluxos de acesso, ocorrências, carrinhos, equipamentos, manutenção preventiva, relatórios, alertas e gestão de usuários para os três perfis previstos (professor, auxiliar docente e gestor). Foram levantados 17 requisitos funcionais e 11 requisitos não funcionais, e a identidade visual seguiu a do Centro Paula Souza, com atenção à acessibilidade conforme as diretrizes do WCAG. Também foram elaborados os modelos conceitual, de classes e lógico dos dados, o que antecipa o trabalho do próximo semestre. 
O projeto tem limitações que o grupo reconhece. Por ser um protótipo estático, o sistema não armazena dados e simula funções que dependem de servidor, como o envio de e-mails, a leitura de QR Code, o cálculo dos alertas e a exportação de relatórios. Os modelos de dados correspondem a uma primeira versão e ainda precisam de revisão e normalização, conforme descrito na seção 6.5. Outros pontos ficaram para a próxima etapa: o perfil de aluno para abertura de ocorrências, o controle de materiais e peças, os anexos de imagem nas ocorrências e a melhoria do contraste nas bordas dos campos. 
Como próximos passos, o grupo pretende validar o protótipo com os auxiliares docentes e os professores, revisar e alinhar os três modelos de dados, criar o banco de dados e o script SQL, desenvolver o back-end com autenticação, perfis e regras de negócio, e integrá-lo às telas já construídas, sempre observando a Lei Geral de Proteção de Dados. Espera-se que a solução reduza o retrabalho do controle manual em folhas de registro, melhore a comunicação entre professores e auxiliares docentes e forneça informações organizadas para a gestão da unidade e para pedidos de recursos junto à direção. 
Por fim, o desenvolvimento do projeto permitiu ao grupo aplicar, em um problema real da instituição, os conteúdos estudados no curso, como levantamento de requisitos, design de interfaces, programação Web e modelagem de dados, além de exercitar o trabalho em equipe e a organização das tarefas ao longo do semestre. 

# 11. Referências# Diario-de-ocorrencias
BRASIL. Lei nº 13.709, de 14 de agosto de 2018. Lei Geral de Proteção de Dados Pessoais (LGPD). Diário Oficial da União: seção 1, Brasília, DF, 15 ago. 2018.

CENTRO PAULA SOUZA. Centro Paula Souza. São Paulo, [s.d.]. Disponível em: https://www.cps.sp.gov.br. Acesso em: 4 nov. 2026.

FIGMA. Figma: the collaborative interface design tool. [S.l.], [s.d.]. Disponível em: https://www.figma.com. Acesso em: 4 nov. 2026.

GITHUB. GitHub Pages. [S.l.], [s.d.]. Disponível em: https://pages.github.com. Acesso em: 4 nov. 2026.

GOOGLE FONTS. Inter. [S.l.], [s.d.]. Disponível https://fonts.google.com/specimen/Inter. Acesso em: 4 nov. 2026.

em: OSTERWALDER, Alexander; PIGNEUR, Yves. Business Model Generation: inovação em modelos de negócios. Rio de Janeiro: Alta Books, 2011.

TRELLO. Grupo 1 – Diário de Ocorrências. [S.l.], [s.d.]. Disponível em: https://trello.com/b/QudlJj59/grupo-1-diario-de-ocorrencias. Acesso em: 4 nov. 2026.

W3C. Web Content Accessibility Guidelines (WCAG) 2.1. [S.l.]: World Wide Web Consortium, 2018.

Disponível em: https://www.w3.org/TR/WCAG21/. Acesso em: 4 nov. 2026.

ELMASRI, Ramez; NAVATHE, Shamkant B. Sistemas de banco de dados. 7. ed. São Paulo: Pearson, 2018.

SOMMERVILLE, Ian. Engenharia de software. 10. ed. São Paulo: Pearson, 2018. 


Projeto Integrador - Fatec Jahu
