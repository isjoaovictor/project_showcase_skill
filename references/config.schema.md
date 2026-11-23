# Contrato da configuração por projeto

O JSON é um **contrato editorial de entrada**, não um esquema de validação exaustivo.

- `project.id`: slug de projeto sem espaços.
- `project.name`: grafia oficial.
- `project.tagline`: proposta de valor verificável.
- `project.origin`: história atestada por fonte.
- `brand.colors`: tokens `background`, `foreground`, `accent`, `surface`.
- `brand.typography`: famílias de display e corpo, pesos, capitalização, fallbacks e carregamento; verificar em quais media queries os tokens são efetivos.
- `brand.media`: contexto opcional de apresentação (`desktop|tv|projector|mobile`), distância e viewport de referência; não presumir TV como padrão.
- `brand.presentation`: princípios opcionais de escala semântica (`display`, título, lead, corpo, legenda, controles), proporção texto/imagem e densidade.
- `brand.diagram`: formato e fallback legível quando representar fluxos ramificados, caso necessário.
- `brand.logo`: asset oficial (arquivo relativo), com fallback de texto se não disponível.
- `brand.style`: direção editorial, não regras para outros projetos.
- `experience`: descrição de jornada, agentes, funções e interações desejadas. A lista de capítulos deve corresponder à ordem e à quantidade de telas efetivamente entregues.
- `features[]`: `{name,status,summary,evidence}` com status `implemented|simulated|in_progress|planned|unverified`.
- `technology[]`: `{name,role,reason,status}`.
- `sources[]`: `{name,url,checked_at}`; inclua arquivos locais quando aplicável.
- `constraints`: regras explícitas do projeto, direitos sobre imagens, restrições da apresentação.

Ao criar um showcase, reporte as fontes que sustentam claims do HTML. Nenhum campo deste arquivo autoriza inventar métricas, promessas ou funcionamento.
