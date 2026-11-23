---
name: project-showcase
description: Cria showcases interativos de projetos de software a partir do repositório e da documentação, apresentando história, propósito, funcionalidades, arquitetura em linguagem acessível, decisões técnicas, inovação e estágio real de implementação. Use quando alguém pedir apresentação narrativa, site showcase, portfólio interativo ou demonstração visual de um projeto, sem aulas, quizzes ou exercícios.
---

# Project Showcase

Transforme projetos reais em uma **experiência editorial interativa**, não em apostila, slide de aula, dashboard de observabilidade nem documentação técnica disfarçada. O resultado deve contar uma história fundamentada, permitir explorar o funcionamento do sistema e mostrar como as tecnologias resolveram problemas concretos.

## Ativação e escopo

Acione a skill para: apresentar um sistema; contar origem e objetivos; explicar o funcionamento de agentes/serviços e jornadas de usuários; demonstrar funcionalidades e inovações; produzir site HTML interativo de portfólio. Não a acione para explicar código linha a linha, desenhar apenas arquitetura técnica, produzir tutorial, criar slides convencionais ou alterar o produto original.

**Princípio de reutilização:** nenhuma identidade de marca, nome, cor, logotipo, tecnologia ou história específica deve estar codificada nesta skill. Os exemplos ficam em `examples/`. Cada projeto fornece ou recebe uma configuração específica de conteúdo e identidade visual.

## Entradas e prioridades

1. Leia, quando existentes, `README.md`, documentos de escopo, `design.md`, decisões, changelog, testes, esquemas de dados e arquivos de implementação relevantes. Se o usuário apontar um repositório ou arquivos, priorize a fonte exata.
2. Busque primeiro os arquivos oficiais da identidade visual e confirme a grafia da marca. Preserve os ativos originais; não reconstrua marcas ou logotipos com aproximações quando eles existirem. Se o logo não estiver acessível no ambiente de geração, mantenha referência substituível e declare a limitação.
3. Use o código e os testes para confirmar o que funciona. Documentos de planos mostram *intenções*, não provas de implementação. Registre a origem das alegações importantes.
4. Observe explicitamente a data/revisão do material consultado. Em caso de divergência, a fonte atual de implementação determina o status funcional; decisões de marca vêm do guia de identidade. Caso a divergência continue sem resolução, marque como `a confirmar`.
5. Não solicite segredos, tokens nem `.env`; não incorpore dados pessoais, chaves ou URL privada na entrega.

## Pipeline obrigatório

### 1. Levantamento factual

Crie uma matriz interna `afirmacao | evidencia | status | fonte`. Classifique cada recurso como:

- **Implementado:** evidenciado por código/testes ou documentação atual claramente descritiva.
- **Simulado:** a interface ou o backend usa mocks/fakes/stubs/provedores simulados.
- **Em desenvolvimento:** há trabalho iniciado, mas não concluído.
- **Planejado:** aparece apenas na especificação ou roadmap.
- **Não verificado:** falta evidência suficiente.

Nunca converta uma simulação em execução real por linguagem, animação, barra de progresso, imagem ou estado visual. Um exemplo hipotético deve ser identificado como tal.

### 2. Narrativa do projeto

Responda às perguntas, nesta ordem lógica (não precisa haver um slide para cada uma):

- **De onde veio a ideia?** Contexto e motivação documentados.
- **Que experiência pretendíamos construir?** Proposta e diferencial.
- **Como funciona na prática?** Um pedido concreto atravessando as funções reais do sistema.
- **Por que foi desenhado desse modo?** Responsabilidades, fluxo de informação, decisões técnicas.
- **O que foi aplicado dos estudos?** Tecnologias conectadas ao problema que resolvem, evitando glossário avulso.
- **O que já funciona e o que vem depois?** Entregas e limites sem exagerar maturidade.
- **Quem construiu?** Créditos e aprendizados, somente se documentados.

Não invente história, números de usuários, economia, resultados, validação de mercado ou impacto.

### 3. Experiência visual

Aplique **o design do projeto**, não o do exemplo desta skill. Leia `references/visual-and-interaction.md` antes de gerar a interface.

Prefira um site HTML responsivo de navegação por capítulos: abertura forte; narrativa editorial; cards apenas onde ajudam; fluxo interativo com etapas; tecnologias explicadas na sua aplicação; estado atual e evolução. As telas não devem parecer todas iguais. Interatividade serve à compreensão, não a tarefas de avaliação.

A identidade vem de `showcase.config.json` (modelo em `references/config.schema.md`): nome, cores, tipografia, ativos, tom, seções, fontes e permissões. Respeite o guia visual do produto acima de tendências genéricas.

### 4. Interatividade honesta

Uma simulação didática pode avançar/voltar pelos nós, destacar o passo atual, mostrar o dado de entrada e o que mudou no estado, comparar aprovação/reprovação e abrir detalhes de uma decisão. **Não conecte o mock a um backend imaginário nem finja logs reais.** Mostre rótulo visível `Simulação ilustrativa`.

Não inclua quiz, exercício, prova, tarefa de casa, desafio, gabarito, narrador/instrutor ou tela de terminal como protagonista, salvo pedido explícito do usuário. Evite porcentagens fictícias, métricas imaginadas e animações que sugiram processamento real.

### 5. Entregáveis

Gere, conforme o pedido:

- `showcase.html`: HTML/CSS/JS autocontido ou uma aplicação equivalente quando justificada;
- `showcase.config.json`: dados e identidade por projeto, separada da skill;
- `SOURCES.md`: fontes consultadas, data da leitura e fatos que exigem atualização;
- `README.md`: como abrir, personalizar e diferenciar simulação de execução real.

Se produzir código, descreva brevemente cada bloco adicionado e como os dados passam por ele. Não edite o produto original sem solicitação explícita. Não faça commit, push ou PR por conta própria.

### 6. Revisão antes da entrega

Leia `references/quality-gates.md` e valide: fidelidade narrativa; status verdadeiros; marca correta; nenhuma aula/quiz; demonstração controlável; contraste, teclado e movimento reduzido; experiência em 390px, 768px e 1440px; sem dependência externa desnecessária; sem segredos. Se possível, capture e examine uma renderização no navegador.

## Exemplos e referências

- Exemplo de projeto: `examples/coxinh-ia/showcase.config.json` e `examples/coxinh-ia/storyboard.md`.
- Referências de roteiro e interações: `references/narrative.md` e `references/visual-and-interaction.md`.
- As regras do exemplo **não são universais**; nenhum outro projeto deve herdar a marca Coxinh.IA.
