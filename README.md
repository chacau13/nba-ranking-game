# NBA Ranking Game

Jogo estático em HTML/CSS/JavaScript.

## Arquivos

- `index.html`: código completo do jogo.
- `dados/`: pasta com os arquivos CSV.
- `dados/sorteio.csv`: lista dos jogadores que podem ser sorteados.

## Estrutura dos CSVs de ranking

Cada CSV de ranking deve ter ao menos estas colunas:

```csv
Rk,Player
1,LeBron James
2,Kareem Abdul-Jabbar
3,Karl Malone
```

O código procura a coluna `Rk` ou `Rank` para definir a posição real. Se essa coluna não existir, ele usa a ordem das linhas.

## Arquivos esperados

```text
dados/jogos.csv
dados/pontos.csv
dados/fg3.csv
dados/assistencias.csv
dados/fta.csv
dados/rebotes_ofensivos.csv
dados/rebotes_defensivos.csv
dados/steals.csv
dados/blocks.csv
dados/turnovers.csv
dados/sorteio.csv
```

## Estrutura do sorteio.csv

```csv
Player
LeBron James
Kareem Abdul-Jabbar
```

Use apenas jogadores que estejam presentes nos 10 rankings.

## Pontuação

A pontuação final é calculada assim:

```text
1 - (soma dos deltas / 2490)
```

O denominador 2490 vem de:

```text
10 categorias × 249 de diferença máxima por categoria
```

## Teste local

Se abrir `index.html` com duplo clique, alguns navegadores podem bloquear a leitura dos CSVs. Para testar localmente, use a extensão Live Server no VS Code.

## Publicação gratuita

Suba todos os arquivos para um repositório no GitHub e publique com GitHub Pages. É importante subir também a pasta `dados/`.
