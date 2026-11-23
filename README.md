# Project Showcase · Skill reutilizável

Skill em formato Agent Skills para gerar apresentações narrativas, visuais e interativas de projetos de software. **Não é um curso nem um gerador de exercícios.**

## Instalação no Codex

Em um repositório, coloque a pasta `project-showcase` inteira dentro de `.agents/skills/` (ela deve conter `SKILL.md` na raiz). O agente a descobre nesse contexto. Para instalar no escopo pessoal, use o diretório pessoal de skills do cliente instalado, conforme sua configuração.

No Claude Code e em outros agentes compatíveis, consulte a localização de skills suportada pelo seu cliente. O formato `SKILL.md` é reaproveitável, mas a instalação varia por produto.

## Como usar

Peça ao agente:

> Use a skill `project-showcase` para ler o README, o guia de identidade e os componentes relevantes deste repositório. Crie um showcase HTML interativo que conte a origem do projeto, mostre o funcionamento com simulações identificadas e explique as tecnologias pelo propósito. Use estritamente a identidade do projeto, não crie exercícios ou quizzes e diferencie implementado, simulado e planejado. Não altere o produto.

## Exemplo incluído

`examples/coxinh-ia/showcase.config.json` traz a identidade visual, histórias e regras de apresentação do Coxinh.IA. `examples/coxinh-ia/showcase.html` é uma demonstração estática interativa **independente do backend**. Abra esse HTML no navegador.

O arquivo de exemplo usa uma assinatura textual estilizada com a grafia do projeto. Para a versão final da marca, importe o logotipo existente em `docs/design/` conforme o `design.md` do repositório; ele não foi copiado para este pacote.

## Arquivos

- `SKILL.md`: gatilhos, entradas, regras e fluxo de execução da skill.
- `references/narrative.md`: como transformar fatos em narrativa de produto.
- `references/visual-and-interaction.md`: experiência visual e regras de interação.
- `references/config.schema.md`: contrato do JSON específico de cada projeto.
- `references/quality-gates.md`: revisão final.
- `examples/coxinh-ia/`: caso concreto de aplicação, sem contaminar o comportamento genérico.

## Fontes do exemplo

- [README do Coxinh.IA](https://github.com/Caio-GBrayner/Coxinh.IA/blob/main/README.md)
- [Design do Coxinh.IA](https://github.com/Caio-GBrayner/Coxinh.IA/blob/main/docs/design/design.md)
- [Referência de interação: slides.html](https://github.com/Theteu1/Semana-3-Bootcamp/blob/main/slides.html)

Conteúdo conferido em 22/11/2026. O HTML é um snapshot editorial e não acompanha automaticamente atualizações futuras do repositório. A skill, quando executada novamente, deve verificar os arquivos atuais.
