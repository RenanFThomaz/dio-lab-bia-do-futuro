# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | função |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores |
| `perfil_investidor.json` | JSON | Personalizar recomendações |
| `produtos_financeiros.json` | JSON | Sugerir produtos adequados ao perfil |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente |

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

Nesse primeiro momento estou usando apenas os dados fornecidos préviamente.

---

## Estratégia de Integração

### Como os dados são carregados?
> Os dados são importados no começo da aplicação e são incluidos no contexto do prompt

 
```python
with open('./data/perfil_investidor.json', encoding='utf-8') as f:
    perfil = json.load(f)

transacoes = pd.read_csv('./data/transacoes.csv')
historico = pd.read_csv('./data/historico_atendimento.csv')

with open('./data/produtos_financeiros.json', encoding='utf-8') as f:
    produtos = json.load(f)
```


### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

```text
Dados do cliente:
Perfil do cliente:
Transações do cliente:
Produtos financeiros para ensino:
---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Dados do Cliente:
- Nome: João Silva
- Perfil: Moderado
- Saldo disponível: R$ 5.000

Últimas transações:
- 01/11: Supermercado - R$ 450
- 03/11: Streaming - R$ 55
...
```
