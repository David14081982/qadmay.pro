# QADMAY

Web estática para https://qadmay.pro/.

## Archivos publicados

- `index.html`: página principal.
- `support.js`: runtime de la página; requiere conexión a unpkg.com.
- `assets/`: imágenes.
- `CNAME`: dominio personalizado.
- `.nojekyll`: desactiva el procesamiento de Jekyll.

La carpeta local `uploads/` contiene materiales originales que no utiliza la web y no se incluye en el repositorio.

## Publicación en GitHub Pages

1. Subir los archivos a un repositorio llamado `qadmay.pro`.
2. En Settings > Pages, seleccionar Deploy from a branch, rama `main`, carpeta `/ (root)`.
3. Configurar Custom domain como `qadmay.pro`.
4. Después de configurar Pages, conectar los DNS del dominio en Hostinger:

| Tipo | Nombre | Destino |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | David14081982.github.io |

El destino de `www` supone que el repositorio pertenece a David14081982; ajustarlo si se utiliza otra cuenta. Revisar registros A/AAAA anteriores para evitar destinos incompatibles. Conservar los registros de correo MX/TXT.

5. Cuando GitHub valide el dominio y emita el certificado, activar Enforce HTTPS.

Guía oficial: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Vista previa

Ejecutar `python -m http.server 8000` y abrir http://localhost:8000/.

Editar `index.html` para actualizar la página publicada.
