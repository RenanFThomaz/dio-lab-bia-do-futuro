# 🤖 Primo Bot — Agente Financeiro Inteligente com IA Generativa

> Projeto desenvolvido por [**Renan F. Thomaz**](https://github.com/RenanFThomaz) como parte do BootCamp Bradesco lab da [Digital Innovation One (DIO)](https://github.com/digitalinnovationone/dio-lab-bia-do-futuro).

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![Licença](https://img.shields.io/badge/licença-MIT-blue)
![DIO Lab](https://img.shields.io/badge/DIO-Lab-orange)

## 📌 Sobre o projeto

Os assistentes virtuais no setor financeiro estão deixando de ser simples chatbots reativos para se tornarem **agentes inteligentes e proativos**. Este repositório documenta o desenvolvimento de um agente financeiro que usa **IA Generativa** para:

- 🔮 **Antecipar necessidades** do cliente, em vez de apenas responder perguntas
- 🎯 **Personalizar** sugestões com base no contexto de cada cliente
- 🤝 **Cocriar soluções** financeiras de forma consultiva
- 🛡️ **Garantir segurança** e confiabilidade nas respostas, evitando alucinações

## 🗂️ Estrutura do repositório

```
📁 dio-lab-bia-do-futuro/
│
├── 📄 README.md                      # Este arquivo
│
├── 📁 data/                          # Dados mockados usados pelo agente
│   ├── historico_atendimento.csv     # Histórico de atendimentos
│   ├── perfil_investidor.json        # Perfil e preferências do cliente
│   ├── produtos_financeiros.json     # Produtos financeiros disponíveis
│   └── transacoes.csv                # Histórico de transações
│
├── 📁 docs/                          # Documentação do projeto
│   ├── 01-documentacao-agente.md     # Caso de uso, persona e arquitetura
│   ├── 02-base-conhecimento.md       # Estratégia de dados
│   ├── 03-prompts.md                 # Engenharia de prompts
│   ├── 04-metricas.md                # Avaliação e métricas
│   └── 05-pitch.md                   # Roteiro do pitch
│
├── 📁 src/                           # Código da aplicação
│   └── app.py                        # Protótipo funcional do agente
│
├── 📁 assets/                        # Imagens e diagramas
│
└── 📁 examples/                      # Referências e exemplos de implementação
```

## 🚀 Entregas do desafio

- [ ] **Documentação do agente** — caso de uso, persona, arquitetura e estratégia anti-alucinação (`docs/01-documentacao-agente.md`)
- [ ] **Base de conhecimento** — uso dos dados mockados de `data/` (`docs/02-base-conhecimento.md`)
- [ ] **Prompts do agente** — system prompt, exemplos de interação e tratamento de edge cases (`docs/03-prompts.md`)
- [ ] **Aplicação funcional** — protótipo interativo (`src/app.py`)
- [ ] **Avaliação e métricas** — precisão, taxa de respostas seguras e coerência (`docs/04-metricas.md`)
- [ ] **Pitch** — apresentação de 3 minutos do projeto (`docs/05-pitch.md`)

## 🛠️ Ferramentas utilizadas

| Categoria | Ferramentas |
|---|---|
| **LLM** | Claude / ChatGPT / Gemini / Ollama |
| **Desenvolvimento** | Streamlit / Gradio / Google Colab |
| **Orquestração** | LangChain / LangFlow / CrewAI |
| **Diagramas** | Mermaid / Draw.io / Excalidraw |

## ▶️ Como executar

```bash
# Clone o repositório
git clone https://github.com/RenanFThomaz/dio-lab-bia-do-futuro.git
cd dio-lab-bia-do-futuro

# Crie um ambiente virtual (opcional, mas recomendado)
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Instale as dependências
pip install -r requirements.txt

# Rode a aplicação
streamlit run src/app.py
```

> ⚠️ Ajuste o comando de execução conforme a stack final escolhida (Streamlit, Gradio, etc.) e adicione um `requirements.txt` com as dependências do projeto.

## 📚 Contexto do desafio

Este projeto faz parte do lab **"Bia do Futuro"** da [Digital Innovation One](https://github.com/digitalinnovationone/dio-lab-bia-do-futuro), cujo objetivo é prototipar um agente financeiro consultivo e seguro, capaz de interagir de forma natural com clientes usando dados simulados de transações, atendimentos e perfil de investidor.

## 👤 Autor

**Renan F. Thomaz**
🔗 [github.com/RenanFThomaz](https://github.com/RenanFThomaz)

## 📄 Licença

Este projeto é livre para fins educacionais, seguindo o propósito do lab da DIO.
