# Auditoría de factura de flete

Cruza la factura (CFDI) de tu transportista contra **tu tarifa pactada**, el embarque y las
evidencias del viaje (tickets de caseta, sellos de llegada, POD, báscula). Renglón por renglón te dice
qué está aprobado, qué se disputa con su evidencia, qué falta por comprobar, y te entrega la **carta
de disputa lista para mandar**. Nunca inventa una tarifa ni una evidencia: si falta el dato, lo pide.

Pre-revisa, cruza y arma evidencia. **No sustituye al contador, al agente aduanal ni al SAT:** no
valida el CFDI ante el SAT (eso lo hace tu contador o tu PAC) y deja el tratamiento fiscal (IVA
acreditable, deducibilidad) para tu contador.

## Uso en 3 pasos

1. **Pégale la factura del transportista** (XML o PDF) y la tarifa que pactaste con él (tabla o CSV
   del contrato, la hoja de tarifas o la carta de confirmación).
2. **Agrega el embarque y las evidencias**: orden de embarque o carta porte, POD firmado, tickets de
   caseta, sellos de llegada/salida y ticket de báscula. Todo se pega o adjunta en el chat.
3. **Copia la carta de disputa** que te devuelve (con la tabla de auditoría y el expediente de
   evidencia) y envíala. Lo que falte va en «Faltantes» con la pregunta exacta, nunca inventado.

Funciona sin terminal, sin scripts y sin API: se conecta con el conector de Agensi en claude.ai o
subiendo el ZIP de la skill, y trabaja en el chat pegando o adjuntando archivos.

## Qué recibes

- **Tabla de auditoría renglón por renglón**: qué cobró el transportista, qué dice tu tarifa, qué
  acredita el embarque y qué respalda la evidencia — con veredicto (Aprobado / Disputado /
  No comprobado / Falta dato) y código de discrepancia (D1–D8).
- **Los totales para decidir el pago**: aprobado, disputado y no comprobado, cada uno con y sin IVA
  tal como el CFDI lo declara, y el pago recomendado de esta factura.
- **El expediente de evidencia** de cada discrepancia: renglón facturado, cláusula de tarifa, dato
  del embarque, evidencia que manda e importe exacto en disputa.
- **La carta de disputa lista para copiar**: folio y UUID de la factura, las diferencias una por una
  con su evidencia, el total disputado y la petición concreta (nota de crédito o soporte faltante).
- **La advertencia de alcance**: qué valida tu contador o PAC y qué quedó fuera de esta auditoría.

## Prueba sin datos propios

La carpeta `ejemplos/caso-01-anden-norte/` trae un caso completo con datos ficticios de la empresa
«Andén Norte»: una tarifa pactada (MTY→GDL, flete con maniobras incluidas, casetas con tope contra
ticket, 24 h de estadía libres, 24 t incluidas), un embarque con sellos y un ticket de caseta, y la
factura F-7781 con cinco renglones. Síguelo a mano: la factura cuadra aritméticamente
($24,045.00 + IVA 16 % = $27,892.20), pero el cruce deja aprobados $19,680.00 de base, disputados
$4,080.00 (casetas duplicadas $1,180.00, estadía dentro de la ventana libre $1,700.00, maniobras ya
incluidas $1,200.00), y $285.00 sin comprobar (excedente de peso sin báscula y contra un embarque de
22 t). El pago recomendado es $22,828.80 y el total retenido con IVA es $5,063.40 — todo derivable a
mano desde `entrada.md`, y la salida esperada se reproduce bien al primer intento.

## Qué no hace

- No inventa ni interpola tarifas, pesos, casetas ni evidencias: todo número sale de tus documentos.
- No valida el CFDI ante el SAT, no verifica sellos digitales ni estatus de cancelación, no calcula
  impuestos ni dictamina nada fiscal; no sustituye al contador, al agente aduanal ni al SAT.
- No negocia ni responde al transportista por ti: deja la carta lista para que la revises y envíes.
- No trabaja con datos de terceros ni de empleadores: solo con lo que tú le pegas.

---

## Licencia

**Propiedad intelectual de Heroldo Escobedo**, con el código a la vista ([Licencia de uso de Heroldo 1.0](LICENSE)):

- **Uso personal: gratis.** Léelo, pruébalo y adáptalo para aprender o en tus propios datos.
- **Uso en una empresa o con fines de lucro: solo con compra.** Cómpralo en [Agensi](https://agensi.io/skills/auditoria-factura-flete)
  o escribe a heroldo@lolo-enterprises.com. La compra cubre a tu empresa.
- **Siempre se cita la fuente:** «Basado en una skill de Heroldo Escobedo — heroldo.org».
- No se revende ni se vuelve a publicar.

> **In English:** Source-available, not open source. Free for personal use. Business use requires purchase on
> [Agensi](https://agensi.io/skills/auditoria-factura-flete). Attribution to Heroldo Escobedo — heroldo.org is always required.
