Landing Page do Centro Académico Clínico dos Açores (CACA)

Grupo 11
Alexandre Pereira
Joana Rego
Tomás Moreira 

---Identidade Visual---

Paleta de Cores:
Azul: #061D60 | Uso: Header, fundo do body, texto da hero section | Justificação: Cor da bandeira dos Açores, estabelece identidade regional e ligação emocional
Cinza claro: #e9e9e9 | Uso: Fundo das secções de conteúdo | Justificação: Contraste com o header azul e cria hierarquia visual
Cinza médio: #dcdcdc | Uso: Fundo dos cards |Justificação: Diferencia os cards do fundo da secção
Branco: #FFFFFF | Uso: Texto no header, hero section, botões | Justificação: Garante legibilidade sobre fundos escuros
Verde: #2ECC71 | Uso: Botões (previsto) | Justificação: Associado à saúde, natureza e renovação - contexto clínico

Tipografia:
Títulos (h1, h2) | sans-serif | 42px | Negrito | Hierarquia clara e impacto visual 
Hero text | sans-serif | 48px (32px mobile) | Normal | Destaque máximo com fundo semi-transparente para legibilidade 
Corpo de texto | sans-serif | 18px | Normal | Legibilidade em ecrã, conforto de leitura 
Menu | sans-serif | 16px | Normal | Navegação discreta mas funcional 
A escolha de fonte sans-serif garante máxima compatibilidade e legibilidade em todos os dispositivos, cumprindo os requisitos de acessibilidade.

---Estilo Geral---
-Design limpo e institucional - adequado ao contexto académico-clínico
-Cards com cantos arredondados (15px) - modernidade sem perder formalidade
-Hero section com imagem de fundo - ligação visual à região dos Açores
-Espaçamento (padding de 50px nas secções) - leitura confortável
-Menu com scroll - experiência de navegação fluida

---
Evolução do Projeto: Wireframe → Mockup → Implementação:

---Fase 1: Wireframe---

O wireframe foi desenvolvido para o esquema da landing page, focando na estrutura e organização do conteúdo:
-Cabeçalho: com logo, nome e menu de navegação
-Hero section: com imagem de fundo e texto principal
-Secção Missão: com 3 cards (três pilares)
-Secção Investigação: com 3 cards (três áreas)
-Secção Parceiros: com área para logótipos
-Secção Oportunidades: com lista de links
-Secção Contactos: dividida em info e formulário
-Rodapé: Info de direitos de autor, referência à universidade, curso e ano letivo
Objetivo: Definir a hierarquia da informação.

---Fase 2: Mockup---

O mockup (desenvolvido em Figma) acrescentou ao wireframe:
- Aplicação da paleta de cores
- Definição tipográfica - tamanhos e pesos para cada elemento
- Uso de imagens - logótipo fictício, paisagem dos Açores, logótipos dos parceiros
- Detalhamento dos cards - conteúdo textual completo
- Alinhamentos e espaçamentos- refinamento visual

Alterações em relação ao wireframe:
- Ajuste da largura das secções para 80% com margem automática (melhor enquadramento visual)
- Definição de border-radius de 15px para todos os cards
- Hero text com fundo semi-transparente para garantir legibilidade

---Fase 3: Implementação (HTML/CSS)---
A implementação final traduziu o mockup para código funcional:
HTML5:
- Tags: `header`, `nav`, `section`
- Estrutura de headings: h1 (Missão), h2 (restantes secções), h3 (cards)
- Listas nos cards e links de oportunidades
- Formulário com campos `required` e placeholders descritivos
- Atributos `alt` em todas as imagens

CSS3:
- Flexbox para organização dos cards e secções
- Media query para responsividade (max-width: 768px)
- Scroll behavior: smooth para navegação por âncoras
- Posicionamento absoluto para hero text sobre imagem


---Melhoramentos incorporados:---
- Aumento do contraste do hero text com fundo rgba(0,0,0,0.4)
- Ajuste do scale do logo (1.3) para proporção adequada
- Correção de alinhamentos no formulário

---

---Aspetos Evitados---

- Navegação complexa com múltiplas páginas
- Contactos pouco destacados 
- Excesso de texto sem suporte visual

---

---Acessibilidade---
-Princípios Aplicados
Atributos alt: Todas as imagens têm descrição: `alt="CACA"`, `alt="Paisagem dos Açores"`, `alt="Universidade dos Açores"` 
Contraste de cores: Texto branco em fundo azul | texto preto em fundo cinza claro 
Hierarquia de cabeçalhos: h1 (Missão) → h2 (restantes secções) → h3 (títulos dos cards) - estrutura lógica 
Labels em formulários: Placeholders descritivos |
Scroll suave: scroll-behavior: smooth - melhora experiência sem comprometer funcionalidade 
Textos descritivos: Links com texto significativo ("+ Estágios e projetos..." em vez de "clique aqui") 

---Responsividade---
Abordagem Mobile-First: O desenvolvimento partiu do desktop com adaptação para mobile através de media query:

```css
@media (max-width: 768px) {
  .hero-texto {
    font-size: 32px;  /* Redução de 48px para melhor legibilidade em ecrãs pequenos */
  }

  .logo-header {
    height: 50px;  /* Redução de 60px para proporção adequada */
  }
  
  /* Comportamento adicional garantido pelo flex-wrap */
  .cards, .cards2, .contactos-tt {
    flex-wrap: wrap;  /* Cards empilham verticalmente */
  }
}
