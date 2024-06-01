
### Diagrama de Flujo de Iniciar Sesión

```markdown
# Diagrama de Flujo de Iniciar Sesión

```mermaid
graph TD
    A[Inicio] --> B[Ingresar nombre de usuario]
    B --> C[Ingresar clave]
    C --> D{Usuario y clave correctos?}
    D -->|No| E[Mostrar error]
    E --> F[Solicitar nuevamente]
    F --> B
    D -->|Sí| G[Mostrar mensaje de éxito]
    G --> H[Fin]
