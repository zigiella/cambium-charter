# ADR 0003 · Portada + poda editorial + dial con suelo de irreversibilidad (v0.6)

**Estado:** propuesto (rama `v0.6-portada-poda`); pendiente de mordida del adversario y ratificación de la dirección.
**Origen:** paquete "Charter v2" de Beatriz (dirección) + Ria (redacción), revisado por Cambium contra el repo v0.5 y contra la operación real del proyecto Savia (`revision-de-cambium.md` en el paquete). El caso manda sobre la opinión.

## Decisiones

1. **Portada, no reemplazo.** El manifiesto de una página entra como `MANIFIESTO.md` (puerta de entrada, prioridad no-dev); `CHARTER.md` sigue siendo la doctrina y la fuente. Publicar el manifiesto como "la Charter" habría amputado lo probado en uso (génesis, bucle, antipatrones, custodia, relevo, adopción). El versionado conserva el linaje: esto es v0.6, no "v2".

2. **Poda editorial de la carta.** La carta baja a esqueleto: sin nombres de equipos ni anécdotas (viven en `EJEMPLOS.md`), justificación extensa en `adr/`, procedimiento fino en `plantillas/`. Se aplican las reglas de escritura de la dirección (`plantillas/reglas-escritura.md`): sin guiones largos, sin contrastes retóricos, verbos con responsabilidad. Reducción aproximada: 36 KB → 19 KB sin pérdida de principios.

3. **Invariantes con nombre corto y tres pares** (presentación; los textos no cambian de significado): Mando humano · Un solo timón · El repo es la verdad · Autoría real · Jurisdicción acotada · Honestidad sin fachada. Pares: quién manda, qué es verdad, cómo se convive.

4. **Dial de autonomía: posturas de presencia + suelo de irreversibilidad.** El dial existente gana dos precisiones. (a) La presencia de la humana sobre la integración es una postura explícita del dial: por turno, por lote, por hito o **por juicio delegado** ("mergea cuando lo veas claro"), registrada y revocable. Caso real: la dirección de Savia operó 12 días en por-merge estricto y delegó por juicio el 2026-06-30; la carta debe describir esa práctica, no prohibirla. (b) **El suelo no baja con la madurez de la spec:** lo irreversible hacia fuera, la doctrina y el redibujo del equipo se escalan siempre. Caso real: la frontera de agua de Savia, con spec madura, exigió ratificación humana y auditoría antes de la primera gota; el auditor emitió un "sin vale" que bloqueó correctamente. La madurez reduce decisiones abiertas; no reduce el riesgo de lo irreversible.

5. **Recibo como pieza del kit** (`plantillas/recibo.md`) y línea en la puerta: evidencia anclada (comando + salida), pendientes declarados; para quien usa PRs, el cuerpo del PR es el recibo. Converge con la issue #7 (recibo de verificación): doble descubrimiento independiente (ledger de Savia + paquete de Ria).

6. **Kit no-dev:** `glosario.md` (con "latido" alineado con §IV), `mapa-jurisdicciones.md`, `registro-decisiones.md`, `arranque-solo.md` (modo humana + una agente; el contrapeso del Art. 5 como pieza crítica).

7. **Gobierno:** `CONTRIBUTING.md` incorpora el alcance "disciplina obligatoria, tooling opcional" (software que verifica sí; software que decide, no; un check *required* exige override humano documentado) y el filtro no-dev como criterio de aceptación registrable.

## Rechazado o aplazado

- **"El merge lo valida siempre el humano" como absoluto** (texto v2): contradice el Art. 5 y la práctica real de la propia dirección. Sustituido por posturas del dial + suelo.
- **"Dial de control" como concepto nuevo:** colisionaba con el Dial de autonomía; se integra en el dial existente.
- **Redefinición de "latido"** del glosario v2 ("cada pequeño avance"): rompía el vocabulario de §IV; corregida.
- **Federación de coordinadores (E02·Op4):** fuera del núcleo mientras el invariante 2 diga "exactamente una"; la propia verificación del paquete lo marcó bloqueante.
- **`AGENTS.md` en dos capas (E07):** aplazado a un cambio de adaptadores coherente (los cuatro comparten cuerpo por diseño).

## Consecuencias

- Los equipos en v0.5 adoptan v0.6 con el ritual de §IX; ningún procedimiento del bucle cambia. La ganancia esperada: reconstrucciones más baratas (carta a la mitad), la letra alcanza a la práctica del merge, recibos que aceleran la revisión, y una puerta de entrada para no-dev y para el modo a solas.
- El manifiesto y el README quedan como espejos derivados de la carta (§VI): si divergen, manda la carta.
