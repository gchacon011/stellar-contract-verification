# Historias de usuario individuales

**Nombre:** Angel Serrano
**Usuario de GitHub:** angeldavid218
**Producto:** CSV Verify — Contract Source Verify
**Fecha:** 4 de octubre de 2026

> Propuesta individual preparada a partir del proyecto. Angel debe revisarla y hacerla propia; este archivo no atribuye contribuciones a otros integrantes.

## Mis historias de usuario

1. **HU-01.** Como usuario de una aplicación en Stellar quiero verificar el código de un contrato mediante su Contract ID para saber si el código publicado corresponde al WASM desplegado antes de interactuar con él.

2. **HU-02.** Como desarrollador Soroban quiero conocer los metadatos y las condiciones de compilación requeridas para publicar un contrato cuya fuente pueda reproducirse por un tercero.

3. **HU-03.** Como auditor técnico quiero consultar la fuente, su revisión, el entorno de compilación y ambos hashes para evaluar la evidencia de una verificación de manera independiente.

4. **HU-04.** Como usuario que consulta un contrato quiero distinguir entre fuente verificada, hashes diferentes y verificación inconclusa para interpretar correctamente el resultado y decidir mi siguiente paso.

5. **HU-05.** Como integrador de una wallet o explorador quiero consultar una verificación vinculada a la red y al hash actual del contrato para mostrar evidencia pertinente sin reutilizar resultados de una versión anterior.

6. **HU-06.** Como desarrollador que recibe un resultado inconcluso quiero identificar la causa y los pasos para corregirla para poder preparar una compilación reproducible y volver a verificar.

7. **HU-07.** Como usuario hispanohablante quiero leer el flujo y sus resultados en español para comprender el alcance de la verificación sin barreras de idioma.

## La más importante y por qué

La historia HU-01 es la más importante porque expresa el resultado que justifica el producto: comprobar si el contrato que una persona considera usar corresponde a la fuente publicada. Todas las demás habilitan, explican o facilitan ese resultado. La verificación de fuente no demuestra que el contrato sea seguro.

| Orden de importancia | Historia # | Por qué |
| :---: | :---: | --- |
| 1 | #1 / HU-01 | Es la promesa central: aporta evidencia de correspondencia entre fuente y despliegue. |
| 2 | #4 / HU-04 | Impide presentar errores de compilación o falta de metadatos como prueba de código diferente. |
| 3 | #2 / HU-02 | Habilita la verificación: sin fuente identificable y entorno reproducible no hay comparación concluyente. |
| 4 | #3 / HU-03 | Hace explicable y revisable el resultado; evita depender únicamente de una insignia. |
| 5 | #5 / HU-05 | Preserva la validez del resultado cuando una misma instancia cambia de código. |
| 6 | #6 / HU-06 | Reduce la fricción de adopción y convierte los fallos en acciones concretas. |
| 7 | #7 / HU-07 | Facilita el acceso del público inicial; se apoya en la traducción ya existente. |

**Criterio:** primero la evidencia central y su interpretación correcta; después reproducibilidad, trazabilidad, vigencia, recuperación y accesibilidad.
