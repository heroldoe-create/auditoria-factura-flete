# Entrada del ejemplo — caso 01 · Andén Norte (datos FICTICIOS)

Empresa ficticia «Andén Norte, SA de CV» audita una factura de flete de su transportista ficticio
«Línea del Bajío Transportes, SA de CV». Los cuatro insumos que el usuario le pegaría a la skill:

---

## 1 · Tarifa pactada (tabla del contrato de tarifas, vigente desde 2026-07-01)

| Campo | Valor |
|---|---|
| Transportista | Línea del Bajío Transportes, SA de CV |
| Ruta | Monterrey, NL → Guadalajara, JAL (caja seca 53') |
| Flete base | $18,500.00 MXN por viaje, con maniobras de carga y descarga **incluidas** |
| Casetas | Se reembolsan contra ticket o XML, tope $1,200.00 por viaje |
| Estadía en destino | Primeras 24 h libres; después $850.00/h solo con sello de llegada y de salida |
| Peso | Hasta 24 t incluidas; excedente $95.00/t solo con ticket de báscula foliado |

## 2 · Orden de embarque AN-EMB-2201 (del expediente del usuario)

| Campo | Valor |
|---|---|
| Embarque | AN-EMB-2201 · 1 caja seca 53' · 40 tarimas |
| Peso declarado | 22,000 kg |
| Salida patio origen | 2026-10-05 08:00 |
| Llegada a patio destino | 2026-10-05 21:15 (sello de acceso) |
| Descarga terminada / salida unidad | 2026-10-06 06:40 (sello de salida) |
| Ticket de caseta | IAVE, pluma Saltillo 184, 2026-10-05 09:52, $1,180.00 |
| POD | Firmado en Guadalajara el 2026-10-05 21:40 |

## 3 · Factura F-7781 — transcripción fiel del CFDI adjunto

Emisor: Línea del Bajío Transportes, SA de CV · Folio: F-7781 · Fecha: 2026-10-08 ·
UUID: ficticio AN-UUID-7781 · Moneda: MXN · Forma de pago: 03 (transferencia)

| # | Concepto | Cantidad | P. unitario | Importe |
|---|---|---|---|---|
| 1 | Flete MTY-GDL caja seca | 1 | 18,500.00 | 18,500.00 |
| 2 | Casetas | 1 | 2,360.00 | 2,360.00 |
| 3 | Estadía destino 2 h | 2 | 850.00 | 1,700.00 |
| 4 | Peso excedente 3 t (25 t declarados) | 3 | 95.00 | 285.00 |
| 5 | Maniobras de descarga | 1 | 1,200.00 | 1,200.00 |
| | **Subtotal** | | | **24,045.00** |
| | IVA 16 % | | | **3,847.20** |
| | **Total** | | | **27,892.20** |

## 4 · Evidencias aportadas por el usuario

- Ticket de caseta IAVE, pluma Saltillo 184, 2026-10-05 09:52, **$1,180.00** (único del viaje).
- Sellos de patio destino: llegada 2026-10-05 21:15, salida 2026-10-06 06:40.
- No hay ticket de báscula en el expediente.
- POD firmado el 2026-10-05 21:40.
