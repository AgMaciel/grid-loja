# Relatório Quantitativo de Análise de Pontos de Função (APF) — SAA v3

Com base no "Roteiro de Análise de Pontos de Função (APF) e Aprimoramento Técnico — SAA v3" fornecido e aplicando as tabelas de pesos padrão do IFPUG (International Function Point Users Group), foi realizado o cálculo dos Pontos de Função Brutos (PFB) do sistema SAA v3.

---

## 1. Pesos Padrão IFPUG Utilizados

Para referência, os pesos aplicados para cada tipo de função e complexidade são:

| Tipo | Baixa | Média | Alta |
|:---|:---:|:---:|:---:|
| **ALI** (Arquivo Lógico Interno) | 7 | 10 | 15 |
| **AIE** (Arquivo de Interface Externa) | 5 | 7 | 10 |
| **EE** (Entrada Externa) | 3 | 4 | 6 |
| **SE** (Saída Externa) | 4 | 5 | 7 |
| **CE** (Consulta Externa) | 3 | 4 | 6 |

---

## 2. Quantitativos: Funções de Dados

As funções de dados medem os repositórios lógicos de informações mantidos ou referenciados pelo sistema.

| Tipo | Nome | Descrição | Complexidade | Pontos de Função (PF) |
|:---:|:---|:---|:---:|:---:|
| **ALI** | `users` | Dados de usuários e perfis administrativos | Baixa | 7 |
| **ALI** | `students` | Cadastro completo de discentes e responsáveis | Média | 10 |
| **ALI** | `occurrences` | Registros de fatos e evidências | Média | 10 |
| **ALI** | `processes` | Processos disciplinares (Modelo complexo) | Alta | 15 |
| **AIE** | `Google Auth`| Dados de identidade providos externamente | Baixa | 5 |
| \multicolumn{4}{|r|}{\textbf{Subtotal (Funções de Dados)}} | **47 PF** |

---

## 3. Quantitativos: Funções de Transação

As funções de transação medem os processos elementares que cruzam a fronteira do sistema.

| Tipo | Nome | Descrição | Complexidade | Pontos de Função (PF) |
|:---:|:---|:---|:---:|:---:|
| **EE** | `signInWithEmail` | Entrada de dados para autenticação | Baixa | 3 |
| **EE** | `addStudent` | Inclusão de novo discente | Baixa | 3 |
| **EE** | `addOccurrence` | Registro de fato com upload de evidências | Média | 4 |
| **EE** | `addProcess` | Abertura de processo automática | Alta | 6 |
| **CE** | `getStudent` | Consulta de perfil por ID | Baixa | 3 |
| **SE** | `PdfNotification` | Geração de documento formal (notificação PDF) | Média | 5 |
| **SE** | `Statistics` | Relatório de distribuição de alunos | Alta | 7 |
| \multicolumn{4}{|r|}{\textbf{Subtotal (Funções de Transação)}} | **31 PF** |

---

## 4. Resumo e Tamanho Funcional

Somando as Funções de Dados e as Funções de Transação identificadas no escopo, temos o tamanho funcional total do sistema medido.

| Categoria | Subtotal de Pontos de Função |
|:---|:---:|
| **Funções de Dados** (ALI + AIE) | 47 PF |
| **Funções de Transação** (EE + SE + CE) | 31 PF |
| **Tamanho Funcional Total (PFB)** | **78 Pontos de Função** |

### Conclusão

O escopo avaliado do SAA v3, conforme as métricas identificadas no roteiro, totaliza **78 Pontos de Função Brutos (PFB)**. Esse quantitativo pode ser utilizado para:
1. **Estimativa de Esforço e Custo:** Cruzando esse valor com a produtividade da equipe (ex: horas/PF).
2. **Medição de Produtividade:** Avaliando a entrega do time no decorrer das sprints (caso convertido em pontos ágeis ou mantido em PF).
3. **Contratos de TI:** Precificação em cenários governamentais que exijam métrica de software padrão IFPUG.
