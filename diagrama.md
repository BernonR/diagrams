# Diagramas del Proyecto

## Diagrama de Clases UML

```mermaid
classDiagram
    class Usuario {
        - string nombre
        - string clave
        - string archivoPalabras
        - bool esAdmin
        + crearUsuario()
        + iniciarSesion()
    }
    
    class Traduccion {
        - string espanol
        - string italiano
        - string frances
        - string aleman
        - string ingles
    }
    
    class Nodo {
        - Traduccion dato
        - Nodo* izquierda
        - Nodo* derecha
        - int altura
    }
    
    class ArbolAVL {
        + insertarAVL(Nodo* nodo, Traduccion& traduccion)
        + eliminarAVL(Nodo* raiz, string& palabra)
        + enOrden(Nodo* nodo)
    }
    
    class Encriptacion {
        + encriptarPalabra(string& palabra)
        + desencriptarPalabra(string& palabraEncriptada)
    }

    Usuario -- Traduccion
    Nodo "1" -- "1" Traduccion : contiene
    Nodo "1" -- "0..1" Nodo : izquierda
    Nodo "1" -- "0..1" Nodo : derecha
    ArbolAVL -- Nodo
    ArbolAVL -- Traduccion
    Encriptacion -- Traduccion

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

graph TD
    A[Inicio] --> B[Seleccionar idioma de origen]
    B --> C[Ingresar palabra en idioma de origen]
    C --> D{Palabra encontrada en el diccionario?}
    D -->|No| E[Mostrar error y solicitar nueva palabra]
    E --> B
    D -->|Si| F[Seleccionar idioma de destino]
    F --> G[Traducir palabra]
    G --> H[Mostrar palabra traducida]
    H --> I{Reproducir sonido?}
    I -->|Si| J[Reproducir sonido de la palabra]
    I -->|No| K[Solicitar nueva traducción?]
    J --> K
    K -->|Si| B
    K -->|No| L[Fin]

