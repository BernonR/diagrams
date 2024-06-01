
### Diagrama de Flujo de Encriptación y Desencriptación de Palabras

# Diagrama de Flujo de Encriptación y Desencriptación de Palabras

```mermaid
graph TD
    A[Inicio] --> B[Seleccionar operación]
    B --> C{Operación}
    C -->|Encriptar| D[Ingresar palabra]
    D --> E[Encriptar usando mapa]
    E --> F[Guardar palabra encriptada]
    F --> G[Mostrar palabra encriptada]
    G --> H[Fin]
    C -->|Desencriptar| I[Ingresar palabra encriptada]
    I --> J[Desencriptar usando mapa]
    J --> K[Mostrar palabra original]
    K --> H
