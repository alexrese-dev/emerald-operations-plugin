---
name: emerald-operations
description: Consulte e analise operações de COMEX da Emerald com dados do Logline e da planilha. Use para pedidos sobre bookings, BLs, containers, clientes, shipments, divergências, despesas, recebimentos ou análises de várias operações.
---

# Emerald Operations

Use as tools do MCP Emerald Operations para obter dados atuais. As tools apenas consultam e organizam dados; faça a interpretação e a análise solicitadas pelo usuário no modelo.

## Escolha da tool

- Para investigar uma operação específica, use `get_operation_context`. Ele aceita booking, BL, container, cliente ou `ref_logline`. Preserve as diferenças entre Logline e planilha e não assuma automaticamente que uma fonte está correta.
- Para análises amplas envolvendo várias operações, use `get_operations_dataset`. Use `include_*` e `sheets` para consultar somente as fontes relevantes quando possível. Shipments, containers e cada aba possuem paginação independente. Quando `has_more=true` e a solicitação exigir o conjunto completo, continue chamando a tool com o offset correspondente até obter todos os dados necessários.
- Para buscas pontuais, use `search_shipments`, `search_containers` ou `search_spreadsheet`, conforme a fonte solicitada.
- Ao encontrar uma operação durante uma análise ampla e precisar aprofundá-la, use `get_operation_context`.

Mantenha a origem de cada dado identificável. Não faça merge rígido entre Logline e planilha e não invente valores ausentes.
