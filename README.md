# The Beatles — Trabalho de Front-end 2

Site sobre os Beatles, feito em grupo pra faculdade. O tema foi dado pelo professor ("Banda") e a gente escolheu Beatles.

## Antes de tocar em qualquer código

Lê o briefing primeiro, tem tudo que o professor pediu, como a gente decidiu montar o site, cores, fontes, as 11 páginas, tudo:
👉 [Briefing do projeto](https://docs.google.com/document/d/11DTxg1GSmS0bQ-Pl0N_hmXWmHbfxiIsZ/edit)

Board com as páginas e quem tá fazendo o quê:
👉 [Project](https://github.com/users/wnsogabriel/projects/3)

Pasta no Drive (fotos, fontes, links):
👉 [Drive](https://drive.google.com/drive/folders/1OR083GTQEs939TgdsOqli17M2Il1lrY6)

## Como começar

1. Clona o repositório no GitHub Desktop
2. Vai no Project e vê qual Issue é sua. Tem um checklist do que a página precisa ter
3. No GitHub Desktop, em cima onde tá escrito "Current branch", clica e depois em "New branch". Dá um nome pra ela, pode ser o nome da sua página mesmo, tipo `john-lennon`
4. Edita o arquivo HTML da sua página (ele já existe, não precisa criar um novo)
5. Vai salvando e comitando enquanto trabalha, não precisa ser só 1 commit gigante no final
6. Quando terminar, no GitHub Desktop tem um botão de "Create Pull Request". Clica nele
7. Escreve na descrição o que você fez. Se fez alguma coisa diferente do que esse README diz, escreve isso também (tipo "usei uma cor que não tava na lista porque achei que ficou melhor aqui"). É só pra facilitar corrigir alguma coisa depois, se precisar
8. Um de nós aprova o PR e aí ele entra na página principal do site

Não sabe mexer em branch ainda? Sem problema, é só ir testando no GitHub Desktop mesmo, os botões são bem visuais. Se travar, chama no grupo.

## Cuidado pra não quebrar o projeto

A gente tem o histórico de commit salvo, então dá pra reverter se alguém fizer merda, mas é um saco ficar caçando o que quebrou. Antes de mexer em alguma coisa que não é só a sua página (tipo o `style.css` compartilhado, o menu, essas coisas), pensa duas vezes.

Se for usar agente de IA no IDE (Claude Code, Codex, Gemini, essas paradas), cuidado pra ele não quebrar a merda do projeto. Se for copiar e colar ou seguir instrução que a IA deu, procura saber o que tá fazendo antes de aceitar.

## Cores

Não usa código de cor direto (tipo `#C1121F`). Usa sempre uma dessas variáveis:

```css
color: var(--preto);
background-color: var(--vermelho);
```

Cores que já existem: `--branco`, `--preto`, `--cinza`, `--vermelho`

Se quiser usar uma cor nova que não tem na lista, tudo bem, mas cria ela como variável também, do jeito que as outras foram feitas lá no `:root` do `style.css`, em vez de jogar o código direto no meio do CSS.

## Fontes

Não precisa escrever `font-family` na mão, usa essas classes prontas:

- `.titulos` pra fonte grande de título de página
- `.paragrafo` pra fonte de texto normal
- `.destaque` pra fonte de citação (fica em itálico)

Exemplo:
```html
<h1 class="titulo">Biografia</h1>
<p class="paragrafo">Texto normal aqui...</p>
<p class="destaque">"Uma frase marcante aqui."</p>
```

## O CSS é compartilhado

Todo mundo usa o mesmo arquivo: `assets/css/style.css`. Não cria um CSS separado pra sua página.

Se precisar adicionar alguma coisa nova nesse arquivo, tipo uma classe que ainda não existe, pode adicionar direto, não precisa pedir autorização pra ninguém. Só manda mensagem no grupo se tiver alguma dúvida de como fazer.

## Estrutura da página

Usa `<section>` pra separar os blocos de conteúdo da sua página. Não usa `<div>` pra isso, só section mesmo, pra ficar tudo padronizado:

```html
<section>
    (um bloco de conteúdo)
</section>

<section>
    (outro bloco de conteúdo)
</section>
```

O espaçamento entre as sections já é automático, não precisa mexer em CSS pra isso.

## Bootstrap

Usa e abusa do Bootstrap (documentação: getbootstrap.com/docs/5.3). O professor pediu, e vale aproveitar já que não teve isso no Front-end 1. Classes mais usadas: `container`, `row`, `col`, `card`, `btn btn-primary`, `img-fluid`.

## O que já vem pronto

- Fontes já configuradas
- Cores já configuradas
- Navbar já pronta em todas as páginas
- Framework CSS: Bootstrap

## Conteúdo de cada página

Todo o conteúdo que você precisa (história, dados dos integrantes, discografia, curiosidades) já tá levantado no briefing. Não precisa pesquisar do zero, só copiar de lá e organizar na sua página.

## Comenta o código

Comenta o que cada parte faz, principalmente se for algo que os outros podem
reaproveitar. Tipo assim, se você fez uma seção de "ficha técnica" bonita na
sua página de integrante, comenta ali o que é:

```html
<!-- Ficha técnica do integrante: foto + nome + instrumento + datas -->
<section>
    ...
</section>
```

Assim, se outra pessoa for fazer algo parecido, não precisa ficar lendo
linha por linha pra entender o que tá rolando ali. Só olha o comentário, vê
se serve, copia e adapta.

Isso não é fazer tudo copiando dos outros sem pensar. O importante é você
entender o que o código faz antes de usar, não só copiar e colar sem saber
o porquê.
