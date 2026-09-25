# Wireframe — Café Cerrado

Este documento apresenta o wireframe (esboço de layout) de cada página do
portal. Os blocos representam a organização dos elementos, não a aparência
final. A identidade visual (cores, tipografia e imagens) é aplicada pelo CSS.

> Convenção dos blocos:
> `[ ... ]` = área/bloco de conteúdo · `( ... )` = botão · `___` = campo de formulário

---

## Estrutura comum (todas as páginas)

```text
+--------------------------------------------------------------+
|  ☕ Café Cerrado        Início  Variedades  Métodos  Contato  |   <- header + nav
+--------------------------------------------------------------+
|                                                              |
|                     [ CONTEÚDO DA PÁGINA ]                   |   <- main
|                                                              |
+--------------------------------------------------------------+
|  Café Cerrado   |   Navegação   |   Autoria                  |   <- footer
|  descrição      |   - links     |   Rodrigo A. O. Bastos     |
+--------------------------------------------------------------+
|                © 2026 Café Cerrado                           |
+--------------------------------------------------------------+
```

---

## 1. index.html — Página inicial

```text
+--------------------------------------------------------------+
| HEADER + MENU DE NAVEGAÇÃO                                   |
+--------------------------------------------------------------+
|                       [ HERO / BANNER ]                      |
|            Título grande + subtítulo + ( botões )            |
+--------------------------------------------------------------+
|                 "O que você vai encontrar"                   |
|   +-----------+     +-----------+     +-----------+          |
|   | [ IMG ]   |     | [ IMG ]   |     | [ IMG ]   |          |
|   | Variedades|     | Preparo   |     | Cultura   |   <- 3 cards (Flexbox)
|   | texto     |     | texto     |     | texto     |          |
|   | ( botão ) |     | ( botão ) |     | ( botão ) |          |
|   +-----------+     +-----------+     +-----------+          |
+--------------------------------------------------------------+
|         "Um país feito de café" (seção destaque)            |
|   [ TEXTO + ( botão ) ]        [ IMAGEM ]                    |   <- Flexbox texto+imagem
+--------------------------------------------------------------+
| FOOTER                                                       |
+--------------------------------------------------------------+
```

---

## 2. variedades.html — Página de conteúdo

```text
+--------------------------------------------------------------+
| HEADER + MENU                                                |
+--------------------------------------------------------------+
|                    [ HERO: "Variedades" ]                    |
+--------------------------------------------------------------+
|            "Principais tipos cultivados no Brasil"           |
|   +-----------+     +-----------+     +-----------+          |
|   | Arábica   |     | Conilon   |     | Especiais |   <- 3 cards
|   +-----------+     +-----------+     +-----------+          |
+--------------------------------------------------------------+
|  "O que influencia o sabor"                                 |
|   +------------------------------+    +------------------+   |
|   | [ LISTA de características ]  |    | ASIDE            |   |  <- conteúdo + aside
|   |  - Altitude                  |    | Regiões          |   |     (Flexbox)
|   |  - Clima e solo              |    | produtoras       |   |
|   |  - Colheita ...              |    | - Cerrado ...    |   |
|   +------------------------------+    +------------------+   |
+--------------------------------------------------------------+
| FOOTER                                                       |
+--------------------------------------------------------------+
```

---

## 3. metodos.html — Métodos de preparo

```text
+--------------------------------------------------------------+
| HEADER + MENU                                                |
+--------------------------------------------------------------+
|                  [ HERO: "Métodos de preparo" ]              |
+--------------------------------------------------------------+
|                     "Escolha o seu método"                   |
|   +-----------+     +-----------+     +-----------+          |
|   | Coado     |     | Prensa    |     | Espresso  |   <- 3 cards
|   +-----------+     +-----------+     +-----------+          |
+--------------------------------------------------------------+
|            "Passo a passo: café coado" (lista ordenada)     |
|   ( 1 ) Ferva a água ...                                    |
|   ( 2 ) Coloque o filtro ...                                |
|   ( 3 ) Umedeça o pó ...                                    |
+--------------------------------------------------------------+
|                 "Dicas para um café melhor"                  |
|   [ LISTA de dicas ]                                        |
+--------------------------------------------------------------+
| FOOTER                                                       |
+--------------------------------------------------------------+
```

---

## 4. contato.html — Sobre e contato

```text
+--------------------------------------------------------------+
| HEADER + MENU                                                |
+--------------------------------------------------------------+
|              [ HERO: "Sobre o projeto e contato" ]           |
+--------------------------------------------------------------+
|  "Sobre o Café Cerrado"                                     |
|   [ TEXTO ]                    [ IMAGEM ]                    |  <- Flexbox
+--------------------------------------------------------------+
|                      "Fale com o autor"                      |
|   +------------------------------------------------------+   |
|   |  Nome:      ______________________________          |   |
|   |  E-mail:    ______________________________          |   |  <- formulário
|   |  Assunto:   [ v seleção ]                            |   |
|   |  Mensagem:  ______________________________          |   |
|   |             ______________________________          |   |
|   |             ( Enviar mensagem )                      |   |
|   +------------------------------------------------------+   |
+--------------------------------------------------------------+
| FOOTER                                                       |
+--------------------------------------------------------------+
```

---

## Responsividade

Em telas menores (tablets e celulares), o layout se adapta:

```text
Desktop (3 colunas)        Tablet (menu centralizado)     Celular (empilhado)
+---+ +---+ +---+          +---+ +---+                     +-------+
|   | |   | |   |    -->   |   | |   |             -->     |       |
+---+ +---+ +---+          +---+ +---+                     +-------+
                          +---+                            +-------+
                          |   |                            |       |
                          +---+                            +-------+
                                                           +-------+
                                                           |       |
                                                           +-------+
```

- **Desktop:** cards em 3 colunas, menu na horizontal ao lado do logo.
- **Tablet (≤ 768px):** menu centralizado abaixo do logo, cards reorganizados.
- **Celular (≤ 480px):** menu vertical, cards e botões ocupando 100% da largura.
