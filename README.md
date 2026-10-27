# 🏷️ Guia Rápido: Tags Semânticas em HTML5

Este guia apresenta os conceitos fundamentais da **semântica no HTML5**, demonstrando a diferença entre estruturar um site de forma genérica e utilizar boas práticas de desenvolvimento web.

---

## ❓ O que é Semântica no HTML?

**Semântica** significa dar sentido e significado ao código.

Antes do HTML5, os desenvolvedores utilizavam a tag `<div>` para construir a página inteira. Embora o código funcionasse visualmente, navegadores, leitores de tela e motores de busca (como o Google) não conseguiam diferenciar um menu de navegação, um cabeçalho ou um rodapé.

> 💡 **Analogia:** Usar apenas `<div>` é como guardar todas as roupas da sua casa em caixas de papelão idênticas e sem etiqueta. As **Tags Semânticas** funcionam como caixas organizadoras com etiquetas bem claras: *"Meias"*, *"Camisetas"*, *"Casacos"*.

---

## 🏗️ As Principais Tags Semânticas (Estrutura do Site)

```text
┌────────────────────────────────────────────────────────┐
│                        <header>                        │
│             (Cabeçalho: Título e Logo)                 │
├────────────────────────────────────────────────────────┤
│                         <main>                         │
│                  (Conteúdo Principal)                  │
│                                                        │
│  ┌──────────────────────┐    ┌──────────────────────┐  │
│  │      <section>       │    │      <article>       │  │
│  │ (Seção de Conteúdo)  │    │  (Post / Card / Item)│  │
│  └──────────────────────┘    └──────────────────────┘  │
│                                                        │
├────────────────────────────────────────────────────────┤
│                        <footer>                        │
│                (Rodapé: Direitos e Contatos)           │
└────────────────────────────────────────────────────────┘
```

---

## 📌 Para que serve cada tag?

| Tag | Para que serve? | Exemplo de uso |
| :--- | :--- | :--- |
| `<header>` | Cabeçalho principal da página ou de um bloco. | Título do site, logo, banner principal. |
| `<main>` | O conteúdo principal da página *(deve existir apenas 1 por página!)*. | O bloco central onde fica a aplicação/dashboard. |
| `<section>` | Agrupa conteúdos que pertencem ao mesmo assunto. | Seção "Sobre Nós", "Módulos da Nave", "Formulário". |
| `<article>` | Um bloco autônomo que faz sentido sozinho. | Post de blog, card de produto, painel de estatísticas. |
| `<footer>` | Rodapé da página ou de um cartão. | Direitos autorais, links de contato, criadores do projeto. |
| `<nav>` | Bloco destinado a links de navegação. | Menus principais e barras de navegação do site. |
| `<label>` | Rótulo/texto explicativo para um campo de entrada. | Texto associado a um campo `<input>`. |

---

## ❌ Como NÃO fazer vs. ✅ Como FAZER

### 🔴 Código Ruim (Sem Semântica - *"Div Soup"*)

> Funciona na tela, mas **nenhum** robô ou leitor de tela entende a estrutura:

```html
<div class="cabecalho">
  <h1>Nave Code-1</h1>
</div>

<div class="conteudo">
  <div class="secao">
    <div class="cartao">
      <p>Status da Missão</p>
    </div>
  </div>
</div>

<div class="rodape">
  <p>SENAI Space Program</p>
</div>
```

### 🟢 Código Profissional (Com Tags Semânticas)

> Estrutura limpa, legível, acessível e otimizada:

```html
<header>
  <h1>Nave Code-1</h1>
</header>

<main>
  <section>
    <article>
      <p>Status da Missão</p>
    </article>
  </section>
</main>

<footer>
  <p>SENAI Space Program</p>
</footer>
```

---

## 🚀 Por que usar Tags Semânticas?

1. **Acessibilidade:** Leitores de tela para pessoas com deficiência visual conseguem navegar pela página utilizando atalhos como *"Ir para o cabeçalho"* ou *"Ir para o conteúdo principal"*.
2. **SEO (Search Engine Optimization):** Os robôs de busca (como o Google) identificam quais informações são mais importantes, melhorando o posicionamento do site nos resultados.
3. **Organização e Manutenibilidade:** Torna o código mais limpo e fácil de entender/manter por outros desenvolvedores da equipe.
