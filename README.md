# 🛡️ Miniguia de Estudos: Cibersegurança em Aplicações de Inteligência Artificial

> Projeto prático desenvolvido para o desafio da **DIO (Digital Innovation One)** utilizando o **NotebookLM** como ferramenta de aprendizagem ativa.

---

## 📌 Contexto e Objetivos

### Contexto
O avanço acelerado da Inteligência Artificial Generativa e dos Modelos de Linguagem de Grande Porte (LLMs) trouxe novas eficiências, mas também novos vetores de ataque. Este repositório documenta a construção de um Caderno Temático no **NotebookLM** voltado para a **Cibersegurança em Aplicações de IA**, explorando como proteger modelos, mitigar vulnerabilidades e garantir a privacidade dos dados.

### Objetivos de Estudo
- Compreender os principais riscos de segurança específicos para sistemas baseados em IA (ex: OWASP Top 10 para LLMs).
- Investigar técnicas de mitigação contra ataques adversariais, *prompt injection* e envenenamento de dados.
- Utilizar o NotebookLM para síntese, curadoria de conhecimento e análise crítica de artigos e relatórios técnicos do setor.

---

## 📚 Curadoria de Fontes

Para alimentar o caderno temático no NotebookLM, foram selecionadas as seguintes fontes abertas e relatórios técnicos de referência:

1. **OWASP Top 10 for Large Language Model Applications**
   - *Fonte:* OWASP Foundation
   - *Descrição:* Documento de referência com as 10 principais vulnerabilidades de segurança em aplicações que utilizam LLMs.
2. **NIST AI Risk Management Framework (AI RMF 1.0)**
   - *Fonte:* National Institute of Standards and Technology (NIST)
   - *Descrição:* Diretrizes para gerenciamento de riscos, confiabilidade e segurança em sistemas de IA.
3. **MITRE ATLAS™ (Adversarial Threat Landscape for Artificial-Intelligence Systems)**
   - *Fonte:* MITRE
   - *Descrição:* Base de conhecimento de táticas e técnicas de invasores contra sistemas habilitados para IA.

---

## 🧠 Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Nesta seção, estão registrados os testes de prompts aplicados no NotebookLM, as análises de respostas e os ajustes realizados durante a interação.

### Teste 1: Síntese de Vulnerabilidades
* **Prompt Inicial:** *"Quais são os principais ataques em IA?"*
* **Resultado Obtido:** A resposta foi muito geral, cobrindo segurança da informação tradicional sem focar nas especificidades de LLMs.
* **Ajuste / Refinamento:** *"Com base nos documentos carregados (especialmente a OWASP Top 10 para LLMs), enumere os 3 principais vetores de ataque específicos para Large Language Models e explique brevemente a diferença entre Prompt Injection e Data Poisoning."*
* **Lição Aprendida:** Especificar a fonte e pedir diferenciações diretas ajuda a IA do NotebookLM a ancorar as respostas estritamente no material curado.

### Teste 2: Aplicação Prática de Defesa
* **Prompt Inicial:** *"Como resolver prompt injection?"*
* **Resultado Obtido:** Resposta com dicas Genéricas de código.
* **Ajuste / Refinamento:** *"A partir do framework do NIST AI RMF presente nas fontes, quais são as medidas defensivas recomendadas na camada de entrada (input validation) e na camada de saída (output sanitization) para conter ataques de Prompt Injection?"*
* **Lição Aprendida:** Delimitar o escopo em "camadas de entrada e saída" gerou um checklist técnico muito mais acionável.

---

## 📖 Miniguia de Estudo (Entrega Final)

### 1. Resumo Estruturado do Assunto

A segurança em aplicações de IA exige uma abordagem de **defesa em profundidade**, cobrindo todo o ciclo de vida do modelo:

* **Fase de Treinamento/Ajuste Fino:** Proteção contra *Data Poisoning* (garantindo a integridade da base de dados utilizada).
* **Fase de Inferência/Aplicação:**
  * **Input Layer:** Filtros e sanitização contra *Direct* e *Indirect Prompt Injection*.
  * **Model/System Layer:** Controle de acessos, limitação de permissões de APIs conectadas e sandboxing.
  * **Output Layer:** Validação de respostas para evitar vazamento de dados sensíveis (*Sensitive Information Disclosure*).

---

### 2. Glossário de Conceitos Aprendidos

| Conceito | Descrição Breve |
| :--- | :--- |
| **Prompt Injection** | Técnica onde um atacante manipula a instrução dada ao LLM para burlar restrições e executar comandos não autorizados. |
| **Data Poisoning** | Manipulação maliciosa dos dados de treinamento do modelo para introduzir vieses, portas dos fundos (backdoors) ou comportamentos incorretos. |
| **Model Inversion Attack** | Ataque que tenta reconstruir os dados privados originais de treinamento a partir das respostas do modelo. |
| **OWASP Top 10 for LLMs** | Lista padrão da comunidade destacando as vulnerabilidades de maior impacto em sistemas baseados em LLM. |

---

### 3. Prompts Reutilizáveis para Revisão Futura

Estes prompts foram desenhados para serem reutilizados no NotebookLM em revisões periódicas do tema:

* 🔄 **Revisão de Conceito:** *"Crie um questionário de 5 perguntas de múltipla escolha sobre [Tópico, ex: Prompt Injection] com gabarito comentado com base nas fontes."*
* 🔍 **Análise de Cenário:** *"Atue como um analista de segurança. Avalie o seguinte cenário de integração de IA [Descrever cenário] e identifique os 2 maiores riscos segundo a OWASP."*
* 📝 **Resumo Executivo:** *"Gere um resumo em tópicos focado em mitigação de riscos de privacidade para apresentar a uma equipe técnica."*

---

## 🛠️ Ferramentas Utilizadas
* [NotebookLM](https://notebooklm.google.com/) - Curadoria e inteligência de estudo
* [GitHub](https://github.com/) - Documentação e portfólio
