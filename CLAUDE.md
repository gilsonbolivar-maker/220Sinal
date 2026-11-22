# Zap220 — regras do repositório

O app que o Gilson usa (o painel) se chama **Zap220** (antes 220Sinal); o repositório continua 220Sinal. Veio do repositório Oficina (pastas `220Sinal/` e `220Sinal-sinal/`), separado para ser só da área 220.

## Estrutura
- `painel/` = Zap220 (o painel do Gilson, lado que chama). O código fica em `painel/app.js` e `painel/app.css`.
- `aa220/` = AA220 (app dos colegas, lado que recebe). Carrega `../painel/app.js` e `../painel/app.css`.
- O convite do painel aponta para `../aa220/#c=…`.
- Guarda tudo com prefixo `220-` e usa tópicos `app-220sinal/`: não se mistura com o Zap232 nem com outras áreas.

## Versão
- A versão aparece ao lado do título, sempre.
- `const VERSAO = 'x.y.z'` em `painel/app.js`, `painel/sw.js` e `aa220/sw.js`, **com o mesmo valor**.
- Toda mudança sobe a versão no mesmo commit: correção → último número; recurso novo → do meio; mudança grande → primeiro.

## Android
- Fica em `painel/android` (APKs `aa220.apk` e `220sinal.apk`, workflow `.github/workflows/apk-220sinal.yml`).
- `Cifra.PREFIXO` precisa casar com o `PREFIXO` do `painel/app.js`.
- Para publicar os APKs, o repositório precisa dos segredos `SINAL_ASSINATURA` e `SINAL_SENHA` (os mesmos do Oficina), em Settings → Secrets and variables → Actions.

## Seletor de arquivo
Não use `accept=".json,…"` em `<input type="file">`: no iPad ele deixa os arquivos cinza.
