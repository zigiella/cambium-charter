# Contribuir a Cambium Charter

Cambium Charter es un **documento vivo**: mejora con el uso real, no con opiniones.

## Cómo proponer cambios
- Abre un **issue** con el **caso real** (qué falló, qué aprendiste). La evidencia manda, como en el método.
- O un **PR** contra `main`. La puerta: que sea coherente con los seis invariantes; si tocas la doctrina, justifícalo con un caso, no con una opinión.
- Un cambio de método relevante va con un **ADR** (usa `plantillas/ADR.md`); los ADR del propio kit viven en `adr/` (el primero: `adr/0001-rigor-proporcional-en-la-puerta.md`).

## Versionado
- SemVer. Doctrina nueva → *minor*; correcciones y plantillas → *patch*. Todo queda en `CHANGELOG.md`.
- La carta **no** lleva su número dentro: el sello vive en `.cambium/VERSION` (y el historial en `CHANGELOG.md`).
- **Sellar** una versión = mergear su PR **+ crear el tag** `vX.Y`. Los proyectos re-vendorizan desde ese tag (§IX); sin tag, el «re-vendoriza desde el tag nuevo» no resuelve.

## Mantenimiento
- Los **cuatro adaptadores** (`adapters/CLAUDE.md` · `AGENTS.md` · `GEMINI.md` · `.cursorrules`) tienen **cuerpo idéntico** por diseño: al tocar la doctrina del adaptador, edítalos los cuatro a la vez (solo difiere la línea-comentario de qué herramienta lo lee).
- `CHARTER.md` es la fuente; `README.md` y su sección EN son **espejo derivado**: si cambias la carta, sincroniza el README.

## Alcance: disciplina obligatoria, tooling opcional
- Cambium es un método. Un CLI o un check es legítimo si (1) su ausencia no rompe nada (el flujo manual existe y está documentado), (2) **verifica y asiste, no aprueba** y (3) no introduce estado fuera del repo. Vive como paquete separado; la documentación del método nunca asume que existe.
- Un check de CI en modo *required* que bloquea el merge está decidiendo de facto: si se usa, debe existir un override humano documentado. Queda vetado cualquier software que ejecute el merge, apruebe traspasos o dirija a los agentes sin la humana.

## Filtro no-dev (salvaguarda anti-deriva)
- La carta y el kit se escriben primero para quien no programa; la superficie dev es añadido opcional, nunca requisito.
- Todo cambio del método registra si pasa el filtro: **¿sigue siendo usable por alguien en solitario sin instalar nada?** Si no lo pasa, va al paquete opcional, no al núcleo. (Columna prevista en `plantillas/registro-decisiones.md`.)

## Estilo
- Todo texto del kit sigue `plantillas/reglas-escritura.md` (precisión, densidad, autoridad nombrada; sin guiones largos, sin contrastes retóricos, sin enemigos inventados). Aplícalas también al proponer cambios.

## Tono
Sobrio, honesto, con cicatrices reales. Sin humo. El "no" es una contribución válida.

## Linaje
Desciende del oficio **Cambium**. Si lo heredas en tu equipo, sella la versión que usas.
