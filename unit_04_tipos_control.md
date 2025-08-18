# Unidad 04: Tipos de Datos y Estructuras de Control

## Introducción

Hasta ahora hemos trabajado principalmente con números y hemos visto que nuestros programas se ejecutan línea por línea. En esta unidad aprenderemos sobre diferentes tipos de información que podemos manejar y cómo hacer que nuestros programas tomen decisiones automáticamente.

---

## 📊 Tipos de Datos en JavaScript

### 1. **Number (Números)**
Ya los hemos usado. Incluyen enteros y decimales:
```javascript
var edad = 25;
var precio = 19.99;
var temperatura = -5;
```

### 2. **String (Cadenas de Texto)**
Representan texto y van entre comillas:
```javascript
var nombre = "María";
var apellido = 'González';
var mensaje = "Hola, ¿cómo estás?";
```

**Operaciones con strings:**
```javascript
var nombre = "Juan";
var apellido = "Pérez";
var nombreCompleto = nombre + " " + apellido; // "Juan Pérez"

var saludo = "Hola " + nombre; // "Hola Juan"
```

### 3. **Boolean (Verdadero o Falso)**
Solo pueden tener dos valores: `true` o `false`
```javascript
var esMayorDeEdad = true;
var estaLloviendo = false;
var tieneDescuento = true;
```

### 4. **Array (Arreglos/Listas)**
Permiten guardar múltiples valores en una sola variable:
```javascript
var numeros = [1, 2, 3, 4, 5];
var nombres = ["Ana", "Luis", "Carmen"];
var mixto = [25, "Juan", true];
```

**Acceder a elementos del array:**
```javascript
var frutas = ["manzana", "banana", "naranja"];
console.log(frutas[0]); // "manzana" (el primer elemento es índice 0)
console.log(frutas[1]); // "banana"
console.log(frutas[2]); // "naranja"
```

---

## ⚖️ Operadores de Comparación

Estos operadores nos permiten comparar valores:

| Operador | Significado | Ejemplo |
|----------|-------------|---------|
| `==` | Igual a | `5 == 5` → `true` |
| `!=` | Diferente a | `5 != 3` → `true` |
| `<` | Menor que | `3 < 5` → `true` |
| `>` | Mayor que | `8 > 4` → `true` |
| `<=` | Menor o igual | `5 <= 5` → `true` |
| `>=` | Mayor o igual | `7 >= 3` → `true` |

```javascript
var edad = 18;
var esMayorDeEdad = edad >= 18; // true
var esNiño = edad < 13; // false
```

---

## 🔗 Operadores Lógicos

Nos permiten combinar condiciones:

| Operador | Significado | Ejemplo |
|----------|-------------|---------|
| `&&` | Y (and) | `true && true` → `true` |
| `\|\|` | O (or) | `true \|\| false` → `true` |
| `!` | No (not) | `!true` → `false` |

```javascript
var edad = 20;
var tienePermiso = true;

var puedeConducir = edad >= 18 && tienePermiso; // true
var necesitaAyuda = edad < 16 || edad > 65; // false
var noEsAdulto = !(edad >= 18); // false
```

---

## 🤔 Estructuras de Control: if/else

La estructura `if/else` nos permite que el programa tome decisiones:

### Sintaxis básica:
```javascript
if (condicion) {
    // Código que se ejecuta si la condición es verdadera
} else {
    // Código que se ejecuta si la condición es falsa
}
```

### Ejemplo simple:
```javascript
var edad = 17;

if (edad >= 18) {
    console.log("Eres mayor de edad");
} else {
    console.log("Eres menor de edad");
}
// Resultado: "Eres menor de edad"
```

### Múltiples condiciones con else if:
```javascript
var nota = 85;

if (nota >= 90) {
    console.log("Excelente - A");
} else if (nota >= 80) {
    console.log("Muy bien - B");
} else if (nota >= 70) {
    console.log("Bien - C");
} else if (nota >= 60) {
    console.log("Suficiente - D");
} else {
    console.log("Insuficiente - F");
}
// Resultado: "Muy bien - B"
```

---

## 💻 Ejemplo Práctico: Sistema de Calificaciones

Vamos a crear un sistema que evalúe calificaciones de estudiantes.

### Crear el archivo `calificaciones.js`

```javascript
// Función para convertir nota numérica a letra
function obtenerLetra(nota) {
    if (nota >= 90) {
        return "A";
    } else if (nota >= 80) {
        return "B";
    } else if (nota >= 70) {
        return "C";
    } else if (nota >= 60) {
        return "D";
    } else {
        return "F";
    }
}

// Función para determinar si aprobó
function estaAprobado(nota) {
    return nota >= 60;
}

// Función para mostrar el resultado completo
function mostrarResultado(nombre, nota) {
    var letra = obtenerLetra(nota);
    var aprobado = estaAprobado(nota);
    var estado = aprobado ? "APROBADO" : "REPROBADO";
    
    console.log("=== REPORTE DE CALIFICACIÓN ===");
    console.log("Estudiante: " + nombre);
    console.log("Nota numérica: " + nota);
    console.log("Letra: " + letra);
    console.log("Estado: " + estado);
    console.log("==============================");
}

// Función para procesar múltiples estudiantes
function procesarCalificaciones(estudiantes, notas) {
    for (var i = 0; i < estudiantes.length; i++) {
        mostrarResultado(estudiantes[i], notas[i]);
    }
}

// Datos de ejemplo
var estudiantes = ["Ana", "Carlos", "María", "Pedro"];
var notas = [95, 67, 78, 45];

// Procesar todos los estudiantes
procesarCalificaciones(estudiantes, notas);

// Ejemplo individual
console.log("\n--- Ejemplo individual ---");
var nombreEstudiante = "Luis";
var notaEstudiante = 88;
mostrarResultado(nombreEstudiante, notaEstudiante);
```

### Ejecutar el programa:
```bash
node .\calificaciones.js
```

### Resultado esperado:
```
=== REPORTE DE CALIFICACIÓN ===
Estudiante: Ana
Nota numérica: 95
Letra: A
Estado: APROBADO
==============================
=== REPORTE DE CALIFICACIÓN ===
Estudiante: Carlos
Nota numérica: 67
Letra: D
Estado: APROBADO
==============================
...
```

---

## 🎬 Ejercicio: Sistema de Recomendación de Películas

Crea un sistema que recomiende películas basándose en la edad y género preferido del usuario.

### Requisitos:
1. Crear un archivo llamado `peliculas.js`
2. Crear las siguientes funciones:

#### Arrays de películas (úsalos en tu código):
```javascript
var peliculasAccion = ["John Wick", "Mad Max", "Avengers", "Fast & Furious"];
var peliculasComedia = ["Toy Story", "El Rey León", "Shrek", "Mi Villano Favorito"];
var peliculasDrama = ["Titanic", "Forrest Gump", "El Padrino", "Gladiator"];
var peliculasHorror = ["Halloween", "El Exorcista", "Scream", "It"];
```

#### Funciones a implementar:

**1. `esAptoParaHorror(edad)`**
- Return `true` si la edad es mayor o igual a 16
- Return `false` en caso contrario

**2. `obtenerRecomendacion(edad, genero)`**
- Si el género es "horror" y no es apto para horror, recomendar comedias
- Si el género es "accion" y la edad es menor a 13, recomendar comedias
- Para cualquier otro caso (incluyendo "drama" y "comedia"), recomendar el género solicitado
- Return el array de películas correspondiente

**3. `mostrarRecomendaciones(nombre, edad, genero)`**
- Obtener las recomendaciones usando la función anterior
- Mostrar un mensaje personalizado con las recomendaciones
- Formato: "Hola [nombre], basado en tu edad ([edad]) y preferencia ([genero]), te recomendamos:"

### Ejemplo de uso esperado:
```javascript
// Casos de prueba
mostrarRecomendaciones("Ana", 25, "accion");
mostrarRecomendaciones("Pedro", 12, "horror");
mostrarRecomendaciones("María", 30, "drama");
mostrarRecomendaciones("Luis", 10, "accion");
```

### Resultado esperado:
```
Hola Ana, basado en tu edad (25) y preferencia (accion), te recomendamos:
- John Wick
- Mad Max
- Avengers
- Fast & Furious

Hola Pedro, basado en tu edad (12) y preferencia (horror), te recomendamos:
- Toy Story
- El Rey León
- Shrek
- Mi Villano Favorito

...
```

### Pistas:
- Si `genero` es "horror" y `!esAptoParaHorror(edad)`, devolver `peliculasComedia`
- Si `genero` es "accion" y `edad < 13`, devolver `peliculasComedia`
- Si `genero` es "comedia", devolver `peliculasComedia`
- Si `genero` es "drama", devolver `peliculasDrama`
- Si `genero` es "horror" y edad >= 16, devolver `peliculasHorror`
- Si `genero` es "accion" y edad >= 13, devolver `peliculasAccion`
- Usa un bucle `for` para mostrar cada película del array

---

## 📚 Conceptos Importantes

### El operador ternario
Una forma corta de escribir if/else:
```javascript
var resultado = condicion ? "si es verdadero" : "si es falso";

// Es equivalente a:
var resultado;
if (condicion) {
    resultado = "si es verdadero";
} else {
    resultado = "si es falso";
}
```

### Longitud de arrays
```javascript
var frutas = ["manzana", "banana", "naranja"];
console.log(frutas.length); // 3
```

### Bucle for básico
```javascript
var numeros = [1, 2, 3, 4, 5];

for (var i = 0; i < numeros.length; i++) {
    console.log(numeros[i]);
}
```

---

## ✅ Verificación de Aprendizaje

Al completar esta unidad deberías poder:

- ✅ Trabajar con diferentes tipos de datos (number, string, boolean, array)
- ✅ Usar operadores de comparación y lógicos
- ✅ Implementar estructuras de control if/else
- ✅ Acceder y manipular elementos de arrays
- ✅ Combinar condiciones complejas
- ✅ Crear programas que tomen decisiones automáticamente

---

## 🔧 Solución de Problemas Comunes

### "Cannot read property of undefined"
- Verifica que estés accediendo a un índice válido del array
- Los arrays empiezan en índice 0

### Mi condición if nunca se ejecuta
- Revisa los operadores de comparación
- Asegúrate de usar `==` para comparar, no `=` (que es asignación)

### Las condiciones lógicas no funcionan
- Recuerda que `&&` requiere que ambas condiciones sean verdaderas
- `||` solo requiere que una de las dos sea verdadera

---

## 🚀 Próximos Pasos

En la siguiente unidad aprenderemos sobre **bucles** (while, for) que nos permitirán repetir código automáticamente, y profundizaremos en la **manipulación de arrays** con métodos más avanzados.

¡Excelente trabajo aprendiendo a hacer que tus programas tomen decisiones! 🎉