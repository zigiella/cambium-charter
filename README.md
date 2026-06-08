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

1. **Use this template** (o copia `adapters/` + `plantillas/`).
2. Rellena los **huecos**: `REGLAS.md` (tus innegociables), un `role.md` por agente, el mapa de jurisdicciones.
3. Pon los **adaptadores** en la raíz (`CLAUDE.md`, `AGENTS.md`…): ya apuntan a `CHARTER.md`.
4. Sella el linaje: en tu adaptador, *"Método: Cambium Charter v0.2"*.

## Cómo se actualiza

Copia versionada, no dependencia viva: re-vendoriza desde el tag nuevo y lee el `CHANGELOG`. Funciona offline.

## Qué hay dentro

    CHARTER.md      la carta (la doctrina)
    adapters/       shims por herramienta (CLAUDE, AGENTS, GEMINI, .cursorrules)
    plantillas/     role · REGLAS · ADR · bitácora · brief · next · PR-checklist
    EJEMPLOS.md     tres equipos reales como prueba viva

## Cambium Charter (EN, essentials)

An open, portable method for one human to direct several AI agents building real software over a shared repo — with traceability and honesty.

**Six invariants**
1. Human direction decides what & why, holds the secrets, has the final vote.
2. One coordinator: architect, QA, sole merge authority.
3. The repo is the truth; if chat and repo diverge, the repo wins.
4. Real authorship: every commit says who made it.
5. Bounded jurisdiction: one front, one owner; outside it, hand off — don't edit.
6. Honesty as a feature: the "no" and the loud failure over false polish.

**Five articles of doctrine**
1. The repo is the clock — truth, total order, attribution. Shared memory is an inbox, never the authority.
2. The PR is the universal interface — any tool plugs in by producing a PR; "there's a PR" is the done signal.
3. The gate is discipline — only the coordinator merges, never red; harden with rules if the repo allows.
4. Shared memory is optional and subordinate — principles over repo+PR; the tool only as a side inbox.
5. Separate auditor from gatekeeper before production — whoever merges can't be the only auditor forever.

## Linaje · licencia · versión

Desciende del oficio **Cambium**. Textos bajo **CC-BY-4.0**; código y plantillas bajo **MIT** (ver `LICENSE`). Versión **v0.2**.
