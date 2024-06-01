
### Diagrama de Flujo de Carga de Palabras


# Diagrama de Flujo de Carga de Palabras

```mermaid
graph TD
    A[Inicio] --> B[Verificar existencia del archivo]
    B --> C{Archivo existe?}
    C -->|No| D[Crear nuevo archivo]
    D --> E[Cargar palabras en el arbol]
    C -->|Sí| E[Cargar palabras en el arbol]
    E --> F[Mostrar mensaje de éxito]
    F --> G[Fin]
