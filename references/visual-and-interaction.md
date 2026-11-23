# Direção de arte e interação

## Identidade

1. Priorize o arquivo de identidade visual da fonte. Reuse logos e fotografias existentes; não crie aproximações com marcas conhecidas.
2. Defina tokens CSS de cor, família de títulos, família de texto, escala, raios, espaçamento e duração de animação; evite espalhar cores hardcoded por componentes. Registre se o projeto já tem tokens e *não os substitua apenas por estilo*. Verifique se fontes carregadas são efetivamente usadas nas regras CSS.
3. Reuse padrões de navegação e controles, mas alterne composições: capa, editorial, fluxo, cards narrativos, recursos, final. Use proporções equilibradas entre imagens, títulos e texto, com uma ideia dominante por capítulo.
4. Use cada animação para indicar relação ou transição de informação. Reduza o movimento se `prefers-reduced-motion` estiver ativo.
5. Preserve nomes, acentuação e grafia da marca conforme o repositório.

## Componentes que fazem sentido

- Navegação sequencial com índice de capítulos e barra de progresso editorial.
- Grafo simplificado clicável, destacando a responsabilidade atual.
- Campo «o que entrou / o que saiu», sem exibir JSON cru por padrão.
- Cenários demonstrativos pré-definidos, separados de chamadas reais ao backend.
- Linha temporal da concepção e evolução com marcos confirmados.
- Cards de tecnologia com ação «ver onde entra».
- Alternância entre «implementado», «simulado» e «planejado» acompanhada de explicação.

## Evitar

- Quiz, exercícios, professor, desafios, gabaritos, avaliações.
- Painéis vazios, gráficos decorativos, KPIs sem fonte, ícones aleatórios.
- Repetir grades de cartões em todos os capítulos.
- Mudar a interface do produto ou abrir PR sem autorização.
- Animações simulando porcentagem ou duração de tarefas reais.

## Acessibilidade e portabilidade

- HTML sem dependências externas é um bom ponto de partida.
- Navegação por teclado, foco visível, nomes acessíveis e controles de verdade.
- Layout legível em 390px, 768px, 1440px.
- `prefers-reduced-motion` suportado.
- Imagens têm alt. Assets ausentes usam fallback textual, não exibem imagem quebrada.
- Não invente esquema de cor caso o `design.md` já estabeleça um.
- Para apresentação em TV ou projetor, teste legibilidade à distância e escalas de títulos, texto explicativo, imagens e controles; não trate essa necessidade apenas como responsividade mobile.
- Prefira capitalização natural em títulos; reserve caixa alta para pequenos rótulos ou casos em que a identidade a exija. Preserve siglas e marcas.

Consulte `display-and-typography.md` para critérios, exemplos de tokens e validação.
