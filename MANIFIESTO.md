# 🌳 Cambium Charter

> **Capa de reglas entre intención y código.**

*El cámbium es la capa viva del árbol, entre la corteza y la madera, donde se organiza el crecimiento. En Cambium, esa capa entre tu intención y el código es un conjunto de reglas en las que tú mandas.*

---

## Qué es

Cambium es una **disciplina** (no un software) para construir con varios agentes de IA, de cualquier tecnología, sobre un mismo repositorio, **sin perder el control**. Pone tu criterio en el centro y lo hace verificable.

## Para quién

Para quien dirige la construcción de un producto con agentes y quiere **entender y aprobar** lo que se construye, sepa programar o no. La versión para no programadores es el piso del método, no una simplificación.

## Cómo opera (en una frase)

Tú diriges. Una **única coordinadora** (un agente) orquesta a las demás, cada una en su **jurisdicción**, y todo el trabajo aterriza en el **repositorio** como única verdad. Es agnóstico de herramienta (Claude, Codex, Gemini, Cursor…).

---

## Los 6 invariantes

*Las reglas que no se rompen. Seis para trabajar; tres pares para recordar.*

**Quién manda**
1. **Mando humano.** Las decisiones y los secretos son tuyos; el voto final es tuyo.
2. **Un solo timón.** Una única coordinadora integra el trabajo y ejecuta cada merge, exactamente una en todo momento.

**Qué es verdad**
3. **El repo es la verdad.** Lo que no está en el repositorio no existe.
4. **Autoría real.** Cada cambio registra quién lo hizo, humano o agente.

**Cómo se convive**
5. **Jurisdicción acotada.** Cada agente tiene su territorio; nadie pisa el de otra.
6. **Honestidad sin fachada.** Se reporta lo que pasó de verdad, fallos y dudas incluidos.

---

## El dial de autonomía

*Tu presencia en las decisiones depende de cuán madura está la especificación. Cuanto mejor especificas, más delegas.*

| Madurez de la spec | Modo | Tu presencia |
|---|---|---|
| **Idea poco definida** | **Co-diseño** | En cada decisión: la spec se descubre construyendo |
| **Idea definida, spec amateur** | **Dirección por fases** | Apruebas en puertas (al cerrar cada fase o jurisdicción) |
| **Bien especificada** | **Dirección por objetivos** | Fijas reglas y objetivos; revisas resultados y evidencias |

**Dos reglas cruzan los tres modos:**

- **El suelo no baja.** Lo **irreversible hacia fuera** (publicar, enviar un correo, mover agua, gastar) pasa por ti siempre, por madura que esté la spec. La madurez reduce decisiones abiertas; no reduce el riesgo de lo irreversible.
- **Tu presencia sobre el merge es tuya y explícita.** Puedes ratificar cada merge al empezar y, cuando la confianza se gana, delegar el merge rutinario en el juicio de la coordinadora ("mergea cuando lo veas claro"). Toda delegación queda registrada y se revoca con una frase.

**Regla de oro:** sube el control en cuanto algo huela mal. Siempre puede volver a subir.

---

## Instrucciones para los agentes

*(Esta sección puede vivir tal cual como `AGENTS.md` en la raíz del repo.)*

- Operas bajo la **Cambium Charter**. La autoridad final es humana.
- **El merge pertenece a la única coordinadora**, bajo la presencia que la dirección haya fijado (por-merge o por juicio delegado). **Lo irreversible hacia fuera se escala a la humana siempre.**
- **Quédate en tu jurisdicción.** Si necesitas tocar otra, pídelo antes.
- Cada entrega deja **evidencia** (recibo): qué hiciste, cómo se verifica y qué queda pendiente. Reporta fallos y dudas.
- **Firma tu autoría real** en cada cambio.
- **Los secretos no entran en el repo.**

---

*Cambium Charter · portada del método. La doctrina completa vive en `CHARTER.md`; si divergen, manda la carta.*
