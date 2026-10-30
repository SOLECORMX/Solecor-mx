# Solecor MX — Web corporativa premium

Sitio estático responsive creado con HTML, CSS y JavaScript, sin frameworks ni suscripciones.

## Antes de publicar
1. WhatsApp configurado: +52 228 300 5702. El formulario abre una conversación con mensaje preparado.
2. Logotipo oficial y fotografía proporcionada integrados. Puedes agregar más fotografías de instalaciones cuando las tengas.
3. Revisa y aprueba todos los textos comerciales y las afirmaciones antes de publicarlos.
4. La calculadora muestra escenarios ilustrativos de reducción del recibo (50%, 70% o 90%). No estima producción fotovoltaica real ni garantiza ahorros.
5. Tras publicar, configura la URL canónica, sitemap y Google Search Console para solicitar indexación. La indexación y el posicionamiento no están garantizados.

## Publicación gratis con GitHub Pages
1. Crea una cuenta gratuita en https://github.com/.
2. Crea un repositorio público llamado `solecor-mx` (o `USUARIO.github.io` para la raíz).
3. Sube los archivos de esta carpeta directamente a la raíz del repositorio.
4. En Settings → Pages, selecciona Deploy from a branch, `main`, carpeta `/(root)` y guarda.
5. Espera a que GitHub indique la URL de publicación; para `solecor-mx` será `https://USUARIO.github.io/solecor-mx/`.
6. Prueba el formulario, los enlaces y el diseño en celular.

El sitio usa Google Fonts (requiere conexión para esas tipografías; si no hay conexión usa Arial). No almacena datos personales en servidor. El formulario construye un mensaje para WhatsApp, que el visitante decide enviar.

Contacto oficial: 228 300 5702 · soluciones.solecor@gmail.com.

Nota: la indexación en Google no es inmediata ni está garantizada; tras publicar configura Search Console.


## Catálogo de proyectos (nuevo)
- Abre `proyectos.html` desde la navegación principal. Los filtros funcionan por categorías: residencial, comercial e industrial.
- Inicialmente `proyectos.json` contiene una lista vacía, porque aún no hay proyectos verificados para publicar. Se muestra un mensaje de próxima disponibilidad.
- Para agregar un proyecto, copia tus fotos en `assets/proyectos/` y añade un objeto a la lista `proyectos` en `proyectos.json`, con esta estructura:

```json
{
  "titulo": "Instalación solar en vivienda",
  "categoria": "residencial",
  "ubicacion": "Xalapa, Veracruz",
  "descripcion": "Descripción real del proyecto",
  "portada": "assets/proyectos/vivienda-01.jpg",
  "imagenes": ["assets/proyectos/vivienda-01.jpg", "assets/proyectos/vivienda-02.jpg"],
  "potencia_kwp": 5.4,
  "paneles": 9,
  "anio": 2026
}
```

Los valores son **solo un ejemplo de formato**, no datos reales de Solecor. No publiques información o imágenes sin autorización del cliente. Las fotografías deben estar optimizadas para web.

**Vista previa local:** al abrir `proyectos.html` directamente como archivo (`file://`), algunos navegadores bloquean la lectura de `proyectos.json`. En GitHub Pages funciona. Para probarlo localmente con proyectos cargados, desde la carpeta `solecor-mx` ejecuta `python3 -m http.server 8000` y visita `http://localhost:8000/proyectos.html`.


## Actualización de galería (30 octubre 2026)
Se agregaron diez fotografías facilitadas por Solecor en `assets/proyectos/`, optimizadas a WebP. La galería funciona directamente abriendo `proyectos.html` sin servidor local porque los datos se cargan desde `proyectos-data.js`. Las fotografías se muestran sin adjudicar una ciudad, cliente, tipo de sistema ni potencia específicos. Para actualizar el catálogo, editar `proyectos-data.js` y mantener sincronizado `proyectos.json`.

## Ubicaciones confirmadas (30 octubre 2026)
El responsable de Solecor confirmó las ciudades asignadas a los 10 proyectos. Se retiraron las etiquetas provisionales. Las fichas técnicas y la clasificación residencial/comercial/industrial aún no se han documentado.
