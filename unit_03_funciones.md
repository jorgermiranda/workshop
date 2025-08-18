# Unidad 03: Funciones en JavaScript

## Introducción

En la unidad anterior aprendimos sobre variables y escribimos código que se ejecutaba línea por línea. Ahora vamos a aprender sobre **funciones**, que nos permiten organizar nuestro código en bloques reutilizables y hacer nuestros programas más eficientes y fáciles de entender.

---

## 🧩 ¿Qué es una Función?

Una **función** es un bloque de código que realiza una tarea específica y que podemos usar (llamar) las veces que queramos.

**¿Por qué son útiles las funciones?**
- **Reutilización**: Escribes el código una vez y lo usas muchas veces
- **Organización**: Divides problemas grandes en partes más pequeñas
- **Facilidad de lectura**: El código es más fácil de entender
- **Menos errores**: Si hay un error, solo lo corriges en un lugar

**Analogía:** Una función es como una receta de cocina. Una vez que escribes la receta para hacer pan, puedes usarla todas las veces que quieras hacer pan sin tener que recordar todos los pasos cada vez.

---

## 📝 Sintaxis Básica de las Funciones

### Declarar una función:
```javascript
function nombreDeLaFuncion() {
    // Código que se ejecutará cuando llamemos a la función
}
```

### Llamar (usar) una función:
```javascript
nombreDeLaFuncion(); // Esto ejecuta el código dentro de la función
```

### Ejemplo básico:
```javascript
function saludar() {
    console.log("¡Hola mundo!");
}

saludar(); // Esto imprimirá: ¡Hola mundo!
```

---

## 🔄 Funciones con Parámetros

Los **parámetros** son valores que le pasamos a la función para que trabaje con ellos.

### Sintaxis:
```javascript
function nombreDeLaFuncion(parametro1, parametro2) {
    // Usar parametro1 y parametro2 aquí
}
```

### Ejemplo:
```javascript
function sumar(numero1, numero2) {
    var resultado = numero1 + numero2;
    console.log("El resultado es: " + resultado);
}

sumar(5, 3); // Imprimirá: El resultado es: 8
sumar(10, 7); // Imprimirá: El resultado es: 17
```

---

## ↩️ Funciones que Devuelven Valores

Las funciones pueden **devolver** un resultado usando la palabra `return`:

```javascript
function multiplicar(a, b) {
    return a * b;
}

var resultado = multiplicar(4, 6);
console.log(resultado); // Imprimirá: 24
```

**¿Cuál es la diferencia?**
- **Sin return**: La función hace algo (como imprimir) pero no devuelve nada
- **Con return**: La función calcula algo y nos devuelve el resultado para usar después

---

## 💻 Ejemplo Práctico: Calculadora Modular

Vamos a crear un programa que use funciones para hacer diferentes operaciones matemáticas.

### Paso 1: Crear el archivo
Crea un nuevo archivo llamado `calculadora.js` en tu carpeta `C:\dev\helloworld`

### Paso 2: Escribir el código
```javascript
// Función para sumar dos números
function sumar(a, b) {
    return a + b;
}

// Función para restar dos números
function restar(a, b) {
    return a - b;
}

// Función para multiplicar dos números
function multiplicar(a, b) {
    return a * b;
}

// Función para dividir dos números
function dividir(a, b) {
    return a / b;
}

// Función para mostrar el resultado de una operación
function mostrarResultado(operacion, num1, num2, resultado) {
    console.log(num1 + " " + operacion + " " + num2 + " = " + resultado);
}

// Usando nuestras funciones
var numero1 = 15;
var numero2 = 3;

var suma = sumar(numero1, numero2);
var resta = restar(numero1, numero2);
var multiplicacion = multiplicar(numero1, numero2);
var division = dividir(numero1, numero2);

mostrarResultado("+", numero1, numero2, suma);
mostrarResultado("-", numero1, numero2, resta);
mostrarResultado("*", numero1, numero2, multiplicacion);
mostrarResultado("/", numero1, numero2, division);
```

### Paso 3: Ejecutar el programa
```bash
node .\calculadora.js
```

### Resultado esperado:
```
15 + 3 = 18
15 - 3 = 12
15 * 3 = 45
15 / 3 = 5
```

---

## 🔍 Entendiendo console.log()

Ahora que conoces las funciones, podemos explicar qué es realmente `console.log()`:

**`console.log()` es una función!**
- **console** es un objeto que representa la consola
- **log** es una función dentro de ese objeto
- **Los paréntesis ()** contienen los parámetros que le pasamos a la función

```javascript
console.log("Hola");           // Parámetro: texto
console.log(42);               // Parámetro: número
console.log(suma);             // Parámetro: variable
console.log("Resultado:", suma); // Múltiples parámetros
```

Es como si fuera:
```javascript
function log(mensaje) {
    // Código interno que muestra el mensaje en pantalla
}
```

---

## 🏃‍♂️ Ejercicio: Sistema de Descuentos

Crea un programa que calcule descuentos para una tienda usando funciones.

### Requisitos:
1. Crear un archivo llamado `descuentos.js`
2. Crear las siguientes funciones:

#### Funciones a crear:

**1. `calcularDescuentoEstudiante(precio)`**
- Aplica 15% de descuento
- Devuelve el precio con descuento

**2. `calcularDescuentoTerceraEdad(precio)`**  
- Aplica 20% de descuento
- Devuelve el precio con descuento

**3. `calcularDescuentoEmpleado(precio)`**
- Aplica 25% de descuento  
- Devuelve el precio con descuento

**4. `mostrarFactura(tipoCliente, precioOriginal, precioFinal)`**
- Muestra un resumen como: "Cliente: Estudiante | Precio original: $100 | Precio final: $85"

### Ejemplo de uso:
```javascript
var precioProducto = 200;

var precioEstudiante = calcularDescuentoEstudiante(precioProducto);
var precioTerceraEdad = calcularDescuentoTerceraEdad(precioProducto);
var precioEmpleado = calcularDescuentoEmpleado(precioProducto);

mostrarFactura("Estudiante", precioProducto, precioEstudiante);
mostrarFactura("Tercera Edad", precioProducto, precioTerceraEdad);
mostrarFactura("Empleado", precioProducto, precioEmpleado);
```

### Resultado esperado:
```
Cliente: Estudiante | Precio original: $200 | Precio final: $170
Cliente: Tercera Edad | Precio original: $200 | Precio final: $160
Cliente: Empleado | Precio original: $200 | Precio final: $150
```

### Pistas para los cálculos:
- Descuento 15%: `precio * 0.85` (precio menos 15%)
- Descuento 20%: `precio * 0.80` (precio menos 20%)
- Descuento 25%: `precio * 0.75` (precio menos 25%)

---

## 📚 Conceptos Importantes

### Scope (Alcance) de Variables
Las variables declaradas **dentro** de una función solo existen dentro de esa función:

```javascript
function ejemplo() {
    var variableLocal = "Solo existe aquí";
    console.log(variableLocal); // Funciona
}

ejemplo();
// console.log(variableLocal); // ¡ERROR! No existe fuera de la función
```

### Parámetros vs Argumentos
- **Parámetros**: Los nombres que usamos cuando declaramos la función
- **Argumentos**: Los valores reales que pasamos cuando llamamos la función

```javascript
function saludar(nombre) { // "nombre" es un parámetro
    console.log("Hola " + nombre);
}

saludar("Ana"); // "Ana" es un argumento
```

---

## ✅ Verificación de Aprendizaje

Al completar esta unidad deberías poder:

- ✅ Entender qué es una función y por qué son útiles
- ✅ Declarar funciones básicas
- ✅ Llamar funciones con y sin parámetros
- ✅ Crear funciones que devuelvan valores con `return`
- ✅ Entender qué es realmente `console.log()`
- ✅ Organizar código usando funciones
- ✅ Comprender el concepto básico de scope

---

## 🔧 Solución de Problemas Comunes

### "function is not defined"
- Asegúrate de declarar la función antes de llamarla
- Verifica que el nombre de la función esté escrito correctamente

### Mi función no devuelve nada
- ¿Estás usando `return`?
- ¿Estás guardando el resultado en una variable?

### Los parámetros no funcionan
- Verifica que estés pasando la cantidad correcta de argumentos
- Asegúrate de que los nombres de los parámetros sean consistentes

---

## 🚀 Próximos Pasos

En la siguiente unidad aprenderemos sobre **tipos de datos** más avanzados como strings (texto), booleanos (verdadero/falso) y arrays (listas), además de **estructuras de control** como if/else que nos permitirán hacer que nuestros programas tomen decisiones.

¡Felicitaciones por aprender a organizar tu código con funciones! 🎉