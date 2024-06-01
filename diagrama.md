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

