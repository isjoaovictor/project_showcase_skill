# Escala, tipografia e mídia de apresentação

Estas orientações são reutilizáveis, mas **não impõem fontes, cores, layouts ou tamanhos do exemplo Coxinh.IA**. Comece consultando o design system original do projeto e o contexto de exibição.

## Auditoria antes de criar

1. Identifique tokens, estilos, mídia de destino, fontes, assets, capítulos e conteúdos.
2. Compare fontes importadas com `font-family` realmente aplicado. Inspecione especificidade, media queries e estilos computados quando possível.
3. Examine capitalização literal no HTML e regras `text-transform`. Uma declaração `text-transform: none` não corrige HTML escrito em caixa alta.
4. Se houver mudanças recentes, consulte diffs e commits. Não atribua a uma revisão alterações que o histórico não comprove.
5. Preserve o que já funciona; mude apenas com melhoria justificável.

## Sistema tipográfico

* Papéis explícitos: display, título de capítulo, subtítulo, lead, corpo, legenda, metadados e controles.
* Prefira capitalização natural em títulos editoriais, reservando caixa alta para rótulos curtos ou exigências da marca.
* Escolha famílias atuais e coerentes com a identidade, com pesos e fallbacks. Não adote Space Grotesk ou Manrope por padrão.
* Ajuste `font-size`, `line-height`, `letter-spacing`, medida do texto e largura das colunas como sistema único. Teste títulos e legendas longos.
* Defina escalas com tokens semânticos e, quando adequado, `clamp()` e media queries. Evite novos overrides contraditórios.
* Contraste e hierarquia devem ser comunicados também por peso e tamanho, não apenas por cor.

## TV e projeção

Se o usuário indicar exibição em TV, projetor ou a alguns metros de distância:

* Defina mídia e viewport de referência, por exemplo 1920×1080 em 16:9. Confirme a viewport CSS real, pois regras por largura/altura não detectam TV.
* Amplie não só títulos, mas corpo explicativo, rótulos, controles, tabelas, passos e diagramas.
* Ajuste as imagens em conjunto com os textos: escala, nitidez, proporção, recorte, posição e espaço negativo.
* Priorize os capítulos que o usuário indicar, mantendo coerência transversal.
* Verifique sobreposição de títulos, quebra de linhas, áreas cortadas e se o conteúdo cabe na altura útil. Não alegue que uma tela cabe inteira sem testar.
* Se crescer demais, reequilibre as colunas e a composição; não apague conteúdo validado sem permissão.

## Fluxos e dependências externas

* Quando houver decisões, loops e retornos, um diagrama com rotas explícitas (Mermaid, SVG ou equivalente) pode comunicar melhor do que cartões com atores. Escolha conforme a complexidade real.
* Recursos remotos (fontes, Mermaid, imagens) precisam ter fallback ou restrição de conectividade explicitada. Não deixe código Mermaid cru como única experiência em caso de falha quando uma versão offline for requisito.
* Se um capítulo for adicionado, atualize contagem, ordem, navegação, README e configuração; evite fontes de verdade contraditórias.

## Validação

1. Verifique o resultado renderizado no(s) viewport(s) alvo: fonte carregada, estilos computados, linhas e overflow.
2. Confira desktop intermediário e estados dinâmicos, especialmente fontes que mudam por breakpoint.
3. Inspecione contraste, imagem preservada, responsividade básica e `prefers-reduced-motion`.
4. Separe testes realmente executados de inferências extraídas do código.
5. Não invente comparações visuais antes/depois sem capturas ou histórico verificável.

## Aprendizado documentado do Coxinh.IA

No snapshot de 23/11/2026, o showcase incorporou Manrope para corpo e Space Grotesk para títulos em viewport >=1200px por >=700px, com ampliação semântica de textos e controles e capitalização natural em títulos. O design também passou a ter **oito telas**, com uma tela de fluxo Mermaid em sétimo lugar e status do projeto na oitava. A media query não vale para todas as dimensões; o carregamento das fontes depende da rede, e o Mermaid depende de CDN. Essas são observações do exemplo, não comportamentos obrigatórios da skill.
