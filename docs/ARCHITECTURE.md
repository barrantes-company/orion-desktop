# ORIÓN — Arquitectura inicial

## Capas

1. **Desktop shell (Tauri/Rust):** ventana, sistema operativo, permisos, almacenamiento seguro e integraciones nativas.
2. **Frontend (React/TypeScript):** experiencia conversacional, navegación, estado de UI y presentación de resultados.
3. **Application core:** sesiones, contexto, políticas, planificación y coordinación de tareas.
4. **Model gateway:** interfaz desacoplada para modelos cloud y locales.
5. **Tools:** adaptadores de archivos, documentos, navegador y automatización, habilitados gradualmente.
6. **Persistence:** SQLite para sesiones, preferencias, metadatos e historial local.

## Principios de diseño técnico

- Separar UI, dominio, proveedores de IA y herramientas.
- Definir contratos tipados entre frontend y backend.
- No acoplar la interfaz a un único proveedor de modelos.
- Manejar streaming, cancelación, timeout y errores.
- Mantener secretos fuera del frontend y del repositorio.
- Validar cada operación de herramienta en el backend.

## Niveles de autorización propuestos

- **L0 — Lectura:** consultar información en ubicaciones autorizadas.
- **L1 — Preparación:** proponer o preparar cambios sin aplicarlos.
- **L2 — Ejecución confirmada:** aplicar cambios tras confirmación del usuario.
- **L3 — Crítica:** operaciones irreversibles o sensibles con confirmación específica.

El modelo propone; el backend valida permisos y ejecuta. El modelo nunca debe poder elevar su propio nivel de autorización.

## Primer incremento

Construir únicamente el shell visual y navegación con datos simulados. No integrar todavía proveedor de IA, ejecución de comandos, automatización ni acceso amplio al sistema de archivos.
