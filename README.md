# Cambium Charter

**An open charter for human-led multi-agent work.**
**Una carta abierta para dirigir agentes de IA sobre un repositorio compartido.**

> *Cambium*: la capa viva del árbol, bajo la corteza, que genera todo el crecimiento.
> Esta carta es esa capa para un equipo de humano + agentes.

---

## Empieza rápido (5 minutos)

Lo primero de un proyecto Cambium no es el repo ni el código: **es crear a tu coordinadora.** Ella monta el resto.

1. **Abre una conversación con tu agente de confianza** (Claude, Codex, Gemini, Cursor…). Será tu **coordinadora**: diseña, revisa, integra y ejecuta el merge. Tú diriges.
2. **Pégale el arranque** ([`plantillas/arranque-coordinadora.md`](plantillas/arranque-coordinadora.md)). En corto:
   > *«Desde ahora eres la coordinadora de `<MI PROYECTO>` bajo el método **Cambium Charter**. Adopta el método leyendo github.com/zigiella/cambium-charter (empieza por `CHARTER.md`). Yo dirijo, tú coordinas. Cuando lo tengas, te paso la idea.»*
3. **Pásale tu idea** (no hace falta spec cerrada; afinarla es trabajo suyo). Ella crea el repo contigo, instala el método en `.cambium/` y te propone el equipo mínimo. **Nada se levanta hasta que tú ratificas.** A partir de ahí diriges por latidos: el repo es la verdad, el PR es la entrega.

**¿No programas?** Empieza por el [`MANIFIESTO.md`](MANIFIESTO.md) (el método en una página) y el [glosario en cristiano](plantillas/glosario.md).
**¿Trabajas con una sola agente?** [`plantillas/arranque-solo.md`](plantillas/arranque-solo.md): el método completo a escala mínima.

---

## Qué es · What it is

**ES** · **Cambium Charter es el "manual de oficio" que le das a uno de tus agentes de IA para que coordine a los demás sobre tu repositorio, contigo dirigiendo.** Fija lo mínimo que sostiene el orden con varios agentes a la vez: dónde está la verdad (el repo), quién manda en qué (jurisdicciones), cómo se entrega (el PR) y cómo se dice "no sé" (honestidad). No es un framework que instalas: es el **oficio**, escrito y listo para que tu agente lo adopte.

**EN** · **Cambium Charter is the "craft manual" you hand to one of your AI agents so it coordinates the others over your repository, with you directing.** It fixes the minimum that holds order with several agents at once: where truth lives (the repo), who owns what (jurisdictions), how work ships (the PR) and how to say "I don't know" (honesty). Not a framework you install: it's the **craft**, written down and ready for your agent to adopt.

## Por qué

Los agentes olvidan, se pisan, derivan y a veces inventan. Sin disciplina compartida, varios agentes degeneran en caos o en un humano haciendo de cable a jornada completa. Esta carta fija lo mínimo que sostiene el orden.

## Cómo queda el proyecto (estructura)

En el proyecto que adopta el método, la **raíz queda limpia**:

- **Raíz:** solo el/los **adaptadores** de tu herramienta (`CLAUDE.md`, `AGENTS.md`…). La herramienta los lee ahí.
- **`.cambium/`:** el método vendorizado: `CHARTER.md`, tu `REGLAS.md` y un `VERSION` con el sello **y la procedencia** (`upstream: github.com/zigiella/cambium-charter`), para que actualizar con §IX resuelva la fuente solo. Opcional: `memoria/`.
- **`docs/equipo/`:** un `role.md` por agente. **`bitacora/`:** `next.md` + las bitácoras.
- El `README.md` del proyecto es **del proyecto**; no lo pises con el del kit.

Nunca escribas rutas locales (`C:\…`) ni secretos en ficheros versionados.

## Las tres configuraciones de equipo

La coordinadora propone (y tú ratificas) cómo se compone el equipo. **El método no cambia entre ellas; cambia el cableado de arranque y de relevo.** La autoridad de merge sigue siendo exactamente una.

### (a) Propio · todas subagentes suyas
La coordinadora instancia y dirige a todo el equipo como subagentes, cada una aislada en su *worktree*, entregando por PR. Sin cable humano.
*Cuándo:* lo más simple y autónomo; frentes en paralelo deprisa.
*Límite:* comparten herramienta con la coordinadora; frágiles para esperas largas (el trabajo sobrevive en su PR).

### (b) Manual · agentes a mano, multi-tecnología
Agentes que configuras tú, cada uno en su herramienta, con su contexto y sus turnos. La coordinadora los levanta con un **prompt iniciático** ([`plantillas/arranque-agente.md`](plantillas/arranque-agente.md)) que siempre incluye "clona el repo".
*Cuándo:* mezclar tecnologías, o agentes robustos para turnos largos.
*Coste:* más cable humano (pegar prompts, pasar latidos).

### (c) Híbrido · lo mejor de ambas
Subagentes y agentes manuales conviviendo; anidable. Cada rama del árbol corre con su cadencia.
*Cuándo:* equipos que crecen.

### De un vistazo

| | **(a) Propio** · subagentes | **(b) Manual** · multi-tec | **(c) Híbrido** |
|---|---|---|---|
| **Quién instancia** | la coordinadora | tú pegas el prompt iniciático | mezcla: ella + tú |
| **Prompt + "clona el repo"** | no aplica | obligatorio por agente | solo las manuales |
| **Topología** | subagentes (worktrees) | clientes separados | ambas, anidables |
| **Cadencia / latido** | la coordinadora despierta a los suyos | latido humano o programado | cada rama, la suya |
| **Relevo (§VIII)** | reconstrucción desde el repo | cada agente, desde el repo | igual, por subárbol |

## Qué hay dentro

    MANIFIESTO.md   la portada: el método en una página (empieza aquí si no programas)
    CHARTER.md      la carta (la doctrina completa)
    adapters/       shims por herramienta (CLAUDE, AGENTS, GEMINI, .cursorrules; cuerpo idéntico)
    plantillas/     arranque-coordinadora · arranque-agente · arranque-solo · role · REGLAS ·
                    brief · next (cola) · bitácora · ADR · PR-checklist · recibo · glosario ·
                    mapa-jurisdicciones · registro-decisiones · reglas-escritura ·
                    traspaso-coordinacion · memoria-coordinadora · actualizacion-charter
    EJEMPLOS.md     equipos reales como prueba viva (incluye el modo "a solas")
    adr/            decisiones de diseño del método

## Cómo se actualiza

Copia versionada, no dependencia viva: re-vendoriza desde el tag nuevo y lee el `CHANGELOG`. Funciona offline. Cuando un equipo adopta una versión nueva, la coordinadora corre el ritual de **§IX**. Plantilla: [`plantillas/actualizacion-charter.md`](plantillas/actualizacion-charter.md).

## Cambium Charter (EN, essentials)

An open, portable method for one human to direct several AI agents building real software over a shared repo, with traceability and honesty.

**Six invariants**
1. **Human command.** Human direction decides what and why, holds the secrets, has the final vote.
2. **One helm.** One coordinator: architect, QA, sole merge authority, exactly one at any moment; she coordinates and codes only the minimum.
3. **The repo is the truth.** If chat and repo diverge, the repo wins.
4. **Real authorship.** Every commit says who made it.
5. **Bounded jurisdiction.** One front, one owner; outside it, hand off, don't edit.
6. **Honesty over polish.** The "no" and the loud failure beat false polish.

**Five articles of doctrine**
1. The repo is the clock: truth, total order, attribution. Shared memory is an inbox, never the authority.
2. The PR is the universal interface: any tool plugs in by producing a PR; a merged PR is the done signal.
3. The gate is discipline: only the coordinator merges, never red. Ratified team PRs merge by discipline; outside contributions also await human ratification.
4. Shared memory is optional and subordinate.
5. Separate auditor from gatekeeper; rigor proportional to risk. Verification cadence: periodic, by-risk (required before anything public or irreversible) and cross-checked. The auditor verifies and does not merge. The human sets her merge presence on the autonomy dial, from per-merge ratification to delegated judgment; the floor never drops: the irreversible always escalates to the human.

## Linaje · licencia · versión

Desciende del oficio **Cambium**. Textos bajo **CC-BY-4.0**; código y plantillas bajo **MIT** (ver `LICENSE`). Versión sellada en `.cambium/VERSION` (**v0.6**).
