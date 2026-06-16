# Contribuir a Cambium Charter

Cambium Charter es un **documento vivo**: mejora con el uso real, no con opiniones.

## Cómo proponer cambios
- Abre un **issue** con el **caso real** (qué falló, qué aprendiste). La evidencia manda, como en el método.
- O un **PR** contra `main`. La puerta: que sea coherente con los seis invariantes; si tocas la doctrina, justifícalo con un caso, no con una opinión.
- Un cambio de método relevante va con un **ADR** (usa `plantillas/ADR.md`).

## Versionado
- SemVer. Doctrina nueva → *minor*; correcciones y plantillas → *patch*. Todo queda en `CHANGELOG.md`.
- La carta **no** lleva su número dentro: el sello vive en `.cambium/VERSION` (y el historial en `CHANGELOG.md`).

## Mantenimiento
- Los **tres adaptadores** (`adapters/CLAUDE.md` · `AGENTS.md` · `GEMINI.md`) tienen **cuerpo idéntico** por diseño: al tocar la doctrina del adaptador, edítalos los tres a la vez (solo difiere la línea-comentario de qué herramienta lo lee).
- `CHARTER.md` es la fuente; `README.md` y su sección EN son **espejo derivado**: si cambias la carta, sincroniza el README.

## Tono
Sobrio, honesto, con cicatrices reales. Sin humo. El "no" es una contribución válida.

## Linaje
Desciende del oficio **Cambium**. Si lo heredas en tu equipo, sella la versión que usas.
