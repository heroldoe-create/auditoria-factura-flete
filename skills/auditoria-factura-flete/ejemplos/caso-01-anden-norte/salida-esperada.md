# Salida esperada — caso 01 · Andén Norte

Lo que la skill debe entregar al pegarle los cuatro insumos de `entrada.md`, sin retoques. Síguelo a
mano: cada cifra se deriva de la entrada.

---

## 1 · Tabla de auditoría

| # | Renglón de factura | Cobrado | Veredicto | Código | Aprobado | En disputa | No comprobado | Evidencia que manda |
|---|---|---:|---|---|---:|---:|---:|---|
| 1 | Flete MTY-GDL caja seca | $18,500.00 | APROBADO | — | 18,500.00 | | | Tarifa (flete base) + POD AN-EMB-2201 |
| 2 | Casetas | $2,360.00 | DISPUTADO | D4 | 1,180.00 | 1,180.00 | | Ticket IAVE $1,180.00; tope tarifa $1,200.00 |
| 3 | Estadía destino 2 h | $1,700.00 | DISPUTADO | D1+D5 | | 1,700.00 | | Sellos: 21:15 → 06:40 = 9 h 25 min < 24 h libres |
| 4 | Peso excedente 3 t | $285.00 | NO COMPROBADO | D6+D7 | | | 285.00 | Embarque declara 22 t (≤ 24 t incluidas); sin báscula |
| 5 | Maniobras de descarga | $1,200.00 | DISPUTADO | D3 | | 1,200.00 | | Tarifa: maniobras incluidas en el flete |

Aritmética interna de la factura: cuadra (24,045.00 × 16 % = 3,847.20; total 27,892.20). Sin D8.

## 2 · Totales

| | Base | IVA 16 % (tal como declara el CFDI) | Total |
|---|---:|---:|---:|
| Factura | 24,045.00 | 3,847.20 | 27,892.20 |
| Aprobado | 19,680.00 | 3,148.80 | 22,828.80 |
| En disputa | 4,080.00 | 652.80 | 4,732.80 |
| No comprobado | 285.00 | 45.60 | 330.60 |
| **Pago recomendado ahora** | **19,680.00** | **3,148.80** | **22,828.80** |

Retener de la disputa: $4,732.80. Pedir soporte del no comprobado: $330.60 (que se disputa en
automático si no llega la báscula, porque 22 t están dentro de las 24 t incluidas).

## 3 · Expediente de evidencia

### Discrepancia D4 — Casetas (renglón 2)

| Campo | Contenido |
|---|---|
| Renglón de factura | «Casetas», 1, $2,360.00 |
| Lo que dice la tarifa | «Casetas se reembolsan contra ticket o XML, tope $1,200.00 por viaje» |
| Lo que dice el embarque | Un solo trayecto MTY→GDL, salida 2026-10-05 08:00 |
| La evidencia | Ticket IAVE pluma Saltillo 184, 2026-10-05 09:52, $1,180.00 (único del viaje) |
| Veredicto | Cobrado el doble de lo comprobado; se aprueba lo del ticket, se disputa $1,180.00 |
| Importe en disputa | $1,180.00 base (+ $188.80 IVA) |

### Discrepancia D1+D5 — Estadía (renglón 3)

| Campo | Contenido |
|---|---|
| Renglón de factura | «Estadía destino 2 h», 2 × $850.00 = $1,700.00 |
| Lo que dice la tarifa | «Primeras 24 h libres; después $850.00/h solo con sello de llegada y de salida» |
| Lo que dice el embarque | Llegada 2026-10-05 21:15; salida 2026-10-06 06:40 → 9 h 25 min |
| La evidencia | Sellos de patio con fecha-hora |
| Veredicto | El tiempo estuvo dentro de las 24 h libres: no hay base tarifada ni tiempo acreditado |
| Importe en disputa | $1,700.00 base (+ $272.00 IVA) |

### Discrepancia D6+D7 — Peso excedente (renglón 4)

| Campo | Contenido |
|---|---|
| Renglón de factura | «Peso excedente 3 t (25 t declarados)», 3 × $95.00 = $285.00 |
| Lo que dice la tarifa | «Hasta 24 t incluidas; excedente $95.00/t solo con ticket de báscula foliado» |
| Lo que dice el embarque | Peso declarado 22,000 kg (≤ 24 t incluidas) |
| La evidencia | Ninguna: no hay ticket de báscula; la factura contradice el propio embarque |
| Veredicto | NO COMPROBADO: se pide báscula foliada; de no llegar, se disputa (22 t caben en tarifa). Además, la factura se contradice: 25 t − 24 t incluidas = 1 t, no 3 t; con báscula de 25 t lo máximo aprobable sería $95.00 |
| Importe no comprobado | $285.00 base (+ $45.60 IVA) |

### Discrepancia D3 — Maniobras (renglón 5)

| Campo | Contenido |
|---|---|
| Renglón de factura | «Maniobras de descarga», 1, $1,200.00 |
| Lo que dice la tarifa | «Flete base … con maniobras de carga y descarga incluidas» |
| Lo que dice el embarque | Descarga efectuada el 2026-10-06 |
| La evidencia | La tarifa misma: el cobro está incluido en el renglón 1 |
| Veredicto | Doble cobro de un concepto ya facturado en el flete base |
| Importe en disputa | $1,200.00 base (+ $192.00 IVA) |

## 4 · Faltantes (preguntas al transportista)

1. Renglón 2: aun con un segundo ticket, la tarifa topa las casetas en $1,200.00 por viaje; lo más
   que podría aprobarse adicional son $20.00, y $1,160.00 se disputan en cualquier caso.
2. Renglón 4: ticket de báscula foliado (folio, fecha, placa) que acredite el peso real; aun con
   25 t, el excedente sería 1 t ($95.00).

## 5 · Carta de disputa (lista para copiar)

> **Asunto: Discrepancias en factura F-7781 — embarque AN-EMB-2201 (retenido $5,063.40)**
>
> Estimados Línea del Bajío Transportes:
>
> Al cruzar su factura F-7781 (UUID AN-UUID-7781, 2026-10-08, total $27,892.20 MXN) contra la tarifa
> pactada, la orden de embarque AN-EMB-2201 y las evidencias del viaje, encontramos tres diferencias
> en disputa por **$4,080.00 base ($4,732.80 con IVA)** y un cargo sin soporte por **$285.00 base
> ($330.60 con IVA)**; en total retenemos **$4,365.00 base ($5,063.40 con IVA)**:
>
> 1. **Casetas (D4):** se cobraron $2,360.00; el expediente acredita un ticket de $1,180.00 (IAVE,
>    pluma Saltillo 184, 2026-10-05 09:52). Diferencia: **$1,180.00 base**. Aun con un segundo
>    ticket, la tarifa pactada topa las casetas en $1,200.00 por viaje.
> 2. **Estadía en destino (D1/D5):** se cobraron 2 h ($1,700.00); los sellos de patio acreditan
>    llegada 2026-10-05 21:15 y salida 2026-10-06 06:40 (9 h 25 min), dentro de las 24 h libres de la
>    tarifa. Diferencia: **$1,700.00 base**.
> 3. **Peso excedente (D6/D7):** se cobraron 3 t ($285.00) sobre «25 t declarados»; el embarque
>    declara 22,000 kg, dentro de las 24 t incluidas, y no hay ticket de báscula. Diferencia:
>    **$285.00 base**, retenida hasta recibir la báscula foliada.
> 4. **Maniobras de descarga (D3):** se cobraron $1,200.00 por un concepto que la tarifa pactada
>    incluye en el flete base. Diferencia: **$1,200.00 base**.
>
> Liberamos el pago de los **$22,828.80** aprobados y solicitamos, a la brevedad, la nota de crédito
> por **$4,732.80** y, para el peso excedente, el ticket de báscula foliado; sin él, también
> pediremos nota de crédito por **$330.60** (o la evidencia que respalde los renglones 2 y 4 de la
> factura: la segunda caseta y la báscula foliada).
>
> Atentamente, Cuentas por pagar — Andén Norte, SA de CV

## 6 · Advertencia de alcance

La factura se tomó tal como el transportista la emitió; la validación del CFDI ante el SAT y el
tratamiento fiscal (IVA acreditable, deducibilidad, retenciones) los confirma tu contador o tu PAC.
Esta auditoría es comercial: cruza tarifa, embarque y evidencias.
