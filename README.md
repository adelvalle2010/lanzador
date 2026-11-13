# Lanzadera

Hub de las aplicaciones web del Prof. Andrés del Valle: cursos, simuladores, actividades y herramientas en un solo lugar.

**Sitio:** https://adelvalle2010.github.io/lanzador/

## Cómo se guardan las apps

La lista vive en `apps.json`. Desde la página, con GitHub conectado (botón de estado arriba a la derecha → «Guardar para siempre»), cada alta, edición, borrado o cambio de categoría se guarda directamente en este archivo como un commit. Así queda permanente y se ve igual en cualquier dispositivo.

Para conectar se usa un token *fine-grained* de GitHub con acceso solo a este repositorio y permiso **Contents: Read and write**. El token queda guardado únicamente en el navegador donde se pega. Quien entra sin token ve la Lanzadera en modo lectura.

## Funciones

- Portada con captura automática de cada sitio, ícono y descripción automáticos (o los que elijas).
- Categorías con nombre, ícono, color y orden.
- Favoritas, «Abiertas hace poco», búsqueda (`/`, `Enter` abre la primera), vista en tarjetas o lista.
- Compartir cualquier app (o la Lanzadera) con enlace y código QR, con modo para proyectar en clase.
- Tema claro / oscuro / automático. Se puede instalar como app desde el navegador.
- Exportar e importar `apps.json`.

## Formato de `apps.json`

```json
{
  "version": 2,
  "categories": { "Java Web": { "color": 1, "icon": "☕", "order": 0 } },
  "apps": [
    { "id": "doget", "name": "doGet", "url": "https://…", "category": "Java Web",
      "icon": "", "description": "", "image": "", "favorite": false, "createdAt": 0 }
  ]
}
```

`color` va de 1 a 6. Los campos vacíos se completan solos en pantalla.
