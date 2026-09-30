
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
uma implementação funcional em etapas futura

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
7. 8. 9. Data e horário de abertura da ocorrência
Descrição do problema e/ou observações do professor(a)
Equipamento(s) relacionado(s) — pode haver mais de um por ocorrência
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
1. 2. 3. 4. Conferência dos notebooks do carrinho
Pergunta obrigatória: houve ocorrência durante o uso? (Sim/Não)
Se "Sim": abertura de formulário de ocorrência (categoria da ocorrência, tipo de problema,
equipamento, descrição)
Registro de data/horário de devolução
RF04 — Cadastrar e gerenciar equipamentos
O sistema deve permitir o cadastramento e gerenciamento de equipamentos com os seguintes
atributos:
1. 2. 3. Bloco, sala, patrimônio/ID, tipo, modelo, data de recebimento, status, observações
Atualização de localização (movimentação entre salas)
Histórico de alterações e ocorrências vinculadas ao equipamento
RF05 — Cadastrar e gerenciar manutenção preventiva
O sistema deve permitir o cadastramento e gerenciamento das manutenções preventivas dos
equipamentos com os seguintes atributos:
1. Separação por Tecnologia (computadores, monitores, cabos, periféricos) e Infraestrutura
(ar-condicionado, TVs, projetores, cadeiras, tomadas, iluminação, estrutura)
2. 3. Checklist com data/horário, auxiliar responsável, sala, itens verificados, observações
Geração automática de ocorrência quando um item do checklist for reprovado
RF06 — Exibir dashboard
O sistema deve permitir a visualização do dashboard no sistema com os seguintes atributos:
1. Filtro por data/período
2. Ocorrências por prioridade
3. Tabela de ocorrências abertas (ID, local, problema, prioridade, status, responsável)
4. Histórico de ocorrências resolvidas/encerradas
RF07 — Gerar e exportar relatórios
O sistema deve gerar e exportar relatórios de acordo com as necessidades estabelecidas com os
seguintes atributos:
1. Períodos: semanal, mensal, anual
2. Total de ocorrências, principais problemas, salas com mais ocorrências, manutenções
realizadas, ocorrências com manutenção externa, demandas que exigem recursos/verba
3. Exportação em PDF e/ou Excel
RF08 — Gerenciar estoque de peças e materiais
O sistema deve permitir o gerenciamento de estoque de peças e materiais utilizados em
manutenções com os seguintes atributos:
1. Cadastro de item, quantidade, unidade, status
2. Baixa automática de estoque ao vincular material usado a uma ocorrência/manutenção
3. Histórico de movimentação (o quê, quando, em qual atendimento, por quem)
RF09 — Gerenciar acesso por perfil de usuário
O sistema deve gerenciar o acesso dos usuários do sistema com os seguintes atributos:
1. Perfis: professor, auxiliar docente, gestor/coordenador
2. Permissões diferentes por tela
RF10 — Autenticar usuários
O sistema deve autenticar o acesso dos usuários do sistema com os seguintes atributos:
1. Login com identificação e senha
2. Diferenciação de perfil
RF11 — Cadastrar usuários
O sistema deve permitir o cadastramento dos usuários do sistema com os seguintes atributos:
1. Nome, e-mail institucional, senha, perfil de acesso
2. Auto cadastro com aprovação dos Auxiliares Docentes
RF12 — Recuperar senha
O sistema deve permitir a recuperação de senha dos usuários do sistema com os seguintes
atributos:
1. Solicitação de redefinição via e-mail institucional
RF13 — Consultar detalhe e histórico da ocorrência
O sistema deve consultar o histórico de ocorrências com os seguintes atributos:
1. Linha do tempo com todas as mudanças de status, data/horário de cada mudança e
responsável dos equipamentos
2. Campo de comentários para comunicação entre quem abriu e quem está atendendo
RF14 — Consultar histórico pessoal (professor)
O sistema deve consultar o histórico pessoal dos professores com os seguintes atributos:
1. Lista de conferência dos carrinhos usados com data/horário, turma, disciplina e sala
utilizada
2. Lista de ocorrências abertas pelo próprio professor
RF15 — Notificar alertas
O sistema deve disparar alertas para os auxiliares docentes em caso de:
1. Carrinho aberto além do tempo esperado
2. Estoque abaixo do mínimo definido
3. Ocorrência crítica sem atendimento
RF16 — Gerenciar perfil do usuário
O sistema deve permitir o gerenciamento dos seguintes dados do perfil dos usuários:
1. Visualizar e editar dados próprios (nome, e-mail, senha)
RF17 — Parametrizar categorias, prioridades e prazos
O sistema deve permitir o gerenciamento dos seguintes dados das ocorrências:
1. 2. Cadastro/edição de categorias e subcategorias de ocorrência
Definição de prazo (SLA) esperado por nível de prioridade

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
Sistema deve estar acessível durante o horário de funcionamento da unidade.
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
•
RNF09 — Proteção de dados pessoais (LGPD)
Dados pessoais (nome, e-mail) tratados apenas para a finalidade do sistema, com acesso restrito
por perfil.
RNF10 — Auditoria e rastreabilidade
Toda ação administrativa relevante (cadastro, edição, exclusão) deve registrar usuário
responsável, data e horário.
RNF11 — Configurabilidade
O gestor deve poder ajustar categorias, prioridades e prazos (SLA) sem depender de alteração de código

# 3. Modelo de casos de uso

# 4. Modelo do banco de dados
(Modelo conceitual, Modelo lógico, Físico)

# 5. Banco de dados

# 6. Diagrama de classes
# 7. Estudo de viabilidade

# 8. Regras de negócio (Modelo canvas)

# 9. Design
(Paleta de cor, Tipografia, Logo, Wireframes, Modelo de navegação)

# 10. Protótipo
(Gere um protótipo funcional na ferramenta que se sentir mais confortável (Figma, por
exemplo) e apresente aqui, indicando o link).

# 11. Aplicação

# 12. Considerações finais

# 11. Referências# Diario-de-ocorrencias
Projeto Integrador - Fatec Jahu
