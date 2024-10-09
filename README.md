# UD1 A5 Sobre XML

### 1. Indica las características propias del lenguaje XML.

- **XML** (eXtensible Markup Language) es un metalenguaje diseñado para el almacenamiento y el intercambio de datos de forma estructurada.  
- **Características**:
  - **Extensible**: Permite definir etiquetas personalizadas según las necesidades del usuario.
  - **Legible por humanos y máquinas**: El formato es fácilmente interpretable.
  - **Jerárquico**: Los elementos están anidados en una estructura de árbol.
  - **Independiente de plataforma**: Se puede utilizar en diferentes sistemas operativos y lenguajes de programación.
  - **Bien definido**: Sigue una estricta normativa sintáctica para evitar errores en su procesamiento.

---

### 2. Identifica la estructura de un documento XML y sus reglas sintácticas.

Un documento XML sigue una estructura jerárquica que contiene:
  - **Declaración XML**: Define la versión y la codificación (`<?xml version="1.0" encoding="UTF-8"?>`).
  - **Nodo raíz**: El elemento principal que engloba a todos los demás elementos.
  - **Etiquetas**: Deben estar bien anidadas y cada etiqueta de apertura debe tener una de cierre.
  - **Atributos**: Se definen dentro de las etiquetas, entre comillas dobles.
  
**Reglas sintácticas**:
  - XML distingue entre mayúsculas y minúsculas.
  - No puede haber elementos superpuestos ni mal cerrados.
  - Un documento XML solo puede tener un nodo raíz.

---

### 3. En XML qué es un nodo raíz.

El **nodo raíz** es el primer y único elemento que contiene a todos los demás elementos en un documento XML. Todos los documentos XML deben tener un nodo raíz que englobará el contenido jerárquico del archivo.

---

### 4. Indica qué es un elemento vacío. Ejemplos.

Un **elemento vacío** es aquel que no contiene contenido ni elementos hijos. Puede definirse de dos formas:
  - `<elemento></elemento>`
  - O bien en su forma abreviada: `<elemento />`

**Ejemplo**:
```xml
<img src="imagen.jpg" />
```
Este es un ejemplo de un elemento vacío en XML.

---

### 5. Qué sentido tiene crear documentos XML bien formados.

Crear un documento XML bien formado asegura que:
  - Cumple con todas las reglas de sintaxis.
  - Facilita la lectura y el procesamiento por las aplicaciones.
  - Permite su correcto intercambio entre diferentes sistemas sin errores.
  
Un documento mal formado podría no ser interpretado correctamente por las herramientas de software, lo que causaría fallos en su procesamiento.

---

### 6. Qué es un espacio de nombres. Ventajas de uso.

Un **espacio de nombres** en XML se utiliza para evitar conflictos de nombres cuando se combinan elementos de diferentes vocabularios XML que podrían compartir nombres de etiquetas. Se define utilizando el atributo `xmlns` y un URI único.

**Ventajas**:
  - **Evitar colisiones de nombres**: Permite distinguir elementos con el mismo nombre que provienen de diferentes contextos.
  - **Interoperabilidad**: Facilita la combinación de documentos XML con diferentes esquemas sin generar ambigüedades.
  
**Ejemplo**:
```xml
<e1:carta xmlns:e1="http://www.ejemplo1.com">
   <e1:palo>Corazones</e1:palo>
</e1:carta>
```

---

### 7. Entidades en XML. Crea un XML con las entidades vistas en clase.

Las **entidades** en XML permiten representar caracteres especiales que tienen significado dentro del propio lenguaje.

**Ejemplo de un documento XML con entidades**:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<documento>
   <titulo>Ejemplo de uso de entidades</titulo>
   <contenido>Los símbolos &lt; y &gt; son usados para etiquetas en XML.</contenido>
</documento>
```

---

### 8. Comentarios en XML. Muestra uno de los ejercicios anteriores con el enunciado dentro de un comentario. Dentro del comentario deben aparecer dos guiones.

Los **comentarios** en XML se escriben entre `<!--` y `-->`. No se procesan y son útiles para dejar notas explicativas.

**Ejemplo**:
```xml
<!-- Este XML muestra un ejemplo de uso de entidades -->
<?xml version="1.0" encoding="UTF-8"?>
<documento>
   <titulo>Ejemplo de uso de entidades</titulo>
   <contenido>Los símbolos &lt; y &gt; son usados para etiquetas en XML.</contenido>
</documento>
```