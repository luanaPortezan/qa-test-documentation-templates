# RELATÓRIO DE DEFEITO (DEFECT REPORT)
*Em conformidade com a norma ISO/IEC/IEEE 29119-3:2013 (Software and systems engineering — Software testing — Part 3: Test documentation)*

---

## 1. Identificação e Metadados do Documento (Document Identification)

| Campo | Descrição / Valor |
| :--- | :--- |
| **ID Único do Defeito:** | `[DEF-YYYYMMDD-XXXX]` |
| **Título/Resumo:** | `[Breve declaração indicando a falha observada e o componente afetado]` |
| **Versão do Documento:** | `1.0` |
| **Data/Hora do Relato:** | `YYYY-MM-DD HH:mm` |
| **Autor/Relator (Reported By):** | `[Nome do Relator / Papel no Projeto]` |
| **Proprietário/Atribuído a (Assignee):** | `[Nome do Desenvolvedor / Responsável pela Análise]` |
| **Organização / Projeto:** | `[Nome do Projeto / Módulo]` |
| **Status Atual:** | `[ Novo / Aberto / Em Investigação / Em Correção / Pronto para Reteste / Reteste Concluído / Fechado / Reaberto / Rejeitado / Adiado ]` |

---

## 2. Contexto e Rastreabilidade do Teste (Context & Traceability)

| Referência | Detalhes |
| :--- | :--- |
| **Nível de Teste:** | `[ ] Teste de Componente / Unidade<br>[ ] Teste de Integração<br>[ ] Teste de Sistema<br>[ ] Teste de Aceitação (UAT / Operacional)` |
| **Tipo de Teste:** | `[ ] Funcional<br>[ ] Não Funcional (Performance, Carga, Usabilidade, Segurança, Compatibilidade, etc.)<br>[ ] Estrutural / Caixa Branca` |
| **Item de Teste (Test Item):** | `[Nome do Artefato/Módulo, ex.: Módulo de Autenticação v2.4.1]` |
| **Requisitos / Histórias Relacionadas:** | `[ID do Requisito, User Story ou Épico, ex.: REQ-1042 / #4521]` |
| **Especificação / Caso de Teste:** | `[ID do Caso de Teste, ex.: TC-AUTH-032 / Procedimento de Teste]` |
| **Execução de Teste (Test Execution):** | `[ID da Execução ou Ciclo de Teste, ex.: RUN-2026-CYCLE-03]` |

---

## 3. Ambiente de Teste (Test Environment)

*Especificação exata da configuração onde o defeito foi identificado:*

* **Hardware / Host:** `[ex.: Servidor x86_64, Dispositivo Móvel Galaxy S23, Máquina Local]`
* **Sistema Operacional / Plataforma:** `[ex.: Ubuntu 24.04 LTS / Windows 11 Enterprise / iOS 17.5]`
* **Navegador / Cliente / Runtime:** `[ex.: Google Chrome 128.0.x / OpenJDK 21 / Node.js 20.x]`
* **Versão/Build do Sistema:** `[ex.: Build #452 (commit sha: a1b2c3d4)]`
* **Base de Dados:** `[ex.: PostgreSQL 16.2 - Snapshot/Dump de Homologação sanitizado v1.2]`
* **Configurações Específicas / Dependências:** `[ex.: Integração com Gateway Sandbox ativo, mock de e-mail habilitado]`

---

## 4. Classificação de Impacto (Defect Classification)

| Dimensão | Classificação Atribuída | Justificativa |
| :--- | :--- | :--- |
| **Severidade (Severity):** | `[ ] Crítica (Catastrófica)<br>[ ] Alta (Grave)<br>[ ] Média (Moderada)<br>[ ] Baixa (Mínima)` | *[Impacto técnico sobre o sistema, integridade de dados ou continuidade operacional]* |
| **Prioridade (Priority):** | `[ ] Urgente (Imediata)<br>[ ] Alta<br>[ ] Normal / Média<br>[ ] Baixa` | *[Urgência de negócio / agendamento para resolução]* |

---

## 5. Descrição Detalhada da Anomalia (Defect Description)

### 5.1 Pré-condições (Preconditions)
1. `[Condição prévia 1, ex.: Usuário autenticado com perfil de Gestor]`
2. `[Condição prévia 2, ex.: Registro com pendência cadastral existente]`

### 5.2 Passos para Reprodução (Steps to Reproduce)
1. `Acesse o menu [...]`
2. `Selecione a opção [...]`
3. `Preencha o campo [X] com o valor [Y]`
4. `Clique no botão [Confirmar]`

### 5.3 Resultado Observado (Actual Result)
> `[Descrever com exatidão o que aconteceu de fato. Incluir mensagens de erro literais, códigos HTTP ou exceções capturadas.]`

### 5.4 Resultado Esperado (Expected Result)
> `[Descrever o comportamento correto esperado, conforme as especificações de requisitos ou regras de negócio.]`

### 5.5 Reprodutibilidade (Reproducibility)
* `[ ] Sempre (100%)`
* `[ ] Frequente (~75%)`
* `[ ] Intermitente (<50%)`
* `[ ] Não reproduzido após primeira ocorrência`

---

## 6. Evidências e Anexos (Evidence & Attachments)

* **Logs do Sistema / Console:** `[Anexar ou referenciar log, ex.: server_error_20260922.log]`
* **Capturas de Tela / Gravação:** `[Screenshot_01.png, video_reproducao.mp4]`
* **Dados de Teste Utilizados:** `[Ex.: Payload JSON, arquivo CSV de entrada ou IDs de entidades usadas]`
* **Dump de Memória / Stack Trace:**
```text
[Cole a Stack Trace completa aqui, se aplicável]
```

---

## 7. Análise de Causa Raiz e Impacto (Root Cause & Scope Analysis)
*(Preenchido durante o diagnóstico técnico / desenvolvimento)*

* **Causa Raiz Suspeita / Confirmada:** `[ex.: Falha na sanitização de payload, condição de corrida no thread pool, inconsistência de chave estrangeira]`
* **Itens/Componentes Impactados:** `[Lista de outros módulos ou serviços afetados]`
* **Impacto em Regressão / Risco Sistêmico:** `[Grau de risco colateral associado à correção]`

---

## 8. Resolução e Conclusão (Resolution & Closeout)

| Campo | Detalhes |
| :--- | :--- |
| **Tipo de Resolução:** | `[ ] Código Corrigido<br>[ ] Comportamento Conforme Especificação (Não é defeito)<br>[ ] Duplicado (Ref. Defeito: #____)<br>[ ] Não Reproduzível<br>[ ] Adiado / Deferido para Release Futura<br>[ ] Documentação Atualizada` |
| **Build de Correção (Fixed in Build):** | `[ex.: v2.4.2-rc1 / Build #460]` |
| **Notas da Correção / Commit:** | `[Hash do commit e resumo técnico da mudança aplicada]` |
| **Responsável pela Resolução:** | `[Nome do Desenvolvedor]` |
| **Data da Resolução:** | `YYYY-MM-DD` |

---

## 9. Histórico de Verificação e Reteste (Retest & Sign-Off)

* **Data do Reteste:** `YYYY-MM-DD`
* **Testador Responsável:** `[Nome do QA / Analista de Testes]`
* **Ambiente / Build de Reteste:** `[ex.: Homologação - Build #460]`
* **Resultado do Reteste:** `[ ] Aprovado (Pass) / [ ] Reprovado (Fail / Reaberto)`
* **Evidência do Reteste:** `[Link/Anexo da execução de sucesso]`
* **Parecer Final / Conclusão:** `[Defeito considerado encerrado e validado em conformidade com os critérios de aceite.]`
