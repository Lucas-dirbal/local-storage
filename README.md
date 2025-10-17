# local-storage

## Nota sobre Node >=17 e erro OpenSSL

Se ao iniciar o Metro/Expo você receber o erro `ERR_OSSL_EVP_UNSUPPORTED`, é por causa de uma incompatibilidade entre OpenSSL em Node >=17 e algumas dependências (Metro). As opções para resolver são:

- Usar Node 16 (recomendado para desenvolvimento com esta versão do Expo).
- Prefixar os scripts do npm com a variável de ambiente `NODE_OPTIONS=--openssl-legacy-provider` (feito nos scripts do package.json).
- Instalar e usar `cross-env` para compatibilidade entre sistemas: `npm install --save-dev cross-env` e atualizar os scripts para `cross-env NODE_OPTIONS=--openssl-legacy-provider expo start`.

Exemplo para rodar web sem instalar nada extra:

```bash
npm run web
```

Se preferir mudar o Node, ferramentas como `nvm` ou `fnm` permitem alternar versões rapidamente.
