# Portfólio – Bruno Cezar da Silva

**Aluno:** Bruno Cezar da Silva
**Contato:** brunocezargdae@gmail.com
**GitHub:** https://github.com/brunocezargdae-jpg
**Site publicado (GitHub Pages):** https://brunocezargdae-jpg.github.io/portfolio-bruno-cezar/

## Descrição do portfólio
Portfólio pessoal criado a partir do projeto "Meus sites favoritos" feito em aula. Ele apresenta quem eu sou, as tecnologias que estou aprendendo, os projetos que desenvolvi no curso e formas de entrar em contato. O projeto evoluiu de uma página simples em CSS Grid para um site completo, responsivo e com Bootstrap.

## Tecnologias utilizadas
- HTML5
- CSS3 (animações, transições, `@keyframes`)
- Bootstrap 5.3 (grid, navbar, cards, carousel, formulário, barras de progresso)
- Bootstrap Icons
- JavaScript (IntersectionObserver, localStorage, validação de formulário)
- Git e GitHub Pages

## Estrutura do projeto
```
portfolio-bruno-cezar/
├── index.html                      # página principal
├── css/style.css                   # estilos próprios
├── js/script.js                    # scripts (animações, tema, formulário)
├── assets/                         # avatar e imagens do carousel
├── projetos/
│   ├── meus-sites-favoritos/       # projeto feito em aula
│   └── portal-entretenimento/      # projeto de Flexbox e CSS Reset
└── README.md
```

## Como o projeto funciona
- **Menu de navegação:** navbar fixa do Bootstrap com links para as seções (`#perfil`, `#habilidades`, `#projetos`, `#contato`). A rolagem é suave e o *scrollspy* destaca a seção atual. No celular o menu vira um botão "hambúrguer".
- **Perfil:** apresentação com avatar, nome, descrição e botões de ação.
- **Habilidades:** barras de progresso com as tecnologias estudadas.
- **Projetos:** três cards (dois abrem as páginas dos projetos feitos no curso, dentro da pasta `projetos/`) e uma galeria em carousel com os sites favoritos.
- **Contato:** e-mail, link do GitHub e um formulário validado com Bootstrap que abre o programa de e-mail já preenchido (`mailto`).
- **Responsividade:** o layout usa o grid do Bootstrap e se adapta a celular, tablet e computador.

## Recursos novos adicionados
Além do que foi feito em aula, incluí:

1. **Seção de Habilidades com barras animadas** (recurso principal)
2. **Animações de entrada ao rolar a página** e efeitos de hover nos cards
3. **Carousel com efeito de fade e zoom suave**
4. **Modo claro/escuro**

### Como foram implementados
**1. Habilidades com barras animadas.** Cada barra é um `progress-bar` do Bootstrap com o nível no atributo `data-nivel` (ex.: `data-nivel="85"`). No CSS a barra começa com `width: 0` e tem `transition: width 1.4s`. No JavaScript, um `IntersectionObserver` detecta quando a barra aparece na tela, define `style.width` com o valor do `data-nivel` (a transição CSS anima o preenchimento) e um contador com `requestAnimationFrame` faz o número subir de 0% até o nível.

**2. Animação de entrada e hover.** Os elementos com a classe `.reveal` começam invisíveis (`opacity: 0` e deslocados para baixo). Quando entram na tela, o `IntersectionObserver` adiciona a classe `.visivel`, e a `transition` faz o elemento aparecer subindo. Os cards de projeto usam `:hover` com `transform: translateY(-8px)` e sombra colorida.

**3. Carousel com fade e zoom.** Usei o carousel do Bootstrap com a classe `carousel-fade` e, no CSS, a animação `@keyframes zoom` aplicada à imagem do slide ativo (`.carousel-item.active img`), que aumenta levemente a imagem enquanto o slide é exibido.

**4. Modo escuro.** O Bootstrap 5.3 troca o tema pelo atributo `data-bs-theme` no `<html>`. O botão da navbar alterna entre `light` e `dark`, troca o ícone (lua/sol) e salva a escolha no `localStorage`, para que o tema seja lembrado na próxima visita.

Também há cuidado com acessibilidade: se o visitante preferir menos movimento (`prefers-reduced-motion`), as animações são desativadas, e se o JavaScript estiver desligado o conteúdo continua visível.

## Como executar localmente
1. Baixe ou clone o repositório.
2. Abra o arquivo `index.html` no navegador (é preciso internet para carregar o Bootstrap pelo CDN).

## Como publicar no GitHub Pages
1. Crie um repositório chamado `portfolio-bruno-cezar` em https://github.com/brunocezargdae-jpg
2. Envie os arquivos (pelo site, com **Add file → Upload files**, ou pelo Git):
   ```bash
   git init
   git add .
   git commit -m "Portfólio com Bootstrap"
   git branch -M main
   git remote add origin https://github.com/brunocezargdae-jpg/portfolio-bruno-cezar.git
   git push -u origin main
   ```
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**, selecione a branch `main` e a pasta `/ (root)` e clique em **Save**.
5. Aguarde cerca de 1 a 2 minutos. O site ficará em:
   https://brunocezargdae-jpg.github.io/portfolio-bruno-cezar/

## Autor
Bruno Cezar da Silva – https://github.com/brunocezargdae-jpg
