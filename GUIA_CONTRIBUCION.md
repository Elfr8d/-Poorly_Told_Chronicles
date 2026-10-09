# 📜 Guía Oficial de Contribución: El Protocolo de Canonización

Bienvenido, cronista. Este documento establece las leyes y los comandos rituales para registrar nuevos hitos históricos en **-Poorly_Told_Chronicles**.

Toda vivencia, catástrofe o gloria debe ser ratificada formalmente mediante un **Pull Request** hacia la rama sagrada: **`Sagrada_linea_del_el_Tiempo`**.

---

## 🧭 Resumen Rápido en 5 Pasos

```text
1. Actualizar tu rama sagrada local
   git checkout Sagrada_linea_del_el_Tiempo
   git pull origin Sagrada_linea_del_el_Tiempo

2. Crear tu línea temporal alternativa
   git checkout -b evento/nombre-del-suceso

3. Redactar tu crónica usando la plantilla
   Copiar eventos/_PLANTILLA_EVENTO.md -> eventos/canon_grupal/ o eventos/integrantes/tu_nombre/

4. Subir tus cambios
   git add .
   git commit -m "Cronica: Registro de [Nombre del Hito]"
   git push origin evento/nombre-del-suceso

5. Abrir Pull Request hacia Sagrada_linea_del_el_Tiempo en GitHub
```

---

## 🛠️ Paso a Paso Detallado

### 1. Sincronizar con la Rama Sagrada
Antes de empezar a escribir, asegúrate de tener la última versión del multiverso:
```bash
git checkout Sagrada_linea_del_el_Tiempo
git pull origin Sagrada_linea_del_el_Tiempo
```

### 2. Abrir una Línea Temporal Alternativa (Nueva Rama)
Nunca escribas directamente sobre la rama principal. Crea una rama descriptiva para tu evento:
```bash
# Formato: evento/nombre-corto-del-evento
git checkout -b evento/el-cisma-del-servidor
```

### 3. Redactar tu Crónica
1. Ve a la carpeta `eventos/` y copia el archivo **`_PLANTILLA_EVENTO.md`**.
2. Guárdalo con un nombre representativo:
   * Si involucra a todo el grupo: en `eventos/canon_grupal/YYYY-nombre-evento.md`.
   * Si es tu propia historia o hazaña individual: en `eventos/integrantes/tu_nombre/YYYY-nombre-evento.md`.
3. Completa los campos del encabezado (Frontmatter):
   ```yaml
   ---
   layout: default
   titulo: "El Cisma del Servidor Moddeado"
   fecha: "2025" # Año (ej. 2025) o fecha completa YYYY-MM-DD para orden automático
   epoca: "La Gran Caída de los Chunks"
   autor: "TuNombre"
   estado: "En Debate" # Cambiará a "Canonizado" al aprobarse
   descripcion: "Breve sinopsis que aparecerá en la Línea Temporal Sagrada."
   ---
   ```
4. Escribe la crónica siguiendo las secciones de la plantilla.

### 4. Adjuntar Evidencia Visual (Imágenes y Capturas)
* Guarda tus imágenes dentro de:
  `assets/images/eventos/tu_nombre/tu_captura.png`
* *(No subas archivos de más de 10 MB. Procura que estén en formato `.png`, `.jpg` o `.webp`).*
* Enlaza la imagen en tu crónica así:
  ```markdown
  ![Momento exacto del desastre](/assets/images/eventos/tu_nombre/tu_captura.png)
  ```

### 5. Guardar y Enviar a GitHub
```bash
git add .
git commit -m "Cronica: Registro de [Nombre del Evento]"
git push origin evento/nombre-del-suceso
```

### 6. El Juicio del Cónclave (Abrir el Pull Request)
1. Entra al repositorio en GitHub: `https://github.com/Elfr8d/-Poorly_Told_Chronicles`.
2. Verás un botón verde que dice **"Compare & pull request"**.
3. **Asegúrate de que la rama base de destino sea:**  
   `base: Sagrada_linea_del_el_Tiempo` ⬅️ `compare: evento/nombre-del-suceso`.
4. Titula tu Pull Request con el nombre de tu crónica.
5. El grupo debatirá en los comentarios del PR si el suceso es fidedigno.
6. Una vez alcanzado el consenso, el administrador fusionará (*merge*) el Pull Request y el evento se convertirá oficialmente en **Canon Absoluto**.

---

### ✨ ¡La Línea Temporal se Actualiza Sola!
Gracias al sistema de Jekyll implementado en la web, **no necesitas editar el índice general ni la línea de tiempo a mano**. En el momento en que tu Pull Request sea aprobado y fusionado, GitHub Pages reconstruirá la web y tu nuevo hito aparecerá automáticamente colocado en su año correspondiente con su tarjeta y su enlace.
