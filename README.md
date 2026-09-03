# P2L Unidades — landing comercial

Sitio estático (pasajero, conductor, empresa), paralelo a `docs/gh-pages-tuki`.

- App (pasajero / conductor): https://www.refactorii.com/p2l-tenant/?redirect=/unidades
- Panel empresa: https://www.refactorii.com/p2l-tenant/?redirect=/unidades-dashboard
- GitHub Pages: https://wbsckt3.github.io/p2l-unidades-mobility/
- Repo: https://github.com/wbsckt3/p2l-unidades-mobility (rama `gh-pages`)

Publica el contenido de **esta carpeta** a la raíz de la rama `gh-pages`.

Página de tarifas (perfil Empresa): `tarifas-y-pagos.html`.

## i18n

Edita `locales/es.json` y `locales/en.json`, luego regenera el embed:

```bash
node -e "const fs=require('fs');const path=require('path');const d=__dirname;const es=JSON.parse(fs.readFileSync(path.join(d,'locales','es.json'),'utf8'));const en=JSON.parse(fs.readFileSync(path.join(d,'locales','en.json'),'utf8'));fs.writeFileSync(path.join(d,'scripts','locales-embed.js'),'window.UNIDADES_I18N_RESOURCES = '+JSON.stringify({es:{translation:es},en:{translation:en}})+';\\n');"
```
