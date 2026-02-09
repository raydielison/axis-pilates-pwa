# axis-pilates-pwa
app PWA AXIS

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


## Dados revisados para implementação

### Identidade
- Nome: **Studio de Pilates Axis**
- Nome curto (PWA): **Axis Pilates**
- Tema principal: `#763000`

### Unidade e contato (site/app)
- Endereço: **Rua Ponte Nova, 354, sala 202, Colégio Batista, Belo Horizonte - MG**
- Horário: **segunda a sexta, 07h às 21h**
- WhatsApp: **(31) 98845-4857**
- E-mail: **studiodepilatesaxis@gmail.com**

### Planos públicos exibidos
- 2x por semana: **R$280,00**
- 3x por semana: **R$320,00**
- Massoterapia: **R$150,00 / 50 min**
- Fisioterapia: **consulte valores**

### Autenticação/admin (estado atual)
- Login e cadastro via Firebase Auth (e-mail/senha)
- Admin principal configurado: `studiodepilatesaxis@gmail.com`
- Painel admin com criação/exclusão de logins e edição de informações exibidas no app

> Se esses dados estiverem validados por você, o próximo passo é separar isso em configuração central (arquivo JSON/Firestore) para não ficar hardcoded no `index.html`.
