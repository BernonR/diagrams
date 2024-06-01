graph TD
    A[Inicio] --> B[Ingresar nombre de usuario]
    B --> C{Nombre de usuario existe?}
    C -->|Si| D[Mostrar error y solicitar nuevo nombre]
    D --> B
    C -->|No| E[Generar clave]
    E --> F[Asignar archivo de palabras]
    F --> G[Guardar usuario en archivo]
    G --> H[Mostrar mensaje de éxito]
    H --> I[Fin]
