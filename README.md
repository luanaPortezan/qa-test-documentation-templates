# QA Test Documentation Templates (ISO/IEC/IEEE 29119-3)

Coleção de modelos de documentação para garantia da qualidade de software (QA), estruturados com base no padrão internacional **ISO/IEC/IEEE 29119-3 (Software Testing - Part 3: Test Documentation)**.

Esses templates foram projetados para padronizar o ciclo de relato, rastreabilidade e ciclo de vida de defeitos em ferramentas como Redmine, Jira, Azure DevOps ou documentação técnica de projetos.

---

## 📂 Modelos Disponíveis

### 1. [Relatório Canônico de Defeito (ISO 29119-3 Completo)](./templates/defect-report/modelo_defeito_iso29119_redmine.md)
* **Objetivo:** Registro detalhado com rastreabilidade total, conformidade formal e governança.
* **Cobertura:** Identificação, Rastreabilidade (níveis e tipos de teste), Ambiente detalhado, Severidade/Prioridade, Passos para Reprodução, Evidências, Análise de Causa Raiz, Resolução e Reteste/Sign-off.
* **Recomendado para:** Ambientes regulados, auditorias, UAT formal e testes de aceitação/sistema.

### 2. [Relatório Enxuto de Defeito (Dia a Dia)](./templates/defect-report/modelo_defeito_iso29119_lean_redmine.md)
* **Objetivo:** Registro ágil e direto ao ponto focado na produtividade dos times de desenvolvimento e QA.
* **Cobertura:** Contexto mínimo essencial, Passos para reprodução, Comportamento observado vs. esperado e Evidências.
* **Recomendado para:** Sprints ágeis, rotina diária e gestão de issues no Redmine/Jira.

---

## 🛠️ Como Utilizar
1. Navegue até a pasta `templates/defect-report`.
2. Abra o arquivo desejado e copie o conteúdo em formato Markdown.
3. Cole diretamente no campo de descrição da issue no Redmine, Jira ou issue tracker de sua preferência.