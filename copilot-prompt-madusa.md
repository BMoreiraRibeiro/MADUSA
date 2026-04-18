# PROMPT — GitHub Copilot / VS Code
# Página Web Institucional: Grupo Madusa (MadusaClima)
# Podes usar este prompt diretamente no Copilot Chat (@workspace) ou no Copilot Edits

---

## CONTEXTO DA EMPRESA

Empresa: **Grupo Madusa / MadusaClima**
Setor: AVAC — Climatização, Aquecimento, Ventilação e Ar Condicionado
Fundação: 2016
Sede: Avenida Manuel Pereira Soares 603 r/c-D, 4630-296 Marco de Canaveses (Porto)
Telefone: 255 535 275
E-mail: madusaclima@hotmail.com
LinkedIn: https://www.linkedin.com/company/madusaclima/
Facebook: https://www.facebook.com/profile.php?id=61576842067718
NIF: 513 887 172

**Serviços principais:**
- Instalação de climatização (split, multi-split, VRF)
- Manutenção preventiva e corretiva de sistemas AVAC
- Reparação e assistência técnica
- Aquecimento central (caldeiras, bombas de calor, radiadores)
- Ventilação industrial e comercial
- Comércio de equipamentos de climatização, aquecimento e ventilação
- Projetos AVAC para unidades industriais

**Setores servidos:** Habitação, Condomínios, Comércio, Escritórios, Indústria, Hotelaria, Saúde, Restauração

---

## IDENTIDADE VISUAL (extraída do logótipo)

O logótipo tem uma chama/onda multicolor (vermelho, laranja, amarelo, magenta, verde, azul)
com a palavra "GRUPO" em azul escuro pequeno e "MADUSA" em vermelho bold grande.

**Paleta de cores a usar:**
```css
--red:       #C8102E;   /* vermelho principal — acento primário */
--red-dark:  #95001F;   /* hover do vermelho */
--orange:    #F4831F;   /* laranja — acento secundário / destaques */
--navy:      #0F1A2E;   /* fundo escuro principal */
--steel:     #1A2540;   /* fundo de cards/secções */
--steel-mid: #2B3A55;   /* hover de cards */
--slate:     #3F5070;   /* bordas / separadores */
--muted:     #8EA0B8;   /* texto secundário */
--light:     #F4F1EC;   /* texto principal em fundo escuro */
```

**Tipografia:**
- Títulos/headings: `Barlow Condensed` (Google Fonts) — pesos 700, 800, 900
- Corpo: `Barlow` (Google Fonts) — pesos 300, 400, 500
- Evitar: Inter, Roboto, Arial, System-UI

---

## PEDIDO AO COPILOT

Cria uma landing page institucional completa em **HTML + CSS + JavaScript vanilla**
(ficheiro único: `index.html`) para o **Grupo Madusa / MadusaClima**.

### Estrutura de Secções (nesta ordem):

1. **NAV** — Barra de navegação fixa no topo, com:
   - Logótipo (SVG inline com motivo de chama + texto "GRUPO / MADUSA")
   - Links: Sobre Nós | Serviços | Vantagens | Contacto
   - CTA button vermelho: "Pedir Orçamento"
   - Background: `rgba(15,26,46,0.95)` com `backdrop-filter: blur(12px)`
   - Borda inferior subtil

2. **HERO** — Secção full-height (100vh), com:
   - Fundo escuro com grid de linhas finas (background-image com linear-gradient)
   - Sobreposição de chama SVG decorativa à direita (semitransparente)
   - Título enorme (`Barlow Condensed 900`): ex. "CONTROLO TÉRMICO AVANÇADO" com a palavra-chave em vermelho
   - Subtítulo explicativo curto
   - 2 botões: "Pedir Orçamento" (vermelho) + "Ver Serviços" (outline)
   - Stats abaixo: "9+ Anos de experiência | 100% Técnicos certificados | 360° Serviço completo"
   - Badge animado no canto inferior: "● Em atividade desde 2016"

3. **STRIP (ticker)** — Faixa vermelha com marquee animado listando serviços

4. **SOBRE NÓS** — Grid 2 colunas:
   - Esquerda: card escuro com checklist de serviços (com tick em SVG vermelho)
   - Direita: texto institucional, localização, parágrafo sobre a empresa
   - Efeito scroll-reveal (IntersectionObserver)

5. **SERVIÇOS** — Grid 3x2 de cards:
   - Emoji/ícone no topo de cada card
   - Título em `Barlow Condensed 800` uppercase
   - Descrição curta
   - Barra animada na base do card ao hover (gradiente vermelho→laranja)
   - Serviços: Ar Condicionado | Aquecimento Central | Ventilação Industrial | Manutenção & Assistência | Projetos Industriais | Venda de Equipamentos

6. **SETORES** — Faixa de pills/tags com os setores servidos (com hover vermelho)

7. **VANTAGENS** — Grid 2 colunas:
   - Esquerda: lista de 4 vantagens numeradas (01, 02, 03, 04) com título e descrição
   - Direita: grid 2x2 de mini-cards com ícone, título e texto curto

8. **CONTACTO** — Grid 2 colunas:
   - Esquerda: título + descrição + info de contacto (morada, telefone, email, horário)
   - Direita: formulário com campos: Nome, Telemóvel, Email, Tipo de Serviço (select), Mensagem
   - Botão de envio vermelho com feedback visual (cor muda para verde ao clicar)

9. **FOOTER** — Uma linha: logótipo | copyright + NIF | links redes sociais (LinkedIn, Facebook)

---

### Requisitos Técnicos:

- **Ficheiro único** `index.html` — sem dependências externas exceto Google Fonts
- **Responsivo** — mobile-first com breakpoints em 900px e 560px
- **Scroll-reveal** — com `IntersectionObserver` nativo, sem bibliotecas
- **Marquee/ticker** — animado com `@keyframes` CSS puro
- **Nav fixa** — com `position: fixed` e `backdrop-filter`
- **Hover interactions** — na nav, cards de serviços, pills de setores, botões
- **Sem frameworks** — HTML/CSS/JS puro (sem React, Vue, Tailwind, Bootstrap)
- **Comentários** em português no CSS e JS
- **Acessibilidade básica** — atributos `alt`, `aria-label` onde relevante
- **SEO básico** — `<title>`, `<meta description>`, `<meta viewport>`
- **Idioma**: `lang="pt"` — toda a página em português europeu

### Tom e Estética:

- Industrial mas profissional — não excessivamente "tech startup"
- Escuro, sólido, confiante — transmite credibilidade técnica e rigor fabril
- Acentos de energia (vermelho/laranja) que remetem para calor e chama (metáfora AVAC)
- Tipografia condensed e bold para títulos — impacto visual imediato
- Cards com bordas subtis, sem sombras excessivas — clean mas robusto

---

## FICHEIRO DE REFERÊNCIA

O ficheiro `grupo-madusa-referencia.html` na mesma pasta contém uma implementação
de referência completa. Usa-o como base ou para comparar abordagens.
Podes melhorar: animações, responsividade, acessibilidade ou adicionar secções.

---

## SUGESTÕES DE MELHORIA PARA O COPILOT (além da referência):

- Adicionar mapa Google Maps embed na secção de contacto
- Galeria de projetos / antes-depois com slider
- Secção de testemunhos/reviews de clientes
- Contador animado nos stats (0 → número final com JS)
- Menu hamburger para mobile
- Efeito parallax subtil no hero
- FAQ accordion com perguntas frequentes sobre climatização
- Badge de WhatsApp flutuante para contacto rápido

---

*Prompt gerado a partir de análise do logótipo, LinkedIn, Facebook e registos públicos da empresa.*
*Não inventar informação não verificada — usar apenas os dados acima.*
