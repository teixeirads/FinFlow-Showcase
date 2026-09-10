  🗺️ Roadmap: Migração FinFlow Showcase

  Fase 1: Infraestrutura de Vitrine (✅ Concluído)
  Fase 2: Engine de Demonstração (✅ Concluído)

  Fase 3: Marketing Técnico (The README)
  - [ ] Passo 5: Construção do README.md de Alto Impacto $\leftarrow$ ESTAMOS AQUI
  - [ ] Passo 6: Curadoria de Assets (Screenshots/GIFs)

  ---

  🚀 Passo 5: O README.md Definitivo

  Abaixo, preparei o conteúdo completo para o seu README.md no repositório de Showcase. Ele foi escrito usando gatilhos mentais que recrutadores sêniores e Tech Leads
  buscam: resolução de problemas, escolhas técnicas justificadas e tangibilidade.

  Instruções:
  1. Vá ao seu repositório Público (FinFlow-Showcase).
  2. Edite o arquivo README.md.
  3. Apague tudo e cole o conteúdo abaixo:

  <div align="center">
    <img src="assets/logo.png" width="120" alt="FinFlow Logo" />
    <h1 align="center">FinFlow 💸</h1>
    <p align="center">
      <strong>Gestão Financeira Inteligente com Foco em Micro-Investimentos e UX Adaptativa</strong>
      <br />
      <a href="https://teixeirads.github.io/FinFlow-Showcase/">
        <img src="https://img.shields.io/badge/🚀_Acesse_a_Live_Demo-blue?style=for-the-badge&logo=flutter" />
      </a>
    </p>

    <p align="center">
      <img src="https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white" />
      <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white" />
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
      <img src="https://img.shields.io/badge/Clean_Architecture-green?style=flat-square" />
    </p>
  </div>

  ---

  ## 🎯 O Problema vs. A Solução

  Muitos aplicativos de finanças pessoais falham devido à **alta fricção no lançamento de despesas** e à falta de engajamento do usuário com seus próprios dados. O
  **FinFlow** foi projetado para eliminar essa barreira.

  **A Solução FinFlow:**
  - **UX de Fluxo Contínuo:** Processo de cadastro e lançamento otimizado para reduzir a carga cognitiva.
  - **Micro-Investimentos (Troco):** Implementação de lógica de arredondamento para investimento automático de trocos, incentivando a poupança passiva.
  - **Inteligência Adaptativa:** Interface que se ajusta ao perfil de risco e objetivos do usuário (Suitability).

  ---

  ## 🏗️ Arquitetura e Decisões Técnicas

  Para garantir escalabilidade e manutenibilidade, o projeto foi construído sob os princípios da **Clean Architecture**, separando rigorosamente as regras de negócio da
  infraestrutura.

  ### Stack Tecnológica
  - **Frontend:** Flutter (Web & Mobile)
  - **Backend as a Service:** Supabase (Auth, Database, Storage)
  - **Banco de Dados:** PostgreSQL
  - **Gerenciamento de Estado:** BLoC / Provider (conforme a complexidade da feature)

  ### Fluxo de Dados
  ```mermaid
  graph LR
    UI[UI Layer] --> BLoC[Business Logic / State]
    BLoC --> Repo[Repository Interface]
    Repo --> Supabase[Supabase Implementation]
    Supabase --> DB[(PostgreSQL)]

  Decisão de Engenharia: Implementei o Repository Pattern. Isso permitiu a criação de um Modo de Demonstração (Mock) para a versão Web, garantindo que a tangibilidade
  do produto seja mantida para stakeholders e recrutadores sem expor dados sensíveis de produção ou chaves de API.

  ---

  🛠️ Por Baixo dos Panos (Code Highlights)

  Como este é um projeto de Propriedade Intelectual (IP), o código-fonte completo é privado. No entanto, abaixo apresento a implementação da camada de abstração de
  dados, demonstrando a aplicação de Inversão de Dependência (DIP):

  // Exemplo de abstração para garantir testabilidade e desacoplamento
  abstract class TransactionRepository {
    Future<List<TransactionEntity>> getRecentTransactions();
  }

  // Implementação Real: Supabase
  class SupabaseTransactionRepository implements TransactionRepository {
    @override
    Future<List<TransactionEntity>> getRecentTransactions() async {
      // Query otimizada via PostgREST
    }
  }

  // Implementação Mock: Versão de Vitrine
  class MockTransactionRepository implements TransactionRepository {
    @override
    Future<List<TransactionEntity>> getRecentTransactions() async {
      return [ /* Dados simulados para a Live Demo */ ];
    }
  }

  ---

  📱 Visualização do Produto

  <div align="center">
    <table border="0">
      <tr align="center">
        <td><img src="assets/screenshots/home.gif" width="250px" /></td>
        <td><img src="assets/screenshots/dashboard.gif" width="250px" /></td>
        <td><img src="assets/screenshots/ai_consultant.gif" width="250px" /></td>
      </tr>
      <tr>
        <td align="center"><b>Home & Saldo</b></td>
        <td align="center"><b>Análise Mensal</b></td>
        <td align="center"><b>Consultor IA</b></td>
      </tr>
    </table>
  </div>

  ---

  <div align="center">
    <sub>Desenvolvido por <strong>Davi Teixeira</strong> | 2026</sub>
  </div>