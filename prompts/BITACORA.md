# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.

Herramienta de IA usada: ChatGPT

## Ejercicio 2: Tokens y ventana de contexto

| Texto                              | Caracteres | Tokens |
| ---------------------------------- | ---------- | ------ |
| Los estudiantes programan en Java. | 35         | 7      |
| The students program in Java.      | 29         | 6      |
| desafortunadamente                 | 18         | 4      |

En el mismo chat, la IA respondio correctamente porque los datos estaban almacenados dentro de su ventana de contexto. En el chat nuevo no supo responder ya que la ventana de contexto inicio desde cero.

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos                                 |
| ----------- | -------------- | --------------------------------------------------------- |
| 0           | 100.0%         | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec     |
| 0.5         | 69.1%          | BiblioTec, PrestaLibro, BiblioTec, LibroYa, BiblioTec     |
| 1           | 45.2%          | BiblioTec, LectoGo, PrestaLibro, LibroYa, BiblioTec       |
| 1.8         | 32.1%          | LectoGo, NubeDeTinta, PrestaLibro, BiblioTec, PaginaLibre |

Al subir la temperatura, la probabilidad se distribuye permitiendo respuestas mas variadas. El simulador nunca inventa nombres nuevos porque la temperatura solo altera la probabilidad de seleccion entre las opciones precargadas.

## Ejercicio 4: Prompt vago vs estructurado

| Criterio                            | Prompt vago | Prompt estructurado |
| ----------------------------------- | ----------- | ------------------- |
| Menciona el objetivo del sistema    | No          | Sí                  |
| Menciona a los usuarios principales | No          | Sí                  |
| Tiene exactamente 3 funcionalidades | No          | Sí                  |
| Esta en 3 parrafos                  | No          | Sí                  |
| Lo usaria en un informe real        | No          | Sí                  |

## Ejercicio 5: Anatomia de un prompt

| Componente  | Texto de mi prompt                                                         |
| ----------- | -------------------------------------------------------------------------- |
| Rol         | Actua como desarrollador Java.                                             |
| Instruccion | Usa una clase Producto con los atributos codigo, nombre, precio y stock.   |
| Contexto    | Para gestionar los productos de una tienda.                                |
| Ejemplo     | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).   |
| Formato     | Explica primero la estructura de la clase y luego presenta el codigo Java. |

## Ejercicio 6: Del prompt basico al profesional

| Qué revisar                                            | Cumple (Sí / No) |
| ------------------------------------------------------ | ---------------- |
| ¿Está escrito en Java y usa Swing?                     | Sí               |
| ¿Pide correo y contraseña?                             | Sí               |
| ¿Explica el funcionamiento antes o después del código? | Sí               |
| ¿El código está organizado en clases?                  | Sí               |
| ¿Valida los datos que ingresa el usuario?              | No               |

```text
PROMPT PROFESIONAL:
Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.

MEJORA (ITERACIÓN):
Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.
```
