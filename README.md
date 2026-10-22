# ScreenCord

Página e downloads do ScreenCord: <https://screencord.miguelsoeth.online/>

O código do aplicativo está em [screencord.app](https://github.com/miguelsoeth/screencord.app) e o da API em [screencord.api](https://github.com/miguelsoeth/screencord.api), ambos abertos. Problemas e sugestões: [issues do app](https://github.com/miguelsoeth/screencord.app/issues).

Este repositório guarda a landing page (`index.html`, publicada pelo GitHub Pages a partir da `main`) e as [releases](https://github.com/miguelsoeth/screencord/releases) com o instalador para Windows. As releases são criadas automaticamente pelo pipeline de release do aplicativo; não crie releases aqui à mão.

Versões depreciadas ou com defeito são marcadas pelo `release-status.ps1` do repo do app (um comentário `<!-- screencord:status ... -->` no começo das notas). A página as tira da lista principal e as mostra em "Versões arquivadas", com o motivo e uma confirmação antes do download.

## Licença

O código da página (`index.html`) está sob a [licença MIT](LICENSE). O nome **ScreenCord**, o logo, os mascotes e as imagens (`icon.png`, `mascot-*.png`, `img/`) não fazem parte da licença.

O instalador publicado nas releases é o aplicativo ScreenCord, distribuído sob a GPL-3.0 (o texto vai junto, em `LICENSE.txt`, na pasta de instalação).
