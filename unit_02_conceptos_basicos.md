# Unidad 02: Conceptos Básicos de Programación

## Introducción

Ahora que ya tenemos nuestro entorno de desarrollo configurado, es momento de entender algunos conceptos fundamentales antes de escribir nuestro primer código. En esta unidad aprenderemos qué son las herramientas que usaremos y escribiremos nuestro primer programa.

---

## 🔧 ¿Qué es un IDE?

**IDE** significa **Entorno de Desarrollo Integrado** (Integrated Development Environment en inglés).

**¿Qué es?** Es una aplicación que nos proporciona todas las herramientas necesarias para escribir, probar y organizar nuestro código en un solo lugar.

**¿Para qué sirve?** Un IDE como Visual Studio Code nos ayuda a:
- Escribir código con colores que nos ayudan a entenderlo mejor (sintaxis resaltada)
- Detectar errores mientras escribimos
- Autocompletar palabras y código
- Organizar nuestros archivos y carpetas
- Ejecutar nuestros programas
- Conectarse con herramientas como Git

**Analogía:** Si programar fuera como cocinar, el IDE sería una cocina completamente equipada con todos los utensilios, ingredientes organizados y recetas a mano.

---

## 💬 ¿Qué es un Lenguaje de Programación?

Un **lenguaje de programación** es una forma de comunicarnos con la computadora usando palabras y símbolos que tanto nosotros como la máquina podemos entender.

**¿Por qué JavaScript?** 
- Es uno de los lenguajes más populares del mundo
- Se puede usar tanto para páginas web como para aplicaciones
- Es relativamente fácil de aprender
- Tiene una gran comunidad que nos puede ayudar

**Analogía:** Si quisieras hablar con alguien de otro país, necesitarías aprender su idioma. JavaScript es el "idioma" que usamos para hablar con las computadoras.

---

## 📦 ¿Qué es una Variable?

Una **variable** es como una caja donde guardamos información que queremos usar después.

**Características importantes:**
- Tiene un **nombre** para identificarla
- Puede **guardar diferentes tipos de información** (números, texto, etc.)
- Podemos **cambiar** lo que contiene durante el programa
- Podemos **usar** su contenido cuando lo necesitemos

**En JavaScript escribimos variables así:**
```javascript
var nombreDeLaVariable;        // Creamos la caja
nombreDeLaVariable = 25;       // Guardamos algo dentro
```

**Analogía:** Una variable es como un cajón de tu escritorio. Puedes ponerle una etiqueta (nombre), guardar cosas dentro (valor) y cambiar el contenido cuando quieras.

---

## 💻 Ejemplo Práctico: Nuestro Primer Programa

Vamos a crear nuestro primer programa que suma dos números.

### Paso 1: Crear la carpeta de trabajo

1. **Abrir el Explorador de Windows**
2. **Ir al disco C:**
3. **Crear una nueva carpeta llamada `dev`**
4. **Dentro de `dev`, crear otra carpeta llamada `helloworld`**
   
   La ruta final debe ser: `C:\dev\helloworld`

### Paso 2: Crear el archivo main.js

1. **Abrir Visual Studio Code**
2. **Ir a File → Open Folder (o Archivo → Abrir Carpeta)**
3. **Seleccionar la carpeta `C:\dev\helloworld`**
4. **Crear un nuevo archivo:**
   - Clic derecho en el panel izquierdo
   - Seleccionar "New File" (Nuevo Archivo)
   - Nombrarlo `main.js`

5. **Escribir el siguiente código:**
```javascript
var value1;
var value2;
var result;

value1 = 67;
value2 = 40;

result = value1 + value2;

console.log( result );
```

### Paso 3: Ejecutar el programa

1. **Abrir la terminal en VSCode:**
   - Presionar `Shift + Ñ` (o ir a Terminal → New Terminal)

2. **Ejecutar el programa:**
   ```bash
   node .\main.js
   ```

3. **¡Deberías ver el resultado: `107`!**

### ¿Qué acabamos de hacer?

**Línea por línea:**
- `var value1;` - Creamos una caja llamada "value1"
- `var value2;` - Creamos una caja llamada "value2"  
- `var result;` - Creamos una caja llamada "result"
- `value1 = 67;` - Guardamos el número 67 en la primera caja
- `value2 = 40;` - Guardamos el número 40 en la segunda caja
- `result = value1 + value2;` - Sumamos lo que está en las dos cajas y guardamos el resultado en la tercera
- `console.log( result );` - Mostramos en pantalla lo que contiene la caja "result"

### ¿Qué es console.log()?

`console.log()` es una **herramienta** que nos permite mostrar información en la pantalla. Por ahora piénsalo como un "imprimir en pantalla".

- **console** = se refiere a la consola (la pantalla negra donde vemos los resultados)
- **log** = significa "registrar" o "anotar"
- **Los paréntesis ()** = aquí ponemos lo que queremos mostrar

*Nota: En la Unidad 03 veremos que console.log() es en realidad una "función", pero por ahora solo necesitas saber que sirve para mostrar cosas en pantalla.*

---

## 🏃‍♂️ Ejercicio: Calculadora de Impuestos

Ahora es tu turno. Vas a crear un programa que calcule el total de una factura aplicando impuestos.

### Requisitos:
1. Crear un archivo llamado `ejercicio02.js` en la misma carpeta
2. Usar **solo variables** (nada de funciones aún)
3. Calcular el total de una factura con IVA (21%) e Impuesto Municipal (5%)

### Lo que debe hacer tu programa:
- Tener una variable con el monto original de la factura
- Calcular el IVA (21% del monto)
- Calcular el Impuesto Municipal (5% del monto)
- Calcular el total final
- Mostrar el resultado en consola

### Pista para los cálculos:
- Para calcular el 21% de un número: `numero * 0.21`
- Para calcular el 5% de un número: `numero * 0.05`
- El total será: `monto original + IVA + Impuesto Municipal`

### Ejemplo de resultado esperado:
Si el monto original es 1000:
- IVA: 210 (1000 * 0.21)
- Impuesto Municipal: 50 (1000 * 0.05)  
- **Total: 1260**

### Para probar tu ejercicio:
```bash
node .\ejercicio02.js
```

---

## ✅ Verificación de Aprendizaje

Al completar esta unidad deberías poder:

- ✅ Explicar qué es un IDE y para qué sirve VSCode
- ✅ Entender qué es un lenguaje de programación
- ✅ Saber qué son las variables y cómo usarlas
- ✅ Crear y ejecutar programas simples en JavaScript
- ✅ Usar console.log() para mostrar resultados
- ✅ Abrir la terminal en VSCode y ejecutar archivos con Node.js

---

## 🔧 Solución de Problemas Comunes

### "node no es reconocido como comando"
- Asegúrate de haber instalado Node.js correctamente en la Unidad 01
- Reinicia VSCode
- Verifica con `node --version` en la terminal

### "No se puede encontrar el archivo"
- Verifica que estés en la carpeta correcta (`C:\dev\helloworld`)
- Asegúrate de que el archivo se llame exactamente `main.js`
- Usa `ls` (Linux/Mac) o `dir` (Windows) para ver los archivos en la carpeta

### Mi código no funciona
- Revisa que no falten punto y coma (`;`)
- Verifica que las variables estén escritas exactamente igual
- Asegúrate de que las llaves y paréntesis estén balanceados

---

## 🚀 Próximos Pasos

En la siguiente unidad aprenderemos sobre **funciones**: cómo crear bloques de código reutilizables que harán nuestros programas más organizados y potentes. También veremos diferentes tipos de datos además de números.

¡Excelente trabajo completando tu primer programa en JavaScript! 🎉