# Cambium Charter

**An open charter for human-led multi-agent work.**
**Una carta abierta para dirigir agentes de IA sobre un repositorio compartido.**

> *Cambium*: la capa viva del árbol, bajo la corteza, que genera todo el crecimiento.
> Esta carta es esa capa para un equipo de humano + agentes.

---

## Qué es · What it is

**ES** — **Cambium Charter es el "manual de oficio" que le das a uno de tus agentes de IA para que coordine a los demás sobre tu repositorio — contigo dirigiendo.** Fija lo mínimo que sostiene el orden con 3-6 agentes a la vez: dónde está la verdad (el repo), quién manda en qué (jurisdicciones), cómo se entrega (el PR) y cómo se dice "no sé" (honestidad). No es un framework ni una librería que instalas: es el **oficio**, escrito y listo para que tu agente lo adopte.

**EN** — **Cambium Charter is the "craft manual" you hand to one of your AI agents so it coordinates the others over your repository — with you directing.** It fixes the minimum that holds order with 3-6 agents at once: where truth lives (the repo), who owns what (jurisdictions), how work ships (the PR) and how to say "I don't know" (honesty). Not a framework or a library you install: it's the **craft**, written down and ready for your agent to adopt.

## Por qué

Los agentes olvidan, se pisan, derivan y a veces inventan. Sin disciplina compartida, 3-6 agentes degeneran en caos o en un humano haciendo de cable a jornada completa. Esta carta fija lo mínimo que sostiene el orden: dónde está la verdad, quién manda en qué, cómo se entrega y cómo se dice "no sé".

## Cómo empezar (poner un proyecto en marcha)

Lo primero de un proyecto Cambium **no es el repo ni el código: es crear a tu coordinadora.** Ella monta el resto.

1. **Abre una conversación con tu agente de confianza** (Claude, Codex, Gemini, Cursor…). Va a ser tu **coordinadora**: diseña, revisa, integra y es la única que mergea. Tú diriges.
2. **Dile que trabajaréis con Cambium Charter y pégale el arranque.** El mensaje listo-para-pegar es [`plantillas/arranque-coordinadora.md`](plantillas/arranque-coordinadora.md). En corto:
   > *«Desde ahora eres la coordinadora de `<MI PROYECTO>` bajo el método **Cambium Charter**. Adopta el método leyendo github.com/zigiella/cambium-charter (empieza por `CHARTER.md`). Yo dirijo, tú coordinas. Cuando lo tengas, te paso la spec.»*
3. **Pásale la spec o la idea de tu proyecto** (no hace falta que esté cerrada — afinarla es trabajo suyo). Con eso, ella te ayuda a **crear el repo** (propone nombre/visibilidad; las credenciales las pones tú), **instala el método** en `.cambium/` y te **propone el equipo mínimo** (roles + una de las 3 configuraciones).
4. **Ratifica el equipo** (o ajústalo). **Nada se levanta hasta tu OK**: tú tienes el voto final y los secretos.
5. **A partir de ahí, diriges por latidos:** despiertas a cada agente con un *«mira tu `next.md`»*; el repo es la verdad, el PR es la entrega.

*(El detalle completo está en [`plantillas/arranque-coordinadora.md`](plantillas/arranque-coordinadora.md) y en §III del CHARTER.)*

## Cómo queda el proyecto (estructura)

En el proyecto que adopta el método, mantén la **raíz limpia**:

- **Raíz:** solo el/los **adaptadores** de tu herramienta (`CLAUDE.md`, `AGENTS.md`…). La herramienta los lee ahí.
- **`.cambium/`:** el método vendorizado — `CHARTER.md`, tu `REGLAS.md` y un `VERSION` con el sello **y la procedencia** (p. ej. `Cambium Charter v0.3.1` + `upstream: github.com/zigiella/cambium-charter`, para que actualizar con §IX resuelva la fuente solo). Opcional: `memoria/` si la coordinadora versiona su memoria.
- **`docs/equipo/`:** un `role.md` por agente. **`bitacora/`:** `next.md` + las bitácoras.
- El `README.md` del proyecto es **del proyecto**; no lo pises con el del kit.

Pasos: *Use this template* (o copia lo necesario) → rellena `REGLAS.md` y los roles → pon el adaptador en la raíz → crea `.cambium/VERSION` (sello + `upstream:`). Nunca escribas rutas locales (`C:\…`) en ficheros versionados.

## Las tres configuraciones de equipo

Una vez nace la coordinadora (ver *Cómo empezar*), propone —y tú ratificas— **cómo se compone el equipo**. Hay tres formas, y una buena coordinadora sabe manejar las tres. **El método no cambia entre ellas; solo cambia el cableado de arranque y de relevo** — y la autoridad de merge sigue siendo **exactamente una** (la coordinadora).

### (a) Propio · todas subagentes suyas
La coordinadora **instancia y dirige a todo el equipo como subagentes** suyos —cada uno aislado en su *worktree*, entregando por PR—. Sin cable humano ni prompts que pegar: una herramienta, una máquina, una sola mano que coordina.
*Cuándo:* lo más simple y autónomo; ideal para abrir frentes en paralelo deprisa.
*Límite:* comparten herramienta con la coordinadora y son frágiles para esperas largas (un subagente muere por inactividad, aunque su trabajo ya viva en su PR).

### (b) Manual · agentes a mano, multi-tecnología
Agentes que **configuras tú a mano**, cada uno en su propia herramienta (Claude, Codex, Gemini, Cursor…), con su contexto y sus turnos. La coordinadora no los instancia: los levanta con un **prompt iniciático** (`plantillas/arranque-agente.md`) que **siempre incluye "clona el repo"** —ese agente no comparte tu sistema de ficheros: sin el repo clonado, no existe para el método—.
*Cuándo:* quieres mezclar tecnologías, o agentes robustos para turnos largos.
*Coste:* más cable humano (pegar prompts, pasar latidos).

### (c) Híbrido · lo mejor de ambas
Subagentes **y** agentes manuales conviviendo; un agente manual puede tener, a su vez, **sus propios** subagentes (anidable). Cada rama del árbol corre con su cadencia.
*Cuándo:* equipos reales que crecen — un núcleo de subagentes rápidos + alguna pieza manual donde haga falta.

### De un vistazo

| | **(a) Propio** · subagentes | **(b) Manual** · multi-tec | **(c) Híbrido** |
|---|---|---|---|
| **Quién instancia** | la coordinadora | tú pegas el prompt iniciático | mezcla: ella + tú |
| **Prompt + "clona el repo"** | no aplica | obligatorio por agente | solo las manuales |
| **Topología** | subagentes (worktrees) | clientes separados | ambas, anidables |
| **Cadencia / latido** | la coordinadora despierta a los suyos | latido humano o programado | cada rama, la suya |
| **Relevo (§VIII)** | reconstrucción desde el repo | cada agente, desde el repo | igual, por subárbol |

## Qué hay dentro

    CHARTER.md      la carta (la doctrina)
    adapters/       shims por herramienta (CLAUDE, AGENTS, GEMINI, .cursorrules; cuerpo idéntico)
    plantillas/     arranque-coordinadora · arranque-agente · role · REGLAS · brief · next (cola) · bitácora · ADR · PR-checklist · traspaso-coordinacion · memoria-coordinadora · actualizacion-charter
    EJEMPLOS.md     tres equipos reales como prueba viva

## Cómo se actualiza

Copia versionada, no dependencia viva: re-vendoriza desde el tag nuevo y lee el `CHANGELOG`. Funciona offline. Cuando un equipo **adopta** una versión nueva, la coordinadora corre el ritual de **§IX** (re-vendorizar `.cambium/` + sellar `VERSION` → migrar `next.md`/`role.md`/plantillas sin perder la cola → encolar la auto-actualización en el `next.md` de cada agente → despertar a cada una según su tipo). Funciona en las tres configuraciones de equipo. Plantilla: `plantillas/actualizacion-charter.md`.

## Cambium Charter (EN, essentials)

An open, portable method for one human to direct several AI agents building real software over a shared repo — with traceability and honesty.

**Six invariants**
1. Human direction decides what & why, holds the secrets, has the final vote.
2. One coordinator: architect, QA, sole merge authority — exactly one at any moment; she coordinates and codes only the minimum.
3. The repo is the truth; if chat and repo diverge, the repo wins.
4. Real authorship: every commit says who made it.
5. Bounded jurisdiction: one front, one owner; outside it, hand off — don't edit.
6. Honesty as a feature: the "no" and the loud failure over false polish.

**Five articles of doctrine**
1. The repo is the clock — truth, total order, attribution. Shared memory is an inbox, never the authority.
2. The PR is the universal interface — any tool plugs in by producing a PR; "there's a PR" is the done signal.
3. The gate is discipline — only the coordinator merges, never red; harden with rules if the repo allows. A ratified team PR she merges by discipline; an outside contribution also waits for the human's ratification.
4. Shared memory is optional and subordinate — principles over repo+PR; the tool only as a side inbox.
5. Separate auditor from gatekeeper before production — whoever merges can't be the only auditor forever; independent verification costs tokens and time, so it is *not per-action* (auditing every action is an antipattern). Its cadence is threefold: periodic (by milestone), by-risk (required before any public or irreversible release), and cross-checked (peers occasionally audit each other's front, which the coordinator may suggest). The auditor verifies but does not merge.

## Linaje · licencia · versión

Desciende del oficio **Cambium**. Textos bajo **CC-BY-4.0**; código y plantillas bajo **MIT** (ver `LICENSE`). Versión sellada en `.cambium/VERSION` (**v0.3.1**).
