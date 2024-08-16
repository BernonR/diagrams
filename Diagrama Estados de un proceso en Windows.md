# Diagrama Estados de un proceso en Windows

```mermaid
graph TD
    A[Inicio] --> B[Proceso creado]
    B --> C{Proceso cargado en memoria}
    C -->|Sí| D[Proceso listo]
    D --> E{Seleccionado por el planificador?}
    E -->|Sí| F[Proceso en ejecución]
    F --> G{Esperando E/S?}
    G -->|Sí| H[Proceso bloqueado]
    H --> I{Evento completado?}
    I -->|Sí| D
    G -->|No| J[Proceso finalizado]
    J --> K[Fin]
