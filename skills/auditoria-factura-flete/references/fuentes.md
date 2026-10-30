# Fuentes y alcance legal

La skill no cita reglas fiscales ni aduanales por su cuenta: ni valida CFDI ante el SAT, ni dictamina
IVA acreditable ni deducibilidad. Esta lista es la evidencia del marco que rodea al paquete
(licencia y alcance); la operación de la auditoría se apoya únicamente en los documentos del usuario
(tarifa, embarque, evidencias, factura).

1. **Ley Federal del Derecho de Autor**, Cámara de Diputados, https://www.diputados.gob.mx/LeyesBiblio/pdf/LFDA.pdf,
   última reforma DOF 14-05-2026. Consultada el 2026-10-29. Es la ley que ampara la licencia del
   paquete (`LICENSE`); no se toca el texto de la licencia.
2. **Guía de precios de Agensi para skills** (una tarea USD 3–9; paquete completo USD 12–25),
   agensi.io, 2026-04-25, vía el scouteo interno `creador/producto/CATALOGO-SKILLS-AGENSI.md`.
   Consultada el 2026-10-29. Sostiene el precio de USD 20 del paquete.
3. **Política interna de licenciamiento de Heroldo**, `creador/producto/licencia/POLITICA-LICENCIA-SKILLS.md`,
   2026-10-29. Define la Licencia de uso de Heroldo 1.0 que lleva este paquete.

## Alcance (lo que la skill no decide)

- **Tratamiento fiscal de la factura** (IVA acreditable, deducibilidad, retenciones, momentos de
  pago): lo confirma el **contador** del usuario con las reglas vigentes del SAT, la LIVA y la LISR;
  la skill toma los impuestos tal como el CFDI los declara y discute solo importes bases.
- **Validación del CFDI** (estatus en el SAT, autenticidad de sellos, cancelación): corresponde al
  **PAC** del usuario o a la verificación oficial del SAT; esta skill audita el contenido comercial,
  no la validez del comprobante.
- **Si el embarque cruza frontera o requiere complemento Carta Porte / pedimento**: corresponde al
  **agente aduanal** y a las reglas oficiales del SAT; esta skill cruza documentos comerciales de
  flete nacional por carretera y nada más.
