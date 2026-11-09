# Portfólio Profissional — Pedro Paulo Leão

**Nome do Aluno:** Pedro Paulo Leão Fernandes Dos Santos  
**Componente Curricular:** Desenvolvimento de Sistemas I — Agenda 15 (ETEC)  

---

## Descrição do Portfólio
Este projeto consiste em um portfólio pessoal e profissional desenvolvido para apresentar minha trajetória acadêmica, habilidades técnicas e projetos práticos construídos ao longo do curso Técnico em Desenvolvimento de Sistemas. A interface foi estruturada para ser responsiva, organizada e acessível em computadores, tablets e smartphones.

---

## Tecnologias Utilizadas
* **HTML5:** Estruturação semântica das seções da página (`<nav>`, `<section>`, `<footer>`).
* **CSS3:** Personalização visual, rolagem suave (`scroll-behavior: smooth`), controle de proporção de imagens (`object-fit: cover`) e animações/transições interativas.
* **Bootstrap 5.3.3:** Sistema de grid responsivo (`container`, `row`, `col`), barra de navegação fixa (`navbar sticky-top`), componente de destaque (`carousel`), cartões (`card`) e botões estilizados.
* **Devicon & Bootstrap Icons:** Ícones vetoriais para identificação visual das linguagens e ferramentas.
* **Git & GitHub Pages:** Controle de versão e hospedagem gratuita do site estático na web.

---

## Link do Site Publicado
* **Repositório no GitHub:** `https://github.com/pedro-leao-dev/portfolio`
* **Site Publicado (GitHub Pages):** `https://pedro-leao-dev.github.io/portfolio/`

*(Observação: substitua `portfolio` pelo nome exato do repositório criado na sua conta, caso utilize outro nome).*

---

## Explicação do Funcionamento do Projeto
O site funciona como uma *Single Page Application* (página única dividida em seções ancoradas):
1. **Menu de Navegação (`Navbar`):** Permanece fixo no topo da tela (`sticky-top`) e possui links internos (`#perfil`, `#formacao`, `#projetos`, `#contato`) que levam diretamente a cada seção, adaptando-se automaticamente para um menu colapsável em telas menores.
2. **Carousel de Destaque:** Exibe três slides introdutórios com controle manual e transição automática em fade.
3. **Seção de Perfil:** Apresenta foto circular, resumo profissional, cards de informações rápidas e grade de tecnologias dominadas.
4. **Seção de Formação e Experiência:** Organiza a trajetória acadêmica e profissional em três colunas responsivas.
5. **Seção de Projetos:** Exibe três aplicações reais desenvolvidas em Python e Web, com links diretos para os repositórios no GitHub.
6. **Seção de Contato e Rodapé:** Centraliza os canais de comunicação direta (e-mail, GitHub e LinkedIn).

---

## Descrição dos Recursos Novos Adicionados
Além da estrutura base desenvolvida em aula, foram incorporados dois recursos inéditos ao portfólio:
1. **Nova Seção de Formação e Experiência (`#formacao`):** Inclusão de uma seção dedicada à trajetória acadêmica (ETEC e Universidade Mackenzie) e experiência analítica, integrada também ao menu de navegação superior.
2. **Animações e Microinterações Visuais (`hover` e transições):** Efeitos dinâmicos de elevação nos cards, zoom suave nas imagens dos projetos e do carousel, além de rolagem suave entre as âncoras da página.

---

## Explicação de Como os Recursos Foram Implementados
* **Seção de Formação e Experiência:** Foi implementada utilizando uma nova tag `<section id="formacao">` estruturada com o sistema de grid do Bootstrap (`row g-4` e três colunas `col-md-4`), contendo cards com bordas arredondadas (`rounded-4`) e etiquetas (`badge`) para destacar os períodos de formação. O link correspondente foi adicionado à lista `<ul class="navbar-nav">` no topo da página.
* **Animações e Transições:** Foram implementadas por meio de regras CSS personalizadas dentro da tag `<style>` no `<head>`:
  * A classe `.card-hover` utiliza `transition: transform 0.3s ease, box-shadow 0.3s ease;` combinada com o seletor `:hover { transform: translateY(-8px); }`, criando um efeito de elevação quando o cursor passa sobre os cartões.
  * As imagens dentro de `.project-img-wrapper` possuem `overflow: hidden` e `transition: transform 0.4s ease`, aplicando um leve zoom (`scale(1.06)`) durante o `hover` sem ultrapassar as bordas arredondadas do card.
  * No carousel, `.carousel-item.active img` aplica uma transição suave de escala (`transform: scale(1.05)` em `6s`), dando movimento contínuo aos banners.
