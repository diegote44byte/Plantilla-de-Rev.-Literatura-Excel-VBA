

# Registro para Revisión de Literatura

Plantilla de Excel con macros para **fichar y organizar las fuentes de una investigación** (tesis, artículos, trabajos de curso). Está pensada para economía, pero sirve para cualquier disciplina.

Llenas un formulario por cada paper, pulsas **Guardar** y la fuente pasa a una base de datos ordenada. Desde ahí puedes filtrarla, buscarla, editarla o eliminarla.

## ¿Para qué sirve?

Cuando revisas decenas de papers, la información termina repartida entre PDFs, notas sueltas y documentos de Word. Esta plantilla te ayuda a:

- **Registrar cada fuente con la misma estructura**: pregunta, datos, método, resultados, brecha y relación con tu tesis.
- **Comparar estudios rápidamente**: con los filtros de la tabla puedes ver, por ejemplo, todos los que usan *diferencias en diferencias* o todos los que estudian Perú.
- **Encontrar brechas de investigación**, porque tienes en un solo lugar lo que cada autor encontró y lo que dejó pendiente.
- **Redactar tu marco teórico y tu estado del arte** a partir de fichas ya resumidas y con su cita lista.

## Funcionalidades

| Botón / acción | Qué hace |
|---|---|
| **Guardar nueva** | Valida los campos obligatorios (Autores, Año y Título), avisa si el título ya existe, asigna un ID automático y guarda la fuente en la tabla. |
| **Buscar** | Busca por ID o por una palabra del autor o del título, y carga la fuente en el formulario. |
| **Actualizar** | Guarda los cambios de la fuente cargada en su misma fila. |
| **Eliminar** | Borra la fuente después de pedirte confirmación. |
| **Limpiar** | Vacía el formulario. |
| **Doble clic en un ID** | Desde la hoja *Literatura*, carga esa fuente en el formulario para editarla. |
| **Listas desplegables** | País / Contexto, Metodología y Unidad de análisis. También aceptan valores propios y se editan en la hoja *Listas*. |

## Campos de cada ficha

`Autores` · `Año` · `Título` · `Journal` · `País / Contexto` · `Pregunta de investigación` · `Teoría / Marco conceptual` · `Datos` · `Metodología` · `Variable dependiente` · `Variables clave` · `Resultados principales` · `Brecha identificada` · `Contribución` · `Relación con mi tesis` · `Unidad de análisis` · `Cita`

## Estructura del libro

| Hoja | Contenido |
|---|---|
| **Registro de fuente** | Formulario de ingreso, con botones y una guía para cada campo. |
| **Literatura** | Base de datos de todas las fuentes, en la tabla `tblLiteratura`, con filtros. |
| **Listas** | Opciones de las listas desplegables, que puedes editar. |

## Cómo usarla

1. Descarga `plantilla_rev_literatura_economia_v2.xlsm`.
2. Ábrela en **Microsoft Excel para escritorio** (Windows o Mac) y pulsa **Habilitar contenido** para activar las macros.
   - Si Windows bloquea las macros de un archivo descargado, haz clic derecho sobre el archivo, ve a **Propiedades**, marca **Desbloquear** y pulsa **Aceptar**.
3. Completa el formulario y pulsa **Guardar nueva**. ¡Listo!

> ⚠️ Las macros no funcionan en Excel Online, Google Sheets ni LibreOffice. En esos programas puedes ver los datos, pero los botones no hacen nada.

## Personalizar

- **Agregar un campo:** inserta una fila en el formulario antes de la fila 24 y agrega una columna en la tabla de *Literatura* con **exactamente el mismo nombre**. La macro la reconoce sola.
- **Cambiar las opciones de las listas:** edita la hoja *Listas* sin dejar filas vacías en medio.
- **Cambiar los campos obligatorios:** edita la constante `OBLIGATORIOS` en `vba/modRegistro.bas`.

## Código fuente

El código VBA está en la carpeta [`vba/`](vba/) para que puedas revisarlo sin abrir Excel:

- `modRegistro.bas` contiene la lógica de los botones (guardar, buscar, actualizar, eliminar).
- `Literatura_Hoja2.cls` contiene el evento de doble clic en la hoja *Literatura*.

## Licencia

Distribuido bajo la licencia MIT. Puedes usar, modificar y compartir la plantilla libremente. Consulta [`LICENSE`](LICENSE).
