# sos-chuva-web

## Rodando localmente com Docker

O site é estático, servido por `python3 -m http.server` dentro de um container:

```bash
docker compose up -d
```

Acesse http://localhost:8000

Para usar outra porta:

```bash
PORT=3000 docker compose up -d
```

Para parar:

```bash
docker compose down
```

Os arquivos do projeto são montados como volume somente leitura, então alterações
em `index.html`, `css/` e `img/` aparecem ao recarregar a página — sem rebuild.
