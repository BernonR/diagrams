
### Diagrama de Flujo Fase 3

# Diagrama de Flujo Fase 3: Gestión de Usuarios y Seguridad

```mermaid
graph TD
    A[Inicio] --> B[Crear usuario]
    B --> C[Verificar si el usuario es administrador]
    C --> D[Iniciar sesión]
    D --> E{Usuario es administrador?}
    E -->|Sí| F[Ver historial de búsquedas]
    E -->|No| G[Acceder al traductor]
    F --> H[Mostrar historial encriptado]
    G --> I[Traducir palabras]
    H --> J[Fin]
    I --> J
