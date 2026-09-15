# Graph Report - finflow-showcase  (2026-09-11)

## Corpus Check
- Corpus is ~430 words - fits in a single context window. You may not need a graph.

## Summary
- 33 nodes · 32 edges · 7 communities (4 shown, 3 thin omitted)
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Experiência e Stack FinFlow
- Abstração e Testabilidade
- Fluxo de Dados
- Arquitetura do Modo Demo
- Personalização por Suitability
- Clean Architecture
- UX Financeira sem Fricção

## God Nodes (most connected - your core abstractions)
1. `FinFlow` - 14 edges
2. `Data Abstraction Layer` - 4 edges
3. `TransactionRepository` - 4 edges
4. `MockTransactionRepository` - 3 edges
5. `Continuous Flow UX` - 2 edges
6. `Adaptive Intelligence` - 2 edges
7. `Clean Architecture` - 2 edges
8. `PostgreSQL` - 2 edges
9. `Business Logic / State` - 2 edges
10. `Repository Interface` - 2 edges

## Surprising Connections (you probably didn't know these)
- `FinFlow` --implements--> `Adaptive Intelligence`  [EXTRACTED]
  README.md → README.md  _Bridges community 0 → community 4_
- `FinFlow` --implements--> `Clean Architecture`  [EXTRACTED]
  README.md → README.md  _Bridges community 0 → community 5_
- `FinFlow` --implements--> `Continuous Flow UX`  [EXTRACTED]
  README.md → README.md  _Bridges community 0 → community 6_
- `FinFlow` --references--> `PostgreSQL`  [EXTRACTED]
  README.md → README.md  _Bridges community 0 → community 2_
- `FinFlow` --implements--> `Repository Pattern`  [EXTRACTED]
  README.md → README.md  _Bridges community 0 → community 3_

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **FinFlow Core Experience** — readme_continuous_flow_ux, readme_micro_investments, readme_adaptive_intelligence [EXTRACTED 1.00]
- **Clean Architecture Data Flow** — readme_ui_layer, readme_business_logic_state, readme_repository_interface, readme_supabase_implementation, readme_postgresql [EXTRACTED 1.00]
- **Transaction Repository Implementations** — readme_transactionrepository, readme_supabasetransactionrepository, readme_mocktransactionrepository [EXTRACTED 1.00]

## Communities (7 total, 3 thin omitted)

### Community 0 - "Experiência e Stack FinFlow"
Cohesion: 0.20
Nodes (10): AI Consultant, BLoC, FinFlow, Flutter, Home & Balance, Micro-Investments (Spare Change), Monthly Analysis, Provider (+2 more)

### Community 1 - "Abstração e Testabilidade"
Cohesion: 0.25
Nodes (8): Data Abstraction Layer, Decoupling, Dependency Inversion Principle, PostgREST, SupabaseTransactionRepository, Testability, TransactionEntity, TransactionRepository

### Community 2 - "Fluxo de Dados"
Cohesion: 0.40
Nodes (5): Business Logic / State, PostgreSQL, Repository Interface, Supabase Implementation, UI Layer

### Community 3 - "Arquitetura do Modo Demo"
Cohesion: 0.50
Nodes (4): Demo Mode (Mock), MockTransactionRepository, Repository Pattern, Simulated Demo Data

## Knowledge Gaps
- **16 isolated node(s):** `Expense Entry Friction`, `User Disengagement from Financial Data`, `Suitability`, `Flutter`, `Supabase` (+11 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **3 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `FinFlow` connect `Experiência e Stack FinFlow` to `Fluxo de Dados`, `Arquitetura do Modo Demo`, `Personalização por Suitability`, `Clean Architecture`, `UX Financeira sem Fricção`?**
  _High betweenness centrality (0.841) - this node is a cross-community bridge._
- **Why does `Repository Pattern` connect `Arquitetura do Modo Demo` to `Experiência e Stack FinFlow`?**
  _High betweenness centrality (0.466) - this node is a cross-community bridge._
- **What connects `Expense Entry Friction`, `User Disengagement from Financial Data`, `Suitability` to the rest of the system?**
  _16 weakly-connected nodes found - possible documentation gaps or missing edges._