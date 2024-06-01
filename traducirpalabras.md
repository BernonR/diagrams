
### Diagrama de Flujo de Traducción de Palabras


# Diagrama de Flujo de Traducción de Palabras

```mermaid
graph TD
    A[Inicio] --> B[Seleccionar idioma de origen]
    B --> C[Ingresar palabra en idioma de origen]
    C --> D[Buscar palabra en el arbol]
    D --> E{Palabra encontrada?}
    E -->|No| F[Mostrar mensaje de error]
    F --> G[Fin]
    E -->|Sí| H[Seleccionar idioma de destino]
    H --> I[Mostrar traducción]
    I --> J[Guardar en historial]
    J --> K{Reproducir sonido?}
    K -->|Sí| L[Reproducir sonido]
    K -->|No| M[Fin]
    L --> M[Fin]
