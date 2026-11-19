# Execução PDV — arquivos para publicar

Envie para a raiz do repositório no GitHub **somente** estes arquivos:

- index.html
- sw.js
- manifest.webmanifest
- icon-192.png, icon-512.png, apple-touch-icon.png (ícones da Tela de Início)

O `config-pdv.json` fica na pasta `NAO-PUBLICAR` e deve ir direto para o iPhone (app Arquivos → Ajustes do Execução PDV).

## Estrutura do config-pdv.json
- `distribuidores`: lista de nomes.
- `bandeiras`: `{ "nome", "canal" }` — o canal define qual tabela de preço é usada.
- `produtos`: `{ "sku", "nome" }`.
- `precos`: `{ "<canal>": { "<sku>": preço } }`.
- `toleranciaPrecoPct`: diferença aceitável entre preço coletado e tabela.
- `oportunidades`: itens marcados como Executado / Não / N/A.
- `contratos`: por bandeira; cada obrigação é `"tipo": "quantitativa"` (com `meta` e `unidade`, cálculo proporcional limitado a 100%) ou `"tipo": "sim_nao"`.
