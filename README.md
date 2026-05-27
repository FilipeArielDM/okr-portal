# 🚀 OKR-Track: Sistema Corporativo de Alinhamento Estratégico & Governança

Seja bem-vindo ao repositório do **OKR-Track**! 

Eu desenvolvi esta plataforma para solucionar um dos maiores desafios na gestão de médias e grandes empresas: a **rastreabilidade de 100% da execução estratégica e a governança operacional**.

O objetivo deste projeto é demonstrar a minha capacidade técnica na construção de arquiteturas corporativas robustas. O OKR-Track integra a definição de objetivos estratégicos com a prestação de contas no nível tático, permitindo que a liderança monitore o andamento de cada iniciativa em tempo real e valide a conformidade das entregas por meio de evidências documentais anexadas diretamente ao sistema.

---

## 🎯 Proposta de Valor & Funcionalidades Centrais

Desenvolvi o OKR-Track focando em resolver a falta de consistência e auditoria de ferramentas genéricas. Os pilares do projeto são:

### 1. Rastreabilidade de 100% da Execução
* O dashboard consolidado exibe o status de todos os OKRs, Key Results e Iniciativas de forma hierárquica e estruturada.
* Indicadores visuais claros identificam instantaneamente quais frentes de trabalho estão **No Prazo (On Track)**, **Em Risco (At Risk)** ou **Atrasadas (Behind)**.
* Suporte a múltiplos modos de visualização dinâmica (Cronogramas semanais/mensais e Diagramas de Gantt).

### 2. Governança & Auditoria com Evidências (Compliance)
* Cada check-in de progresso na plataforma exige o preenchimento de justificativas detalhadas e permite o **anexo de arquivos (PDFs, propostas comerciais, orçamentos e especificações técnicas)** como provas físicas de execução.
* Workflow de aprovação de propostas e anexos integrado para garantir auditoria contínua da utilização de recursos corporativos.

### 3. Matriz de Permissões & Controle de Acesso (RBAC)
* Estrutura de papéis hierárquicos bem delineados para simular um ambiente de produção real:
  * **Gestor Tático (Colaborador):** Focado no progresso das metas e iniciativas de seu respectivo departamento.
  * **Gestor Estratégico:** Acesso amplo e poder de edição estratégica sobre os OKRs de alto nível da organização.
  * **Administrador (TI Admin):** Gerenciamento de usuários, parametrizações e auditoria completa de acessos e modificações de dados.

---

## 🛠️ Arquitetura Técnica & Stack Tecnológico

Eu estruturei o projeto seguindo princípios de clean code, desacoplamento e robustez de banco de dados:

* **Frontend (React 19 + TypeScript):**
  * Componentização moderna com Tailwind CSS e efeitos de Glassmorphism.
  * Gerenciamento de estados robusto e rotas protegidas em ambiente dinâmico.
  * Geração de relatórios executivos em formato Word (DOCX) diretamente pelo navegador.
  * Gráficos dinâmicos com **Recharts** para análise de progresso e correlações.

* **Backend (Node.js + Express):**
  * API RESTful modularizada com tratamento de erros centralizado.
  * Cliente SQL nativo com suporte a transações atômicas e consultas parametrizadas.

* **Banco de Dados (Microsoft SQL Server):**
  * Modelagem robusta contendo tabelas de objetivos, key results, check-ins, anexos, logs de sistema (audit trail) e histórico de acesso do usuário.

---

## ⚡ Como Testar a Plataforma (Modo de Demonstração / Sandbox)

Para facilitar a avaliação da plataforma por recrutadores e engenheiros, o repositório disponibiliza um **Ambiente de Teste (Sandbox)** 100% funcional que roda de forma estática no navegador (sem necessidade de configurar banco de dados ou chaves externas).

1. Acesse o diretório do frontend:
   ```bash
   cd okr
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Inicie o servidor de desenvolvimento local:
   ```bash
   npm run dev
   ```
4. Ao abrir a página inicial, clique em **Acessar Ambiente de Teste**. 
5. Escolha um dos perfis pré-configurados (Gestor Tático, Gestor Estratégico ou Administrador) para experimentar as diferentes telas, permissões e usabilidades em tempo real. Os dados alterados persistem na sessão do navegador via `localStorage`.

---

## 🔒 Governança de Código & Segurança
* **Código Higienizado:** Todas as integrações com SSO Azure AD e credenciais corporativas foram desacopladas deste repositório público, sendo gerenciadas unicamente por variáveis de ambiente (`.env`).
* **Dados Fictícios:** O banco de dados mock e a massa de testes contêm apenas dados anonimizados e corporações simuladas, sem qualquer exposição de segredos comerciais ou nomes de colaboradores.
