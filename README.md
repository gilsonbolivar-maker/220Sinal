# 220Sinal
Comunicação da área 220.

- `painel/` — **Zap220**, o painel do Gilson (lado que chama). O código do app mora aqui (`painel/app.js`).
- `aa220/` — **AA220**, o app dos colegas (lado que recebe). Carrega `../painel/app.js`.
- `painel/android/` — os dois APKs (`aa220.apk` e `220sinal.apk`), compilados pelo workflow `apk-220sinal.yml`.

Endereços (GitHub Pages):
- https://gilsonbolivar-maker.github.io/220Sinal/painel/
- https://gilsonbolivar-maker.github.io/220Sinal/aa220/
