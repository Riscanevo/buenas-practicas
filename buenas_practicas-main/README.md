# 🧮 Refactorización del Archivo `app-legacy.js`

Este documento explica todas las **refactorizaciones realizadas** al archivo original `app-legacy.js` como parte del proceso de auditoría manual.  
El objetivo fue modernizar el código, aplicar buenas prácticas de estilo y mantener la misma funcionalidad sin alterar la lógica del programa.

---

## 📋 Objetivo General

Optimizar el código eliminando malas prácticas y ajustándolo a las normas de estilo modernas de JavaScript.  
Se aplicaron las siguientes reglas de auditoría:

1. **no-var:** Prohibir el uso de `var`, reemplazándolo por `let` o `const`.  
2. **eqeqeq:** Reemplazar todas las comparaciones laxas `==` o `!=` por comparaciones estrictas `===` o `!==`.  
3. **camelCase:** Cambiar todos los nombres de variables y funciones a formato `camelCase`.  
4. **quotes:** Usar únicamente comillas simples `' '` en todo el archivo.  

---

## ⚙️ Refactorizaciones Realizadas

### 🔹 1. Reemplazo de `var` por `let` o `const`
Se reemplazaron todas las declaraciones `var` por `let` o `const` según el contexto:
- **`const`** para valores inmutables, como constantes o configuraciones.
- **`let`** para variables cuyo valor puede cambiar durante la ejecución.

**Ejemplo:**
```
    js
    // Antes
    var buffer = "0";
    var historial = [];
    
    // Después
    let buffer = '0';
    let historial = [];
```
### 🔹 2. Comparaciones estrictas (=== y !==)
Se reemplazaron todas las comparaciones laxas por comparaciones estrictas para evitar errores de coerción de tipos y mejorar la precisión lógica del código.
```
    // Antes
    if (buffer == "0") { ... }
    if (display_element != null) { ... }

    // Después
    if (buffer === '0') { ... }
    if (displayElement !== null) { ... }
```

### 🔹 3. Conversión de nombres a formato camelCase

Todos los nombres de variables y funciones que estaban en snake_case fueron renombrados a camelCase para seguir la convención estándar de JavaScript.

### 🔹 4. Comillas simples unificadas (' ')

Todas las comillas dobles (") fueron reemplazadas por comillas simples (') para mantener la consistencia del estilo.

```
    // Antes
    alert("Error: La tarea no puede estar vacía.");

    // Después
    alert('Error: La tarea no puede estar vacía.');
```

### 🔹 5. Uso de plantillas literales (Template Strings)
Se reemplazaron concatenaciones con el operador + por template strings (${}) para mejorar la legibilidad y reducir errores al construir cadenas.

```
    // Antes
    var logEntry = memoriaPrevia + " " + operacionPrevia + " " + intBuffer + " = " + memoria;

    // Después
    const logEntry = `${memoriaPrevia} ${operacionPrevia} ${intBuffer} = ${memoria}`;

```
### 🔹 6. Mejoras de legibilidad y consistencia
- Se reestructuró la indentación del código para mantener un formato uniforme.
- Se añadió espaciado entre bloques lógicos y funciones para mejorar la lectura.
- Se eliminaron comentarios redundantes o inconsistentes, conservando solo los relevantes.
- Se normalizó el uso de const y let dentro de funciones y ciclos.


### 🔹 7. Inicialización más clara de 
Las funciones de inicialización (initCalculadora() e initTodoList()) se mantuvieron, pero ahora usan variables con nombres más claros y verificaciones estrictas para los elementos del DOM.}
```
    // Antes
var calculator_buttons = document.querySelector(".buttons");
if (calculator_buttons != null) {
    calculator_buttons.addEventListener('click', function(event) {
        buttonClick(event.target.innerText);
    });
}

// Después
const calculatorButtons = document.querySelector('.buttons');
if (calculatorButtons !== null) {
    calculatorButtons.addEventListener('click', (event) => {
        buttonClick(event.target.innerText);
    });
}

```
