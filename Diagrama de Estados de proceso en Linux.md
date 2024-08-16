# Diagrama de Estados de proceso en Linux

```mermaid
graph TD
    A[Inicio] --> B[Proceso creado]
    B --> C[Proceso listo]
    C --> D{Seleccionado por el planificador?}
    D -->|Sí| E[Proceso en ejecución]
    E --> F{Esperando evento o en espera?}
    F -->|Sí| G[Proceso suspendido]
    G --> H{Evento completado?}
    H -->|Sí| C
    F -->|No| I{Proceso detenido por señal?}
    I -->|Sí| J[Proceso detenido]
    J --> K{Reanudado por señal?}
    K -->|Sí| C
    E --> L{Proceso terminado?}
    L -->|Sí| M[Proceso zombi]
    M --> N[Fin]
