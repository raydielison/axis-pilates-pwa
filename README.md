# axis-pilates-pwa

PWA do Studio de Pilates Axis com:

- home institucional (estilo site) com seções de serviços, horários e contato;
- autenticação por e-mail/senha usando Firebase;
- instalação como app (manifest + prompt de instalação);
- cache offline básico via Service Worker.

## Verificação rápida do PWA

- Manifesto principal em `manifest.json` (compatível também com `manifest.webmanifest`);
- Service Worker registrado em `service-worker.js`;
- Cache estático controlado em `sw.js`.

Comandos úteis de validação:

```bash
python3 -m json.tool manifest.json >/dev/null
python3 -m http.server 4173 --bind 0.0.0.0
curl -I http://127.0.0.1:4173/manifest.json
curl -I http://127.0.0.1:4173/service-worker.js
```


> Observação: os ícones/logomarca estão em SVG (texto), sem dependência de arquivos binários no repositório.
