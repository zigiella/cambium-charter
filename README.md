# Cambium Charter

**An open charter for human-led multi-agent work.**
**Una carta abierta para dirigir agentes de IA sobre un repositorio compartido.**

> *Cambium*: la capa viva del árbol, bajo la corteza, que genera todo el crecimiento.
> Esta carta es esa capa para un equipo de humano + agentes.

---

## Qué es · What it is

**ES** — Método abierto, portable y versionado para que una dirección humana coordine varios agentes de IA (Claude, Codex, Gemini…) construyendo algo real sobre un mismo repositorio, con trazabilidad y honestidad. No es un framework ni una librería: es el **oficio**, escrito y listo para heredar.

**EN** — An open, portable, versioned method for one human to direct several AI agents building something real over a shared repo, with traceability and honesty. Not a framework or a library: it's the **craft**, written down and ready to inherit.

## Por qué

Los agentes olvidan, se pisan, derivan y a veces inventan. Sin disciplina compartida, 3-6 agentes degeneran en caos o en un humano haciendo de cable a jornada completa. Esta carta fija lo mínimo que sostiene el orden: dónde está la verdad, quién manda en qué, cómo se entrega y cómo se dice "no sé".

## Cómo se adopta

En el proyecto que adopta el método, mantén la **raíz limpia**:

- **Raíz:** solo el/los **adaptadores** de tu herramienta (`CLAUDE.md`, `AGENTS.md`…). La herramienta los lee ahí.
- **`.cambium/`:** el método vendorizado — `CHARTER.md`, tu `REGLAS.md` y un `VERSION` con el sello (p. ej. `Cambium Charter v0.3`). Opcional: `memoria/` si la coordinadora versiona su memoria.
- **`docs/equipo/`:** un `role.md` por agente. **`bitacora/`:** `next.md` + las bitácoras.
- El `README.md` del proyecto es **del proyecto**; no lo pises con el del kit.

Pasos: *Use this template* (o copia lo necesario) → rellena `REGLAS.md` y los roles → pon el adaptador en la raíz → crea `.cambium/VERSION`. Nunca escribas rutas locales (`C:\…`) en ficheros versionados.

## Cómo se actualiza

Copia versionada, no dependencia viva: re-vendoriza desde el tag nuevo y lee el `CHANGELOG`. Funciona offline. Cuando un equipo **adopta** una versión nueva, la coordinadora corre el ritual de **§IX** (re-vendorizar `.cambium/` + sellar `VERSION` → migrar `next.md`/`role.md`/plantillas sin perder la cola → encolar la auto-actualización en el `next.md` de cada agente → despertar a cada una según su tipo). Funciona en las tres configuraciones de equipo. Plantilla: `plantillas/actualizacion-charter.md`.

## Cómo nace un equipo · cómo se compone

**Génesis — la coordinadora nace primero:** lo primero del proyecto no es repo ni código, es **crear a la coordinadora** desde una spec/idea (o trabajándola). Ella asume su rol, ayuda a crear el repo online, instala el método y propone el equipo mínimo; la humana ratifica.

**Tres configuraciones de equipo** que la coordinadora debe saber manejar: **(a) propio** — todas subagentes suyas; **(b) manual** — agentes configurados a mano, posiblemente en tecnologías distintas (su prompt iniciático **siempre incluye "clona el repo"**); **(c) híbrido** — subagentes + agentes manuales (que pueden tener sus propios subagentes). El método no cambia entre las tres; cambia el cableado de arranque y de relevo.

## Qué hay dentro

    CHARTER.md      la carta (la doctrina)
    adapters/       shims por herramienta (CLAUDE, AGENTS, GEMINI, .cursorrules; cuerpo idéntico)
    plantillas/     arranque-coordinadora · arranque-agente · role · REGLAS · brief · next (cola) · bitácora · ADR · PR-checklist · traspaso-coordinacion · memoria-coordinadora · actualizacion-charter
    EJEMPLOS.md     tres equipos reales como prueba viva

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

Desciende del oficio **Cambium**. Textos bajo **CC-BY-4.0**; código y plantillas bajo **MIT** (ver `LICENSE`). Versión sellada en `.cambium/VERSION` (**v0.3**).
