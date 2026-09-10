# Página de cobro para llavero NFC

Página de una sola pantalla con los datos de transferencia. El llavero NFC
guarda el enlace; quien paga acerca el teléfono y copia los datos hacia la
app del banco.

La plantilla para un cliente nuevo (incluidos llaveros para Uber) vive en
[`simpleideal/cobro`](https://github.com/simpleideal/cobro).

## Idea práctica: dos personas, dos mensajes

El llavero se usa en la calle, con apuro. El caso más claro —y el de los
llaveros para Uber más adelante— es este:

1. El pasajero (el **tercero**) se sube al auto.
2. El conductor (el **cliente**) le muestra el llavero.
3. El pasajero acerca el teléfono, copia los datos y hace la transferencia
   en la app de su banco.
4. El pasajero toca el ícono verde de WhatsApp.
5. El conductor recibe ese mensaje y se entera de que le van a transferir.

Hay dos lectores. No se les puede decir lo mismo en el mismo texto.

| Quién | Dónde lo lee | Qué tiene que entender |
| --- | --- | --- |
| El tercero (quien paga) | La página que abre el NFC | Que debe subir el voucher o mostrárselo a quien le está cobrando (en Uber: al conductor). |
| El cliente (quien cobra) | El WhatsApp que le llega | Que le van a hacer una transferencia. No que el pago ya está hecho. |

Por eso esta página muestra el aviso con el pin, para quien paga:

> 📌 Importante: sube tu voucher por WhatsApp o muéstraselo a quien te está cobrando.

El texto prellenado del ícono de WhatsApp lo recibe el cliente:

> Hola Brillith, te aviso que haré la transferencia.

Si el WhatsApp dice “sube tu voucher”, quien cobra cree que le hablan a él.
Si dice “envío el comprobante”, parece que el pago ya está hecho.

En un llavero para Uber, el aviso de la página puede decir “al conductor”
en lugar de “a quien te está cobrando”.
