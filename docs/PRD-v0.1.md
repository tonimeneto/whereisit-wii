# PRD v0.1 — WhereIsIt (WII)

## 1. Objetivo da Versão

Entregar um **núcleo funcional mínimo** do WhereIsIt (WII) que permita ao criador **usar diariamente** o sistema para localizar arquivos com confiança, respeitando integralmente os guardrails definidos no README.

Esta versão existe para provar que o **core funciona** — não para escalar, vender ou impressionar.

---

## 2. Problema que a v0.1 Resolve

* Arquivos espalhados sem entendimento confiável
* Interpretações invisíveis da IA
* Dificuldade em confiar na busca

A v0.1 resolve **apenas**:

> “Eu sei onde está e sei por que está ali.”

---

## 3. Fluxo Suportado (Canônico)

A versão v0.1 implementa **exatamente** o fluxo:

`RAW → INGESTED → INTERPRETED → REVIEW_REQUIRED → READY`

Sem exceções, atalhos ou estados implícitos.

---

## 4. Funcionalidades Mínimas

### 4.1 Ingestão de Arquivos

* Upload manual de arquivos
* Armazenamento do documento bruto (RAW)
* Geração de hash imutável

### 4.2 Leitura Técnica

* Extração de texto (OCR / parsing quando necessário)
* Normalização básica

### 4.3 Interpretação da IA

* Geração de sugestões:

  * título
  * tags
  * resumo
  * tipo de documento
* Tudo marcado explicitamente como **entendimento da IA**

### 4.4 Revisão Humana

* Interface para visualizar:

  * documento
  * interpretação da IA
* Capacidade de:

  * editar qualquer metadado
  * aceitar ou corrigir sugestões

### 4.5 Estado READY

* Marcação explícita de prontidão
* Apenas arquivos READY:

  * entram na busca

### 4.6 Busca Simples

* Busca textual baseada **somente** em metadados validados
* Nenhum uso de chat
* Nenhuma inferência adicional

---

## 5. Fora de Escopo (NÃO ENTRA NA v0.1)

* ❌ Chat com documentos
* ❌ Perguntas sobre arquivos
* ❌ Integrações externas (Google Drive, OneDrive, etc.)
* ❌ Arquivos locais fora da nuvem
* ❌ Multiusuário
* ❌ Compartilhamento
* ❌ Permissões
* ❌ Cobrança / planos
* ❌ Otimizações de escala
* ❌ Automação de reprocessamento

Se algo desta lista aparecer no código, **o escopo foi violado**.

---

## 6. Requisitos Não-Funcionais

* Todos os estados do arquivo devem ser **visíveis**
* Nenhuma ação automática invisível
* Logs claros de mudança de estado
* Backend como fonte de verdade
* Frontend considerado descartável

---

## 7. Critérios de Aceitação

A v0.1 é considerada **aceita** quando:

* [ ] Consigo subir arquivos reais do meu dia a dia
* [ ] Vejo claramente o que a IA entendeu
* [ ] Consigo corrigir erros sem fricção
* [ ] A busca retorna apenas coisas confiáveis
* [ ] Nunca fico em dúvida se algo foi interpretado ou não
* [ ] Consigo usar por alguns dias sem medo

---

## 8. Riscos Conhecidos

* UX confusa entre interpretação e validação
* Tentação de adicionar chat cedo demais
* Dependência invisível de ferramentas de dev

Esses riscos são mitigados **seguindo estritamente o README**.

---

## 9. Status

Este PRD descreve **exclusivamente** a versão v0.1.

Qualquer mudança de escopo exige:

1. Atualizar o README
2. Atualizar este PRD
3. Só então alterar código
