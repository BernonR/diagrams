# Diagrama General del Proyecto (Horizontal)

```mermaid
graph LR
    subgraph Fase 1
        A1[Inicio] --> B1[Cargar archivo de palabras]
        B1 --> C1{Archivo existe?}
        C1 -->|No| D1[Crear nuevo archivo]
        D1 --> E1[Mostrar mensaje de éxito]
        C1 -->|Sí| F1[Cargar palabras en el árbol]
        F1 --> E1
        E1 --> G1[Agregar nuevas traducciones]
        G1 --> H1[Eliminar palabras]
        H1 --> I1[Guardar cambios en archivo]
        I1 --> J1[Fin]
    end

    subgraph Fase 2
        A2[Inicio] --> B2[Encriptar palabras buscadas]
        B2 --> C2[Guardar palabras encriptadas en archivo]
        C2 --> D2[Desencriptar palabras para mostrar historial]
        D2 --> E2[Mostrar top de palabras más buscadas]
        E2 --> F2[Fin]
    end

    subgraph Fase 3
        A3[Inicio] --> B3[Crear usuario]
        B3 --> C3[Verificar si el usuario es administrador]
        C3 --> D3[Iniciar sesión]
        D3 --> E3{Usuario es administrador?}
        E3 -->|Sí| F3[Ver historial de búsquedas]
        E3 -->|No| G3[Acceder al traductor]
        F3 --> H3[Mostrar historial encriptado]
        G3 --> I3[Traducir palabras]
        H3 --> J3[Fin]
        I3 --> J3
    end

    subgraph Integración General
        J1 --> A2
        F2 --> A3
    end
