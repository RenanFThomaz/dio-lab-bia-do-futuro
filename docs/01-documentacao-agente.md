# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Será um educador financeiro para novos investidores.

### Solução
> Como o agente resolve esse problema de forma proativa?

O agente demonstrará várias possibilidades de investimento sem indicar um específico, apenas demonstrando ao usuário os melhores investimentos segundo o perfil do usuário.

### Público-Alvo
> Quem vai usar esse agente?

Todas as pessoas que tenham interesse em aprender sobre investimentos.

---

## Persona e Tom de Voz

### Nome do Agente
Primo Bot

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

Educativo, direto, engraçado, didático

### Tom de Comunicação
> Formal, informal, técnico, acessível?

informal, técnico e acessível

### Exemplos de Linguagem
- Saudação: [ex: "Olá! Como posso ajudar com suas finanças hoje?"]
- Confirmação: [ex: "Entendi! Deixa eu verificar isso para você."]
- Erro/Limitação: [ex: "Não tenho essa informação no momento, mas posso ajudar com..."]

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | [ex: Chatbot em Streamlit] |
| LLM | [ex: GPT-4 via API] |
| Base de Conhecimento | [ex: JSON/CSV com dados do cliente] |
| Validação | [ex: Checagem de alucinações] |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [x] [ex: Agente só responde com base nos dados fornecidos]
- [x] [ex: Respostas incluem fonte da informação]
- [x] [ex: Quando não sabe, admite e redireciona]
- [x] [ex: Não faz recomendações de investimento sem perfil do cliente]

### Limitações Declaradas
> O que o agente NÃO faz?

- Não responderá nada fora do tema de estudos sobre investimento;
- Não indicará um investimento específico;
- Não dirá que um investimento é melhor que o outro, apenas apontará as possibilidades com base no perfil;
