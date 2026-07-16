# Generador de comunicaciones de cobranza GPF

Aplicación web estática para generar comunicaciones de cobranza relacionadas con los pasos definidos del proceso de pensiones.

## Funciones

- Selección del número de paso y su descripción.
- Formulario automático de campos dinámicos.
- Mensaje de WhatsApp listo para copiar.
- Vista previa y descarga del correo en HTML.
- Opción para imprimir o guardar el correo como PDF.
- Identificación de hitos internos que no generan mensajes al cliente.
- Procesamiento local en el navegador; la aplicación no guarda ni transmite los datos capturados.

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
