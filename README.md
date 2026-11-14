# 🐱 Cat Trap Adventure

Um jogo de plataforma 2D em HTML5 Canvas, no estilo "troll game" de *Cat Mario* (Syobon Action): tudo parece normal, mas quase tudo é uma armadilha. Sem dependências, sem build: é só abrir e jogar.

> Projeto de fã, sem vínculo com Nintendo ou com o autor de Syobon Action. Todos os gráficos são desenhados em código HTML.

## Jogar

- **Local:** abra o `index.html` no navegador, ou rode `python3 -m http.server` e acesse `http://localhost:8000`.
- **Online:** ative o GitHub Pages (Settings → Pages → Source: *GitHub Actions*). O workflow em `.github/workflows/pages.yml` publica a cada push na `main`.

## Controles

| Ação | Teclas |
|---|---|
| Andar | ← → ou A D |
| Pular | Espaço, ↑ ou W (segure para pular mais alto) |
| Reiniciar | R |

## Armadilhas da fase 1

- **Bloco invisível** sobre o buraco, que barra o seu pulo.
- **Chão falso** que some pouco depois de você pisar.
- **Espinho que cai** do teto quando você passa embaixo.
- **Espinho que sobe** do chão quando você chega perto.
- **Bandeira que foge** quando você se aproxima.

## Estrutura

```
cat-trap-adventure/
├── index.html
├── css/style.css
├── js/
│   ├── level.js      # dados da fase (tiles e entidades)
│   └── game.js       # loop, física, colisão, armadilhas e desenho
├── .github/workflows/pages.yml
├── LICENSE
└── README.md
```

## Como criar uma armadilha nova

1. Em `js/level.js`, adicione uma entidade na lista `ents` com um novo `t` (tipo).
2. Em `js/game.js`, trate o tipo em `updateEnts()` (comportamento) e em `drawEnt()` (visual).

## Roadmap

- [ ] Várias fases (carregar de arquivos JSON)
- [ ] Controles de toque para celular
- [ ] Sons e música (Web Audio)
- [ ] Sprites em pixel art
- [ ] Mais inimigos e blocos (plataforma móvel, cano traiçoeiro, nuvem assassina)
- [ ] Placar com tempo e número de mortes

## Contribuindo

Pull requests são bem-vindos. Abra uma issue para discutir ideias de armadilhas antes de implementar.

## Licença

[MIT](LICENSE)
