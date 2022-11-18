# Deploy to Github Page [Typescript Tips | typescript-tips](https://jellydn.github.io/typescript-tips/)

## Step 1: Sync the change from `main` branch to `gh-pages` branch

## Step 2: Create index.md from readme.md and replace `.md` with `.html`

```sh
cp readme.md to index.md
```

## Step 3: Change the configuration on \_.config.yaml

Add all markdown files to the config. For example:

```yaml
plugins:
  - jekyll-relative-links
relative_links:
  enabled: true
  collections: true
include:
  - Carlillo - 1591148366070747347.md
  - mgechev - 1462654597059817481.md
  - code-of-conduct.md
  - readme.md
  - contributing.md
  - stackblitz - 1325818478675304448.md
  - housecor - 1581638360543600640.md
  - stackblitz - 1328353096179789824.md
  - housecor - 1586865516395876359.md
  - stackblitz - 1330890655351123968.md
  - mattpocockuk - 1509964736275927042.md
  - sulco - 1160890708615716864.md
  - mattpocockuk - 1542079199543975937.md
  - wesbos - 1524040757518258176.md
  - mattpocockuk - 1591047557702389760.md
  - wesbos - 1584905090628034560.md
  - mattpocockuk - 1592130978234900484.md
  - wesbos - 1585641232155348992.md
  - mgechev - 1309379618034642946.md
  - wesbos - 1587082842110033926.md
  - mgechev - 1361186013029269506.md
```

Please refer to [pages build and deployment · jellydn/typescript-tips@45cd36c](https://github.com/jellydn/typescript-tips/actions/runs/3497633573)

Credits to [mryap/markdown-to-github-pages: Turn a folder of markdown files into website without using command-line tools](https://github.com/mryap/markdown-to-github-pages)
