# Emerald Operations

Plugin do Claude para consultar e analisar operações de COMEX da Emerald, incluindo shipments, containers e dados da Logline e da planilha Emerald.

O plugin usa exclusivamente o MCP remoto:

~~~text
https://mcp.emeraldcoast.group/mcp
~~~

## Instalação no Claude Code

Baixe ou clone este diretório e inicie o Claude Code carregando o plugin:

~~~bash
claude --plugin-dir caminho/para/emerald-operations-plugin
~~~

No Claude Code, execute /mcp para confirmar que emerald-operations está conectado.

## Autenticação

Na primeira conexão, abra /mcp, selecione emerald-operations e conclua o fluxo OAuth do Auth0 com a conta Google autorizada pela Emerald. Tokens e credenciais não devem ser adicionados a este repositório.

## Exemplos de uso

- “Analise o booking informado.”
- “Veja os containers desse booking.”
- “Compare Logline e planilha dessa operação.”
- “Analise todas as operações disponíveis.”
- “Compare recebimentos SWIFT e cripto.”
- “Procure inconsistências gerais entre Logline e planilha.”

## Backend

Este repositório contém somente o pacote do plugin. O backend, as integrações de dados e a autenticação são operados separadamente no MCP remoto e não fazem parte deste repositório.
