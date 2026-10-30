# Tipología de discrepancias (D1–D8)

Cada discrepancia se clasifica con UN código. El código manda sobre el texto: si el caso no encaja
en ninguno, se usa el más cercano y se explica por qué; no se inventa un código nuevo.

| Código | Discrepancia | Qué la desmiente | Evidencia que exige la tarifa |
|---|---|---|---|
| **D1** | Concepto no pactado | El concepto no aparece en la tarifa pactada | La tarifa misma |
| **D2** | Precio sobre tarifa | Cobro mayor al precio pactado para ese concepto | Tarifa (fila o cláusula citada) |
| **D3** | Cantidad/cobro duplicado | El mismo concepto cobrado dos veces en la factura, o ya incluido en otro renglón | La propia factura + tarifa |
| **D4** | Casetas: sin soporte o sobre lo comprobado | Ticket de caseta con importe menor, faltante, o casetas duplicadas | Ticket o XML de caseta por tramo |
| **D5** | Estadía sin evidencia de tiempo | Sellos de llegada/salida que no cubren las horas cobradas, o inexistentes | Sello de llegada y de salida (fecha-hora) |
| **D6** | Excedente de peso no acreditado | Peso del embarque menor al cobrado, o sin ticket de báscula | Ticket de báscula + peso del embarque |
| **D7** | Contradicción con el embarque | La factura contradice carta porte / orden de embarque (ruta, bultos, fechas, peso) | El documento de embarque |
| **D8** | Aritmética interna de la factura | Cantidad × unitario ≠ importe, o subtotal/IVA/total no cuadran | La propia factura |

## Jerarquía cuando chocan dos códigos

1. **D8 manda primero:** si la factura no cuadra consigo misma, eso se reporta antes que cualquier
   cruce externo (un importe mal multiplicado invalida el renglón entero).
2. Después **D7** (el embarque es el hecho físico), luego **D1/D2** (la tarifa es el derecho a cobrar)
   y al final **D3–D6** (la evidencia del cobro específico).
3. Un mismo renglón puede tener dos códigos (p. ej. estadía no pactada Y sin sellos): se reporta una
   sola discrepancia con ambos códigos «D1+D5» y el importe completo en disputa, no dos importes.

## Lo que NO es discrepancia

- Un renglón caro pero pactado y evidenciado: está APROBADO aunque al usuario le duela; la skill no
  renegocía tarifas, audita contra las que hay.
- Diferencias por redondeo de centavos dentro de la tolerancia que la tarifa declare explícitamente.
- Impuestos: la skill toma el IVA y retenciones **tal como el CFDI los declara**; discute el importe
  base y su proporción, no la tasa.
