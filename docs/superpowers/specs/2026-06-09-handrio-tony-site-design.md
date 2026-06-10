# Design Spec — Site Handrio e Tony Cabeleireiros

**Data:** 2026-06-09
**Status:** Aprovado

---

## Visão Geral

Site cartão de visita online para o salão Handrio e Tony Cabeleireiros, localizado no Centro Histórico de Porto Alegre. O objetivo é apresentar o salão, seus serviços e informações de contato de forma simples, elegante e acolhedora — sem sistemas complexos como agendamento online.

---

## Dados do Negócio

| Campo | Valor |
|-------|-------|
| Nome | Handrio e Tony Cabeleireiros |
| Endereço | R. Espírito Santo, 96 — Centro Histórico, Porto Alegre - RS, 90010-370 |
| WhatsApp | (51) 99212-4041 |
| Telefone Fixo | (51) 3517-1945 |
| Horário | Seg–Sex 08h30 (sábado a confirmar com o dono) |
| Google | 5.014 avaliações |

---

## Arquitetura

**Tecnologia:** Single-page HTML estático (`index.html`) com CSS e JavaScript embutidos no mesmo arquivo. Sem dependências externas além de fontes do Google Fonts e o embed do Google Maps.

**Deploy:** GitHub Pages (repositório `handrio-tony`).

**Estrutura do arquivo:**
```
handrio-tony/
├── index.html          ← arquivo único com todo o site
├── images/             ← fotos do salão e da equipe
└── README.md
```

---

## Identidade Visual

| Elemento | Valor |
|----------|-------|
| Paleta principal | Bege claro `#FAF5EF`, bege médio `#EDE0D0`, caramelo `#D4A97A` |
| Paleta escura | Marrom escuro `#3D2B1F`, marrom médio `#5C3D2E` |
| Accent / destaque | Laranja caramelo `#C07C3A` |
| Texto principal | Marrom escuro `#3D2B1F` |
| Texto secundário | Marrom médio `#8B6347` |
| Fonte títulos | Georgia (serif) — transmite tradição |
| Fonte corpo | Arial / system-ui (sans-serif) — legibilidade |
| WhatsApp | Verde padrão `#25D366` |

---

## Seções (ordem na página)

### 1. Header / Navegação
- Fixo no topo, fundo `#5C3D2E`
- Logo/nome do salão à esquerda
- Links de navegação à direita: Serviços, Galeria, Equipe, Contato
- Em mobile: menu hamburguer

### 2. Hero
- Fundo com gradiente caramelo `#EDE0D0 → #D4A97A`
- Opcionalmente com foto do salão ou fachada em overlay
- Nome do salão em destaque (Georgia, tamanho grande)
- Subtítulo: "Tradição e qualidade há décadas no coração de Porto Alegre"
- Localização: "Porto Alegre · Centro Histórico"
- Dois botões de CTA: WhatsApp (verde) e Ligar (marrom)
- Badge de avaliação: ⭐⭐⭐⭐⭐ 5.014 avaliações no Google

### 3. Serviços
- Fundo bege claro `#FAF5EF`
- Título "Nossos Serviços" centralizado
- Grid 3 colunas (2 em mobile) com cards de serviços
- Serviços listados: Corte Masculino, Corte Feminino, Coloração, Escova, Barba, Hidratação, Relaxamento, Progressiva (o dono confirma a lista final)
- Cards com ícone emoji + nome do serviço, fundo `#EDE0D0`

### 4. Galeria de Fotos
- Fundo marrom escuro `#3D2B1F` para contraste
- Título "Galeria" em bege claro
- Grid 3 colunas de fotos do salão e trabalhos realizados
- Lightbox ao clicar: overlay escuro, seta prev/next, fechar com Esc ou clique fora
- Placeholder: fotos do Google Maps já disponíveis + fotos que o dono fornecer

### 5. Avaliações do Google
- Fundo bege claro `#FAF5EF`
- Destaque da nota geral: ⭐⭐⭐⭐⭐ com contagem de avaliações
- 3–4 cards com depoimentos reais do Google (texto, nome, estrelas)
- Link "Ver todas no Google" que abre o perfil do Google Maps
- Depoimentos iniciais: Rodrigo Denicol Franzoni e Ilza Zacouteguy (já disponíveis)

### 6. Nossa Equipe
- Fundo bege médio `#EDE0D0`
- Título "Nossa Equipe"
- Cards com foto circular (placeholder se não houver foto), nome e função
- Membros confirmados: Handrio (sócio), Tony (sócio), Joãozinho (cabeleireiro)
- O dono pode fornecer nomes e fotos adicionais

### 7. Contato & Localização (Footer)
- Fundo marrom escuro `#3D2B1F`
- Endereço completo com ícone 📍
- Número WhatsApp com link `https://wa.me/5551992124041`
- Número fixo com link `tel:+555135171945`
- Horário de funcionamento
- Embed do Google Maps (iframe) mostrando R. Espírito Santo, 96
- Botões WhatsApp e Ligar repetidos para conversão
- Copyright no rodapé

---

## Responsividade

- **Desktop (>768px):** Grid 3 colunas para serviços e galeria, navegação horizontal
- **Tablet (768px):** Grid 2 colunas para serviços, galeria 2 colunas
- **Mobile (<480px):** Tudo em coluna única, menu hamburguer, botões CTA em largura total

---

## Componentes JavaScript

- **Menu hamburguer mobile:** toggle de classe no `<nav>`
- **Lightbox da galeria:** reutiliza o padrão já implementado no site da Biopharma (overlay, prev/next, teclado Esc/setas)
- **Smooth scroll:** navegação suave ao clicar nos links do header
- **Botão WhatsApp flutuante:** ícone fixo no canto inferior direito em mobile

---

## Conteúdo a Confirmar com o Dono

- Lista completa de serviços oferecidos
- Horário de funcionamento do sábado
- Fotos do salão, fachada e equipe
- Nomes e funções de todos os profissionais
- Depoimentos adicionais do Google para usar no site

---

## Fora do Escopo

- Sistema de agendamento online
- Área administrativa / CMS
- Blog
- Loja / e-commerce
- Múltiplas páginas
