# Tarea: Mi prompt profesional

## Funcionalidad elegida

Sistema de control de inventario y stock de productos en Java Swing.

## Version 1: prompt basico

```text
Hazme un sistema de inventario en Java.
```

Qué cambié: Solicitud inicial sin especificar el tipo de interfaz, datos a registrar ni restricciones de diseño.

Qué mejoró en la respuesta: La IA entrego un codigo simple en consola utilizando listas en memoria.

## Version 2

```text
Actua como desarrollador Java. Crea un programa con interfaz grafica Swing para registrar productos con su codigo, nombre, precio y stock disponible.
```

Qué cambié: Asigne un rol claro de desarrollador Java y defini la interfaz grafica Swing junto a los campos de entrada requeridos.

Qué mejoró en la respuesta: La IA diseño un formulario basico en Swing con cajas de texto y un boton para registrar datos.

## Version 3: prompt final

```text
Actua como desarrollador Java experto en aplicaciones de escritorio. Diseña un sistema de control de inventario en Java Swing para registrar productos en una tienda.

Requisitos del formulario:
- Campos: Codigo del producto, Nombre, Precio unitario y Stock inicial.
- Boton: 'Agregar Producto' que valide los campos e ingrese el registro.

Restricciones: No uses librerias externas, no agregues estilos CSS, valida que el precio y el stock sean numeros positivos mayores a cero, y muestra las alertas de confirmacion o error con JOptionPane.

Ejemplo de salida esperada:
Producto registrado: Laptop Lenovo | Precio: S/. 2500.00 | Stock: 10 unidades

Formato: Explica brevemente la estructura de clases utilizada antes de presentar el bloque de codigo en Java.
```

Qué cambié: Agregue los 5 componentes del prompt (rol, instruccion, contexto, ejemplo y formato) sumados a reglas estrictas de validacion de datos y manejo de alertas.

Qué mejoró en la respuesta: La IA genero una clase Java Swing completa con validacion numerica, manejo de excepciones de formato y alertas emergentes mediante JOptionPane sin librerias adicionales.

## Componentes del prompt final

| Componente  | Texto de mi prompt                                                                 |
| ----------- | ---------------------------------------------------------------------------------- |
| Rol         | Actua como desarrollador Java experto en aplicaciones de escritorio.               |
| Instruccion | Diseña un sistema de control de inventario en Java Swing para registrar productos. |
| Contexto    | Registro de codigo, nombre, precio y stock para una tienda comercial.              |
| Ejemplo     | Producto registrado: Laptop Lenovo \| Precio: S/. 2500.00 \| Stock: 10 unidades    |
| Formato     | Explica la estructura de clases antes de entregar el codigo Java.                  |

## Evaluacion del resultado

| Criterio                                           | Cumple (Sí / No) |
| -------------------------------------------------- | ---------------- |
| ¿Usa Java Swing sin librerias ni CSS?              | Sí               |
| ¿Valida que el precio y stock sean mayores a cero? | Sí               |
| ¿Muestra los mensajes con JOptionPane?             | Sí               |
| ¿Entrega la explicacion antes del codigo?          | Sí               |

## Errores que evite

1. **Omitir tipos de datos y validaciones:** Lo evite especificando que precio y stock deben ser numericos y positivos para evitar errores de ejecucion.
2. **Generacion de librerias de terceros:** Lo evite restringiendo el uso a componentes nativos de Java Swing y JOptionPane.
