# ScreenCord

Página e downloads do ScreenCord: <https://screencord.miguelsoeth.online/>

O código do aplicativo está em [screencord.app](https://github.com/miguelsoeth/screencord.app) e o da API em [screencord.api](https://github.com/miguelsoeth/screencord.api), ambos abertos. Problemas e sugestões: [issues do app](https://github.com/miguelsoeth/screencord.app/issues).

Este repositório guarda a landing page (`index.html`, publicada pelo GitHub Pages a partir da `main`) e as [releases](https://github.com/miguelsoeth/screencord/releases) com o instalador para Windows. As releases são criadas automaticamente pelo pipeline de release do aplicativo; não crie releases aqui à mão.

Versões depreciadas ou com defeito são marcadas pelo `release-status.ps1` do repo do app (um comentário `<!-- screencord:status ... -->` no começo das notas). A página as tira da lista principal e as mostra em "Versões arquivadas", com o motivo e uma confirmação antes do download.

## Verificar o instalador

O instalador (`ScreenCord-Setup-<versão>-x64.msi`) é gerado pelo [workflow de release](https://github.com/miguelsoeth/screencord.app/blob/main/.github/workflows/release.yml) do repo do app, nos servidores do GitHub Actions, a partir da tag da versão; ninguém o envia à mão. Para conferir o arquivo que você baixou:

1. Na página da [release](https://github.com/miguelsoeth/screencord/releases), o SHA-256 aparece ao lado do arquivo e nas notas, em "Verificar o instalador". A landing page mostra o da versão mais recente abaixo do botão de download.
2. No PowerShell, na pasta do download, compare com o do seu arquivo:

   ```powershell
   Get-FileHash .\ScreenCord-Setup-0.9.0-x64.msi -Algorithm SHA256
   ```

3. Veja a análise no VirusTotal: `https://www.virustotal.com/gui/file/<sha256>`. As notas de cada release já trazem esse link, e o pipeline envia o instalador ao VirusTotal quando a release é criada.

O instalador ainda não é assinado digitalmente, por isso o Windows SmartScreen pode avisar na primeira execução.

## Licença

O código da página (`index.html`) está sob a [licença MIT](LICENSE). O nome **ScreenCord**, o logo, os mascotes e as imagens (`icon.png`, `mascot-*.png`, `img/`) não fazem parte da licença.

O instalador publicado nas releases é o aplicativo ScreenCord, distribuído sob a GPL-3.0 (o texto vai junto, em `LICENSE.txt`, na pasta de instalação).
