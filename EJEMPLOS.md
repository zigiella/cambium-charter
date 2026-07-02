# Cambium Charter — Ejemplos

*Prueba viva: tres equipos, tres dominios, el mismo esqueleto. Anonimizados a propósito; lo que importa es el patrón, no el proyecto.*

La carta no es teoría: sale de **tres equipos reales** que la encarnaron en dominios muy distintos. El dato más fuerte — **uno ni siquiera conocía la carta y convergió en lo mismo**, partiendo solo del estilo de su dirección humana. Eso sugiere que el núcleo es portable.

## Equipo A — producto en dominio regulado

- **Qué construye:** una herramienta que cita **fuentes oficiales verificables**; exige trazabilidad y anonimato.
- **Forma:** varias agentes en **clientes separados** (multi-herramienta), coordinadas por **cable humano**; la verdad en el repo, las decisiones en ADRs.
- **Cómo encarna la carta:** atribución con *trailer* de co-autor; puerta por disciplina (repo privado); la regla dura del dominio ("si la fuente falla, no inventes") vive en el **código**, no solo en la doctrina.
- **Cicatriz:** el cable humano es robusto (las agentes no mueren si la coordinadora se inactiva) pero es el cuello de botella → motiva la **bandeja en el repo** (`next.md`).

## Equipo B — datos abiertos, público

- **Qué construye:** un observatorio de datos territoriales; confianza pública = trazabilidad de cada número.
- **Forma:** todas en **una herramienta y una máquina**, lanzadas como **subagentes en worktrees** de la coordinadora (auto-coordinadas, sin cable).
- **Cómo encarna la carta:** atribución **sin trailer** (el personaje-agente *es* el autor de registro); repo **público** → la puerta *podría* endurecerse con reglas; un choque entre dos jurisdicciones se detectó por **CI en rojo** y se resolvió con un **PR coordinado en la misma rama**, cada commit firmado por su autora.
- **Cicatriz:** **dos agentes murieron de noche** por inactividad, sin avisar → pasó a **primer plano y serie** en el camino crítico, y aprendió que **la señal de fin fiable es el PR**. Además, un *guard* de hora + un cron retrasado le comieron un digest en silencio → **probar el camino de producción**.

## Equipo C — competición, con métrica y coste

- **Qué construye:** una entrega para un **benchmark con deadline, métrica objetiva y coste por cada medición**.
- **Forma:** **multi-herramienta de verdad** (tres proveedores distintos), por **turnos**, con **una sola escritora** (solo la coordinadora commitea; las demás *alimentan* datos).
- **Cómo encarna la carta:** **jurisdicción funcional** (diseñar / medir / romper), no por carpetas; una **memoria compartida vía MCP** (tipo Engram) como bandeja, pero con el **repo como reloj**; y —único de los tres— un **adversario independiente** activo que **acertó las tres veces** que avisó de un fallo.
- **Cicatriz:** la memoria compartida **no modela autoría** → tuvieron que *hackear* "de quién es el turno" en texto, y un turno **mutable** hizo que se escribiera sobre el id viejo → la corrección: **el repo es el reloj, la memoria es bandeja**. El adversario se sostiene solo porque **hay métrica objetiva y el error cuesta dinero** — y precisamente por ese coste **no auditaba cada acción**: entraba por **hito y antes de cada medición cara o irreversible** (por-riesgo), no en cada paso. Auditar todo habría quemado presupuesto sin pagarse.

## La foto, en una tabla

| | A · regulado | B · datos/público | C · competición |
|---|---|---|---|
| Topología | clientes separados | subagentes (worktrees) | turnos, multi-proveedor |
| Escritura | varias + merge | varias + merge | single-writer |
| Jurisdicción | por carpetas | por carpetas | funcional |
| Atribución | trailer co-autor | sin trailer (agente=autor) | un autor en git |
| Memoria | repo + bitácora + ADRs | repo + bitácora | repo + bandeja compartida |
| Auditor independiente | no | no (juez y parte) | sí (3/3) |
| Cable lateral | humano | coordinadora + contratos | bandeja + repo-reloj |

## Cambium a solas (humana + una agente)

El método funciona a escala uno; el detalle operativo y el prompt viven en `plantillas/arranque-solo.md`. Lo esencial: la agente única es la coordinadora (invariante 2, trivial); la jurisdicción degenera al reparto humana↔agente; duermen el relevo, el cross-audit y los latidos múltiples. **La pieza crítica es el contrapeso del Art. 5:** con una sola agente que construye e integra, el adversario antes de lo irreversible es la humana o una copia fresca sin contexto. El resto (repo-verdad, cola, PR, recibo, dial con suelo) opera idéntico. Crecer a equipo no exige re-aprender: la agente ya es la coordinadora.

## Encarnación dev de los invariantes

Para quien viene del oficio técnico, tres invariantes tienen implementación estándar: **Un solo timón** (2) → release manager, merge queue; **Autoría real** (4) → commit trailers (`Co-Authored-By`), `git blame`; **Jurisdicción acotada** (5) → `CODEOWNERS`. El kit define el contenido, no el formato: la tabla Markdown y el fichero ejecutable son encarnaciones de la misma regla.

## Qué demuestran juntos

- **El núcleo aguanta en tres dominios opuestos:** dirección humana + una coordinadora con la llave + repo-verdad + atribución + jurisdicción + honestidad.
- **Cuatro muros comunes**, en equipos que no se hablaban: puerta blanda · auditor juez-y-parte (solo el de competición lo resolvió) · fragilidad en segundo plano · memoria compartida sin autoría.
- **Mismo esqueleto, cuerpos distintos:** las diferencias son **adaptación sana**, no incoherencia.
- **No hace falta el documento para llegar aquí:** un equipo lo re-derivó solo. La carta no inventa el método; lo **escribe para que se herede sin re-derivarlo**.
