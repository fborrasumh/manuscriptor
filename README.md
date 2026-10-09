# Manuscriptor

Asistente de redacción de artículos científicos IMRaD, en un único fichero HTML. Versión 3 (rediseño de Manuscriptor v2).

**Usar la app:** https://fborrasumh.github.io/manuscriptor/

**Idiomas:** español (por defecto), inglés y portugués; selector en la barra superior o `?lang=en` / `?lang=pt` en la URL. El idioma del manuscrito es independiente del de la interfaz.

## Qué hace

- Recorrido en seis pasos: proyecto (pregunta, tipo de estudio, revista, estilo de citas), material (notas, documentos Word/PDF/PowerPoint/texto y tablas CSV/TSV/Excel), literatura, redacción, revisión y exportación.
- **Redacción por sección con tres modos a elegir:** borrador con IA, guía con preguntas (la IA no escribe) o texto propio. Secciones: Introducción, Métodos, Resultados, Discusión, Conclusiones, Resumen, Título y palabras clave.
- **Referencias reales:** búsqueda en PubMed, OpenAlex y Crossref, alta por DOI o a mano. La IA solo puede citar con marcadores `[R#]` de la lista elegida; el código marca las citas que no existen y comprueba en Crossref que cada DOI existe y que su título coincide.
- **Cifras comprobadas por código:** se registran las cifras de las notas, los documentos y las tablas (y se calculan medias, desviaciones, medianas, recuentos y porcentajes). Cada número de cada sección se contrasta con ese registro; los que no aparecen se marcan. La Tabla 1 descriptiva por grupos la calcula el código.
- **Comprobaciones:** límites de palabras de la revista, citas huérfanas, referencias sin citar, abreviaturas sin definir, resultados que interpretan, discusión sin limitaciones, coherencia entre resumen y resultados.
- **Revisión:** informe de revisor simulado cuyos puntos llevan un fragmento literal que el código verifica.
- **Exportación:** Word (líneas numeradas e interlineado doble opcionales), Markdown, LaTeX con BibTeX, texto, RIS, CSV de comprobaciones, ZIP y proyecto en JSON. Borrador de declaración de uso de IA basado en un registro de uso (sin contenido).

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador. No hace falta servidor. El ejemplo (datos ficticios) funciona sin clave.

## Privacidad

Notas, tablas y borradores se guardan solo en el navegador (IndexedDB). A la IA solo llega lo que la persona decide enviar, con correos, DNI y teléfonos enmascarados y tras ver una muestra; de las tablas de datos brutos solo sale un resumen estadístico. PubMed, OpenAlex y Crossref reciben únicamente las consultas y los DOI. No pegues datos identificables de pacientes o participantes.

## Límites

- No comprueba que una referencia respalde la frase donde se cita, ni que el análisis estadístico sea adecuado. No calcula valores de p ni intervalos: deben venir de las notas.
- No incluye listas de comprobación de guías de reporte (CONSORT, STROBE, PRISMA…).
- Los límites de cada revista son orientativos y no están verificados con sus instrucciones vigentes: confírmalos.
- OpenAlex no separa apellidos compuestos: revisa los nombres de autor.
- La IA puede equivocarse; la responsabilidad del manuscrito es de los autores. Consulta la política de IA de la revista.
- Probada con IA y fuentes bibliográficas simuladas; no con claves ni servicios reales.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) · ORCID [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573).

## Cómo citar

Borrás Rocher, F. (2026). *Manuscriptor* (v3.0.0) [Software]. https://doi.org/10.5281/zenodo.21423297 (DOI de concepto; cada versión tiene el suyo).

## Licencia

MIT. Véase [LICENSE](LICENSE).
