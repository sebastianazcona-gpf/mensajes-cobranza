# Generador de comunicaciones de proceso y cobranza GPF

Aplicación web estática para generar comunicaciones vinculadas con el proceso de VIRAAL Pensiones y con la cobranza de GPF, desde la formalización y dispersión del financiamiento hasta la carta de no adeudo.

## Funciones

- Selección de los hitos del nuevo flujo comercial, pensionario y de cobranza.
- Identificación del área responsable y del tipo de comunicación.
- Formulario automático de campos dinámicos para cada mensaje.
- Mensajes cálidos para actualizaciones del proceso y mensajes directos para cobranza.
- Mensaje de WhatsApp listo para copiar.
- Vista previa y descarga del correo en HTML.
- Opción para imprimir o guardar el correo como PDF.
- Identificación de hitos internos que no generan mensajes al cliente.
- Procesamiento local en el navegador; la aplicación no guarda ni transmite los datos capturados.

## Reglas incorporadas

- El orden de recuperación es: préstamo de nómina con MasNómina, retroactivo y, como última fuente, AFORE.
- No existe una etapa de recuperación posterior a AFORE.
- El proyecto debe estructurarse para liquidarse, como máximo, con AFORE antes de llegar a GPF.
- GPF solo comunica un nuevo saldo después de recibir, conciliar y registrar el pago.
- GPF solicita únicamente el saldo pendiente; cualquier excedente de AFORE permanece con el pensionado.
- Cuando el saldo llega a $0.00, deben detenerse los mensajes posteriores de pago.

## Ejecución local

Abre `index.html` directamente en un navegador moderno o ejecuta un servidor local:

```bash
python -m http.server 8000
```

Después visita `http://localhost:8000`.

## Publicación en Vercel

1. En Vercel, selecciona **Add New > Project**.
2. Importa el repositorio `sebastianazcona-gpf/mensajes-cobranza`.
3. Deja **Framework Preset** como `Other`.
4. No configures comando de compilación.
5. Usa el directorio raíz como directorio de salida.
6. Publica el proyecto.

Vercel reconocerá `index.html` como sitio estático.

## Control de uso

**[VALIDAR] Pendiente de revisión de Legal (Jorge Rico) antes de uso externo.**

No deben enviarse comunicaciones con campos incompletos, saldos sin fecha de corte, pagos no conciliados o datos bancarios que no provengan de un catálogo autorizado.
