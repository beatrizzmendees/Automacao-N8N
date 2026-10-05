# Relatório de Vendas Automático (n8n)

Workflow simples no n8n que lê a base de vendas de uma planilha do Google Sheets, resume o valor vendido por produto e envia o resultado por e-mail em um arquivo Excel.

## Fluxo

```
Manual Trigger → Google Sheets → Summarize → Convert to File → Gmail
```

| Nó | O que faz |
|---|---|
| **Manual Trigger** | Inicia o fluxo ao clicar em *Execute workflow* |
| **Get row(s) in sheet** | Lê todas as linhas da aba `Vendas` da planilha `Base de Vendas` |
| **Summarize** | Soma a coluna `Valor Total`, agrupando por `Produto` |
| **Convert to File** | Converte o resumo em um arquivo `.xlsx` ("Relatório de Vendas") |
| **Send a message** | Envia o arquivo como anexo por e-mail (Gmail) |

## Pré-requisitos

- Instância do n8n (cloud ou self-hosted)
- Credencial **Google Sheets OAuth2**
- Credencial **Gmail OAuth2**
- Planilha com as colunas `Produto` e `Valor Total`

Feito apenas para entender um pouco do N8N.
