# Diagrama de Flujo de Liberación de Memoria

```mermaid
graph TD
    A[Inicio] --> B[Recorrer el árbol AVL]
    B --> C{Nodo actual es NULL?}
    C -->|Sí| D[Retornar]
    C -->|No| E[Liberar subárbol izquierdo]
    E --> F[Liberar subárbol derecho]
    F --> G[Eliminar nodo actual]
    G --> H[Fin]
