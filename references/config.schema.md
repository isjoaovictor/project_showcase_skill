# Contrato da configuração por projeto

O JSON é um **contrato editorial de entrada**, não um esquema de validação exaustivo.

- `project.id`: slug de projeto sem espaços.
- `project.name`: grafia oficial.
- `project.tagline`: proposta de valor verificável.
- `project.origin`: história atestada por fonte.
- `brand.colors`: tokens `background`, `foreground`, `accent`, `surface`.
- `brand.typography`: títulos e texto; preferência por fontes disponíveis ou fallbacks.
- `brand.logo`: asset oficial (arquivo relativo), com fallback de texto se não disponível.
- `brand.style`: direção editorial, não regras para outros projetos.
- `experience`: descrição de jornada, agentes, funções e interações desejadas.
- `features[]`: `{name,status,summary,evidence}` com status `implemented|simulated|in_progress|planned|unverified`.
- `technology[]`: `{name,role,reason,status}`.
- `sources[]`: `{name,url,checked_at}`; inclua arquivos locais quando aplicável.
- `constraints`: regras explícitas do projeto, direitos sobre imagens, restrições da apresentação.

Ao criar um showcase, reporte as fontes que sustentam claims do HTML. Nenhum campo deste arquivo autoriza inventar métricas, promessas ou funcionamento.
