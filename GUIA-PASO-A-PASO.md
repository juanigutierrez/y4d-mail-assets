# Guía completa — Y4D Mail Assets con GitHub Pages

Esta guía replica la lógica utilizada en el repositorio de recursos de Politeia, pero adaptada para **Youth for Democracy (Y4D)**, **Kairos Global**, las identidades regionales, partners y ediciones provinciales.

---

## 1. Qué vas a tener al final

Vas a tener:

- un repositorio público de GitHub;
- una biblioteca web visible con GitHub Pages;
- una URL pública estable para cada logo, flyer o imagen;
- un buscador para encontrar archivos;
- filtros por Y4D, Kairos, regiones, partners, ediciones y flyers;
- un botón para copiar la URL pública lista para insertar en un email HTML.

Ejemplo de estructura de URL:

```text
https://TU-OWNER.github.io/y4d-mail-assets/brand/y4d/y4d-logo.png
```

`TU-OWNER` será el usuario u organización de GitHub que sea propietario del repositorio.

---

## 2. Crear el repositorio

1. Ingresá a GitHub con la cuenta u organización que deba ser propietaria del repositorio.
2. Elegí **New repository**.
3. Nombre recomendado:

```text
y4d-mail-assets
```

4. Descripción recomendada:

```text
Recursos gráficos para comunicaciones HTML de Youth for Democracy y Kairos Global
```

5. Elegí **Public**.
6. Podés crear el repositorio vacío. Si GitHub te pide inicializarlo, también puede tener un README; después se reemplaza por el de este paquete.
7. Creá el repositorio.

IMPORTANTE: GitHub Pages publica estos archivos en Internet. No subas datos personales, documentos internos, bases de participantes, presupuestos, contraseñas, archivos sensibles ni material que no deba ser público.

---

## 3. Subir los archivos iniciales

Subí al repositorio, en la rama `main`, como mínimo:

```text
index.html
.nojekyll
README.md
GUIA-PASO-A-PASO.md
ESTRUCTURA-DE-CARPETAS.md
```

Luego conservá las carpetas del paquete.

Git no conserva carpetas vacías. Por eso este paquete incluye archivos `.gitkeep`; pueden permanecer allí hasta que cada carpeta tenga imágenes reales.

---

## 4. Activar GitHub Pages

En el repositorio:

1. Abrí **Settings**.
2. En el menú lateral, entrá en **Pages**.
3. En **Build and deployment**, buscá **Source**.
4. Elegí **Deploy from a branch**.
5. En **Branch**, seleccioná:

```text
main
```

6. En carpeta seleccioná:

```text
/(root)
```

7. Guardá con **Save**.

GitHub va a desplegar el sitio. La primera publicación puede tardar algunos minutos.

La dirección normalmente tendrá esta forma:

```text
https://TU-OWNER.github.io/y4d-mail-assets/
```

---

## 5. Verificar que funciona

Abrí la URL de GitHub Pages.

La portada debe mostrar:

- el encabezado de Youth for Democracy;
- el buscador;
- el filtro de categorías;
- las imágenes que ya hayas cargado;
- un botón **Copiar link**;
- un botón **Abrir**.

Si todavía no cargaste imágenes, la biblioteca aparecerá vacía. Eso es correcto.

---

## 6. Subir el logo de Youth for Democracy

Guardalo dentro de:

```text
brand/y4d/
```

Ejemplo:

```text
brand/y4d/y4d-logo-horizontal.png
```

Después de confirmar el commit y esperar el despliegue, aparecerá automáticamente en la biblioteca.

Su enlace público será aproximadamente:

```text
https://TU-OWNER.github.io/y4d-mail-assets/brand/y4d/y4d-logo-horizontal.png
```

Ese es el enlace que debe utilizarse en el HTML del correo.

---

## 7. Subir el logo de Kairos Global

Ubicar los recursos permanentes de Kairos en:

```text
brand/kairos/
```

Ejemplo:

```text
brand/kairos/kairos-logo-horizontal.png
```

No mezclar logos de Kairos con los de Y4D, porque después el sistema de correos necesita poder distinguir qué identidad corresponde.

---

## 8. Recursos regionales de Y4D

La estructura prevista es:

```text
regions/metro/
regions/cuyo/
regions/patagonia/
regions/pampeana/
regions/noreste/
regions/noroeste/
```

Acá deben guardarse únicamente recursos visuales regionales reutilizables.

No hace falta crear una imagen por cada color si el color puede aplicarse directamente mediante CSS en el HTML. Esta carpeta sirve para elementos gráficos reales: headers, isotipos, patrones, placas base u otros recursos aprobados.

Paleta Y4D utilizada en el sistema actual:

### Base Y4D

```text
Principal:  #39a5c3
Highlights: #41bddf
Oscuro:     #013263
```

### Metro

```text
Fuerte: #ff0049
Pastel: #df3565
```

### Cuyo

```text
Fuerte: #5a72ff
Pastel: #6a74ba
```

### Patagonia

```text
Fuerte: #0072dc
Pastel: #0053a1
```

### Pampeana

```text
Fuerte: #98c83f
Pastel: #98e159
```

### Noreste

```text
Oscuro: #ff3e3e
Claro:  #ff1616
```

### Noroeste

```text
Fuerte: #ffb000
Pastel: #fccc61
```

---

## 9. Recursos por edición

Los archivos propios de una edición concreta deben organizarse por año y provincia.

Ejemplo:

```text
editions/2026/chubut/
editions/2026/mendoza/
editions/2026/santa-fe/
```

Dentro de cada carpeta pueden convivir:

```text
convocatoria.png
recordatorio.png
seleccionados.png
agenda.png
cierre.png
```

La nomenclatura debe permitir saber qué archivo es sin abrirlo.

---

## 10. Flyers

Si una pieza no pertenece todavía a una edición organizada o sirve transversalmente, puede ir a:

```text
flyers/
```

Sin embargo, para piezas provinciales conviene priorizar `editions/AÑO/PROVINCIA/` para que el archivo quede históricamente ordenado.

---

## 11. Logos de partners

Los logos de aliados se guardan en:

```text
partners/
```

Ejemplo:

```text
partners/embajada-eeuu.png
partners/amicana.png
partners/suricana.png
```

El hecho de que un logo exista en el repositorio NO significa que deba aparecer en todos los mails.

Su uso siempre depende de la actividad concreta y de la relación institucional correspondiente.

---

## 12. Cómo obtener el link para un correo

1. Abrí la biblioteca de GitHub Pages.
2. Buscá el recurso.
3. Tocá **Copiar link**.
4. Pegá ese enlace dentro del HTML.

Ejemplo:

```html
<img
  src="https://TU-OWNER.github.io/y4d-mail-assets/brand/y4d/y4d-logo-horizontal.png"
  alt="Youth for Democracy"
  style="display:block; width:100%; max-width:220px; height:auto; border:0;"
>
```

Nunca utilices el link de la página de GitHub que dice `/blob/main/...` dentro de `<img>`.

Usá la URL pública de GitHub Pages que copia la biblioteca.

---

## 13. Cómo subir una imagen nueva desde GitHub web

1. Entrá al repositorio.
2. Abrí la carpeta correcta.
3. Elegí **Add file** → **Upload files**.
4. Arrastrá el archivo.
5. Revisá el nombre.
6. En el mensaje de commit escribí algo descriptivo, por ejemplo:

```text
Add Chubut 2026 convocatoria flyer
```

7. Confirmá el commit en `main`.
8. Esperá unos minutos.
9. Abrí la biblioteca de Pages y actualizá.
10. Buscá la imagen y copiá su link.

---

## 14. Cómo reemplazar una imagen sin romper el link

Si querés corregir una imagen y conservar la misma URL del HTML:

1. utilizá exactamente la misma carpeta;
2. utilizá exactamente el mismo nombre de archivo;
3. reemplazá el archivo en GitHub;
4. confirmá el commit;
5. esperá el nuevo despliegue.

La URL seguirá siendo la misma.

Esto es útil para corregir una pieza sin tener que editar todos los mails o plantillas que ya utilizan esa dirección.

IMPORTANTE: no utilizar esta técnica si el archivo viejo debe conservarse históricamente. En ese caso, crear una versión nueva con un nombre nuevo.

---

## 15. Cómo eliminar un recurso

Solo eliminar si estás seguro de que ningún correo, documento o plantilla activa depende de esa URL.

Si se elimina el archivo, cualquier `<img>` que apunte a esa dirección dejará de mostrarlo.

Para activos permanentes de marca, lo más seguro es mantenerlos y reemplazarlos únicamente cuando exista una decisión formal de identidad.

---

## 16. Qué archivos deben considerarse permanentes

Conviene tratar como recursos permanentes:

- logo principal de Y4D;
- logo alternativo de Y4D para fondos oscuros;
- logo de Kairos Global;
- versiones institucionales aprobadas;
- recursos generales de marca;
- gráficos regionales reutilizables.

Los flyers y piezas de una actividad son recursos variables.

---

## 17. Seguridad y privacidad

Este repositorio existe para recursos gráficos públicos.

NO subir:

- bases de participantes;
- teléfonos;
- correos personales;
- documentos de identidad;
- presupuestos internos;
- comprobantes;
- datos de selección;
- evaluaciones;
- contraseñas;
- archivos privados de Embajadas o partners;
- documentación institucional sensible.

Asumí que todo archivo del repositorio puede ser visto por cualquier persona en Internet.

---

## 18. Qué hacer cuando el sitio no actualiza

1. Confirmá que el archivo está en `main`.
2. Revisá **Actions** en GitHub para comprobar el deployment de Pages.
3. Revisá **Settings → Pages** y confirmá que siga configurado como `main / (root)`.
4. Esperá algunos minutos y recargá la página.
5. Probá abrir directamente la URL del archivo.
6. Si el nombre contiene espacios o caracteres especiales, usá el botón **Copiar link** de la biblioteca para evitar errores de codificación.

---

## 19. Regla para los prompts de correo Y4D

Una vez que el repositorio esté activo, los prompts de correos deben dejar de pedir que se “busque” un logo permanente.

Los recursos permanentes deben documentarse con sus URLs oficiales.

Por ejemplo:

```text
Y4D — logo principal
https://TU-OWNER.github.io/y4d-mail-assets/brand/y4d/y4d-logo-horizontal.png

Kairos Global — logo principal
https://TU-OWNER.github.io/y4d-mail-assets/brand/kairos/kairos-logo-horizontal.png
```

Los flyers nuevos sí deben seguir confirmándose actividad por actividad.

---

## 20. Mantenimiento recomendado

Cada cierto tiempo:

- revisar duplicados;
- normalizar nombres;
- mover piezas provinciales a su edición;
- no borrar activos permanentes sin revisar dependencias;
- conservar únicamente versiones institucionalmente válidas de logos;
- evitar que `partners/` se convierta en una carpeta desordenada;
- comprobar que la biblioteca de Pages siga cargando correctamente.

La lógica del repositorio es simple: **un lugar público, estable y ordenado para todos los recursos que deban renderizarse dentro de comunicaciones HTML de Y4D y Kairos Global.**
