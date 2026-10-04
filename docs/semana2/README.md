# Semana 2 · Product Blueprint de CSV Verify

**Fecha:** 4 de octubre de 2026.  
**Estado:** documentación preparada; entrega académica pendiente de cierre de las dependencias siguientes.

## Documentos

- [Product Blueprint](ProductBlueprint.md): las ocho secciones en el orden solicitado.
- [Historias individuales de Angel Serrano](AngelSerrano.md): siete historias y prioridad razonada.
- [Lean Canvas](LeanCanvas.md): lienzo de una página en Markdown, enlazado desde el blueprint.

La copia en el main vault es para consulta. Los archivos de entrega viven en `docs/semana2/` del repositorio; el backlog operativo debe estar en GitHub Projects.

## Pendientes que condicionan la entrega

- Repositorio de entrega confirmado: [gchacon011/stellar-contract-verification](https://github.com/gchacon011/stellar-contract-verification); integrar allí la rama de documentación mediante revisión.
- Aportar `docs/semana1/ProblemBrief.md` y contrastar usuario, problema y criterio de pertinencia. No se inventó un Problem Brief retroactivo.
- Cada integrante debe aportar entre cinco y siete historias en su propio archivo y realizar su propio commit. Sólo se preparó el archivo de Angel, cuya identidad consta en la configuración Git local.
- El equipo debe validar la priorización colectiva.
- El [Kanban de semana 2](https://github.com/users/angeldavid218/projects/2/views/1) ya está creado con siete historias. Es público y está vinculado al fork local; el enlace es accesible desde el blueprint; el equipo puede vincularlo también a `gchacon011/stellar-contract-verification`.
- Los commits están publicados en [docs/product-blueprint-semana2](https://github.com/angeldavid218/stellar-contract-verification/tree/docs/product-blueprint-semana2/docs/semana2). Falta integrar la documentación en la rama de entrega del equipo mediante revisión.
- Cargar el repositorio en Apex según el plazo indicado por la convocatoria: domingo 4 de octubre, 5:00 p.m., hora México. Verificar la zona horaria que utiliza la plataforma; no se convierte automáticamente a la zona del dispositivo.

## Evidencia y límites de la revisión

| Fuente revisada | Qué sostiene |
| --- | --- |
| `README.md` local | Nombre, finalidad, flujo, stack, tutorial y repositorio padre. |
| `src/hooks/useVerifyFlow.ts` y `src/lib/api.ts` | Consulta GET antes de POST; GET puede devolver un resultado persistido sin lectura actual del ledger. |
| `src/types/index.ts` y componentes de resultado | Esquema de evidencia, estados y niveles internos. Los niveles por sí solos no prueban una reconstrucción exitosa. |
| `src/hooks/useWallet.ts` | Freighter existe como integración de interfaz; la consulta no requiere firma. |
| [Backend: verify.rs](https://github.com/sebasberrios-dev/stellar-contract-verification/blob/demo-backend/backend/src/routes/verify.rs) y [lookup.rs](https://github.com/sebasberrios-dev/stellar-contract-verification/blob/demo-backend/backend/src/routes/lookup.rs) | POST lee el WASM antes de consultar caché; GET sólo consulta el store; Testnet es la red habilitada. |
| [Backend: rpc/client.rs](https://github.com/sebasberrios-dev/stellar-contract-verification/blob/demo-backend/backend/src/rpc/client.rs) | Dos lecturas `getLedgerEntries`: instancia y código. |
| [Backend: docker.rs](https://github.com/sebasberrios-dev/stellar-contract-verification/blob/demo-backend/backend/src/builder/docker.rs) | Imagen por defecto con tag `latest`, comprobación de imagen por substring y compilación con acceso a red. No se presenta como aislamiento endurecido ni entorno inmutable. |
| [SEP-58 vigente](https://github.com/stellar/stellar-protocol/blob/master/ecosystem/sep-0058.md) | Draft v0.6.0: diferencia entre vocabulario vigente y formato implementado. |
| [Plantilla oficial de semana 2](https://github.com/mestupinanm/ProyectoBase/tree/main/docs/semana2) | Estructura y orden de los documentos. |

La revisión leyó código y documentación; no ejecutó el frontend, el backend ni verificaciones on-chain. Los criterios del MVP son comprobaciones pendientes, no tests aprobados. La rama está publicada en GitHub. No se declara aprobación del equipo, integración en main ni envío a Apex.
