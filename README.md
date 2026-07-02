# 📦 Controle de Validades

Aplicação web simples, em um único arquivo HTML, para cadastrar produtos e acompanhar suas datas de validade. Feita para o dia a dia de uma cozinha/confeitaria: mostra rapidamente o que já venceu, o que vence nos próximos 7 dias e o que está dentro do prazo.

## Como usar

Acesse o site publicado: **https://hugoalonsosinatra-cyber.github.io/controle-validades/**

Ou, se preferir usar localmente, basta abrir o arquivo [`index.html`](index.html) em qualquer navegador moderno (Chrome, Edge, Firefox) — não precisa instalar nada.

Os dados ficam salvos no próprio navegador (localStorage). Ou seja: cada navegador/computador tem a sua própria lista. Para levar os dados de um lugar para outro, use os botões **Exportar CSV** e **Importar**.

## Funcionalidades

- **Cadastro de produtos** com nome, categoria, quantidade e data de validade
- **Painel de estatísticas** clicável: total, vencidos, vencendo em 7 dias e dentro do prazo
- **Filtros combináveis**: busca por nome/categoria, data exata de validade, "vence em até X dias" e status
- **Edição e exclusão** de produtos direto na tabela
- **Exportar/Importar CSV** (separado por `;`, compatível com Excel) para backup ou migração entre dispositivos
- **Layout responsivo** — funciona no celular

## Arquivos

| Arquivo | Descrição |
| --- | --- |
| `index.html` | A aplicação completa (HTML + CSS + JavaScript, sem dependências) |
| `produtos_iniciais.csv` | Lista inicial de produtos para importar pela função **Importar** |

## Formato do CSV

O CSV usa `;` como separador, com cabeçalho na primeira linha:

```csv
"nome";"categoria";"quantidade";"validade"
"Leite condensado 5k";"";"1";"2026-08-26"
```

- `nome` e `validade` são obrigatórios; a validade deve estar no formato `AAAA-MM-DD`
- Linhas duplicadas (mesmo nome e mesma validade) são ignoradas na importação
