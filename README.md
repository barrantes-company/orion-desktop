# ORIÓN Desktop

Asistente IA de escritorio de BARRANTES CO.

## Estado

Fase inicial: estructura del proyecto y definición de arquitectura. La interfaz de referencia aprobada es ORIÓN UI v3 (conversación activa).

## Dirección del producto

ORIÓN debe sentirse como un asistente cercano y práctico: entiende solicitudes, propone soluciones, ejecuta acciones autorizadas y comunica resultados con claridad.

### Principios de experiencia

- Conversación como espacio principal.
- Interfaz compacta, simple y amigable.
- Acciones sugeridas contextuales, no un panel administrativo.
- Tema claro predeterminado y tema oscuro alternativo.
- Identidad visual premium tecnológica.
- El logo maestro aprobado es un activo inmutable: no redibujar, reinterpretar ni sustituir.

## Arquitectura objetivo

- **Desktop:** Tauri 2
- **UI:** React + TypeScript
- **Estilos:** Tailwind CSS
- **Backend nativo:** Rust
- **Persistencia local:** SQLite
- **IA:** gateway desacoplado para proveedores cloud y runtime local

La elección de proveedores y la integración de modelos se realizará después de tener la capa de interfaz y los límites de seguridad establecidos.

## Fases

1. **Base visual:** shell de escritorio, navegación, conversación, panel lateral, tema claro/oscuro.
2. **Interacción local:** estado de conversación, adjuntos de interfaz, historial y preferencias.
3. **Servicios IA:** gateway, selección de modelo, streaming y gestión de errores.
4. **Herramientas:** archivos, documentos y acciones con permisos explícitos.
5. **Endurecimiento:** auditoría, almacenamiento seguro, pruebas y empaquetado Windows.

## Seguridad por diseño

- El modelo no recibe acceso directo a credenciales.
- Las acciones con efectos externos requieren validación del motor y autorización según nivel de riesgo.
- Los documentos y páginas externas se tratan como datos no confiables.
- Acceso a archivos limitado a ubicaciones autorizadas.
- Registrar operaciones sensibles y resultados.

## Desarrollo

La estructura de carpetas y los comandos de instalación se añadirán al completar el scaffold de Tauri/React en el entorno Windows de desarrollo.

## Licencia

Todos los derechos reservados. BARRANTES CO.
