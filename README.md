Markdown

# Projeto Bootstrap — Paysandu Sport Club

Site institucional e painel administrativo desenvolvidos para o **Paysandu Sport Club**, utilizando o framework **Bootstrap 5.3** e **HTML5 Semântico**, seguindo rigorosamente a restrição de **zero tags `<div>`**.

---

## 🧭 Explicação de Cada Seção (Páginas / Módulos)

1. **Header & Navbar (Etapa 1):** 
   - Cabeçalho responsivo contendo a logo oficial do clube e menu de navegação. 
   - No mobile, o menu exibe-se em formato vertical centralizado; no desktop, transforma-se em um menu horizontal fluído através de media queries customizadas.
2. **Hero Section (Etapa 2):** 
   - Seção de destaque inicial com headline, subheadline, imagem ilustrativa do clube e botões de chamada para ação (*CTA*). A ordem dos elementos inverte-se por breakpoint (`order-*`), priorizando a imagem no mobile e o texto no desktop.
3. **Seção de Conteúdo / Cards (Etapa 3):** 
   - Grade contendo 12 cards informativos sobre notícias, categorias de base, ingressos e loja oficial (`col-12 col-md-6 col-lg-3`), adaptando-se de 1 coluna (mobile), 2 colunas (tablet) a 4 colunas (desktop).
4. **Tabela Profissional (Etapa 4):** 
   - Tabela de classificação detalhada com cabeçalho escuro, linhas alternadas (*striped*), efeito *hover* e ícones via **Bootstrap Icons**. Totalmente responsiva sem quebrar o layout em telas menores (`table-responsive`).
5. **Formulários (Etapa 5):** 
   - Dois formulários completos (Cadastro de Sócio Campeão e Fale Conosco) estruturados em grid, contendo inputs variados, grupos de entrada (*input-group*), rádios, checkboxes, selects, textarea e estados visuais de validação nativa (`is-valid`, `is-invalid`).
6. **Modais sem JavaScript (Etapa 6):** 
   - Simulação de janela modal para compra de ingressos utilizando a técnica do ***Checkbox Hack*** (HTML + CSS puro), com overlay fixo, backdrop clicável e controle de empilhamento (`z-index`).
7. **Responsividade Extrema (Etapa 7):** 
   - Aplicação transversal de utilitários de visibilidade e comportamento responsivo em todo o conteúdo do projeto, garantindo adaptações perfeitas em múltiplos tamanhos de tela.
8. **Sistema de Design (Etapa 8):** 
   - Padronização visual coerente utilizando diversas cores do tema Bootstrap (`primary`, `success`, `warning`, `danger`, `info`, `dark`, `secondary`), variações de botões e múltiplos estilos de badges.
9. **Dashboard Administrativo (Etapa 9):** 
   - Painel de gestão sem JavaScript, utilizando o sistema de **Grid + Flex** do Bootstrap para estruturar uma sidebar fixa em desktop e oculta em mobile, além de cartões de métricas (*metrics cards*), alertas do sistema e tabela de transações.
10. **Rodapé Institucional (Footer):** 
    - Rodapé personalizado com informações sobre o projeto, links úteis de navegação e redes sociais oficiais, mantendo a identidade visual do clube.

---

## 🛠️ Quais Classes Bootstrap Foram Usadas

- **Layout e Grid:** `container`, `container-xl`, `row`, `col-12`, `col-md-6`, `col-lg-3`, `col-lg-4`, `col-lg-6`, `col-lg-9`.
- **Flexbox e Alinhamento:** `d-flex`, `flex-column`, `flex-lg-row`, `justify-content-between`, `align-items-center`, `align-self-start`, `flex-grow-1`.
- **Espaçamento e Bordas:** `py-5`, `mb-3`, `mb-4`, `g-3`, `g-4`, `rounded-3`, `rounded-4`, `shadow-sm`, `shadow-lg`, `border-0`.
- **Visibilidade:** `d-none`, `d-block`, `d-md-block`, `d-lg-block`.
- **Componentes:** `navbar`, `navbar-expand-lg`, `collapse`, `card`, `badge`, `btn`, `table`, `table-striped`, `table-hover`, `alert`, `list-group`, `input-group`, `form-control`, `form-select`.

---

## 🎨 Onde Foi Necessário CSS Próprio e Por Quê

1. **Gradient Background (`.background` e `.hero-section`):** Utilizado para aplicar degradês personalizados nas cores oficiais do Paysandu e sobreposições escuras na imagem de fundo da Hero Section, garantindo legibilidade perfeita do texto.
2. **Checkbox Hack para o Modal (`.modal-checkbox-hack`, `.modal-custom-overlay`):** Necessário para esconder o elemento nativo de caixa de seleção e manipular a propriedade `display` do overlay do modal puramente através do seletor de estado CSS (`:checked ~ .modal-custom-overlay`), cumprindo a regra de proibição absoluta de JavaScript.
3. **Controle de Logo e Responsividade Específica (`.logo-paysandu`):** Ajustes de altura fixa, largura automática, margens responsivas e regra de ocultação (`display: none`) em telas menores que `500px` para otimizar o espaço do cabeçalho.
4. **Transições e Efeitos no Rodapé (`footer a`):** Aplicação de transições suaves de cor no *hover* dos links do rodapé.

---

## ⚠️ Principais Dificuldades

- **Restrição Absoluta de Tags (`<div>` Proibidas):** O maior desafio estrutural foi substituir todas as tradicionais caixas `<div>` por tags semânticas corretas do HTML5 (`<section>`, `<article>`, `<header>`, `<aside>`, `<figure>`, `<figcaption>`), mantendo a exata compatibilidade com o sistema de grid e componentes do Bootstrap.
- **Modais sem JavaScript:** Implementar o comportamento de abertura e fechamento de modais com cliques de fundo (*backdrop*) e botões de fechar sem recorrer a scripts de JS exigiu domínio preciso da hierarquia de elementos irmãos e seletores avançados de CSS (*Checkbox Hack*).
- **Manutenção do Layout Responsivo:** Garantir que a sidebar do dashboard, a barra de navegação e as seções de conteúdo funcionassem de maneira fluida em telas de celulares, tablets e desktops sem quebrar o fluxo semântico.