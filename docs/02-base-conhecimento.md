# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | Utilização no Agente |
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
perfil = json.load(open('./data/perfil_investidor.json'))
transacoes - pd.read.csv('./data/historico_atendimento.csv')
gistorico = pd.read.csv('./data/historico_atendimento.csv')
produtos = json.load(open('./data/produtos_financeiros.json'))
```


### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

with open('./data/perfil_investidor.json', encoding='utf-8') as f:
    perfil = json.load(f)

transacoes = pd.read_csv('./data/transacoes.csv')
historico = pd.read_csv('./data/historico_atendimento.csv')

with open('./data/produtos_financeiros.json', encoding='utf-8') as f:
    produtos = json.load(f)
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
