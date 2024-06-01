# Diagrama de Flujo Fase 1: Proceso de Captura y Definición de Datos

```mermaid
graph TD
    A[Inicio] --> B[Cargar archivo de palabras]
    B --> C{Archivo existe?}
    C -->|No| D[Crear nuevo archivo]
    D --> E[Mostrar mensaje de éxito]
    C -->|Sí| F[Cargar palabras en el árbol]
    F --> E
    E --> G[Agregar nuevas traducciones]
    G --> H[Eliminar palabras]
    H --> I[Guardar cambios en archivo]
    I --> J[Fin]
