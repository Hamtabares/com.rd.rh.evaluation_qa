# Instrucciones para los Candidatos

## Pasos a seguir:
1. Clonar el repositorio.
2. Crear una nueva rama con el formato `feature/nombre_apellido`.
3. Implementar la solución utilizando **Karate**.
4. Realizar commits con mensajes claros y descriptivos.
5. Subir la rama y crear un **Pull Request**.

⚠ **Nota importante:** No se permite modificar la rama principal directamente.

---

## 🎯 Objetivo del Ejercicio
Automatizar pruebas funcionales del endpoint `https://jsonplaceholder.typicode.com/comments` validando los siguientes aspectos:

1. **Contrato**
2. **Integridad de datos**
3. **Consistencia**
4. **Buenas prácticas de diseño en Karate**

---

## 📋 Requerimientos Técnicos

### 🔹 1. Validación Básica
- Verificar que el **status code** sea `200`.
- Asegurarse de que el **tiempo de respuesta** sea menor a **2 segundos**.
- Validar que el array contenga exactamente **500 registros**.

### 🔹 2. Validación de Estructura
Validar que cada elemento del array cumpla con la siguiente estructura:
- `postId` (número)
- `id` (número)
- `name` (cadena de texto)
- `email` (cadena de texto válida como correo electrónico)
- `body` (cadena de texto no vacía)

> **Nota:** Usar `match each` en Karate para evitar validaciones repetitivas.

### 🔹 3. Validaciones de Negocio Simuladas
Validar que:
- No existan **IDs duplicados**.
- Todos los **emails** contengan el carácter `"@"`.
- No existan **campos null**.
- No existan **IDs negativos**.

### 🔹 4. Validación por Filtro
Consumir el endpoint: /comments?postId=1

- Todos los resultados tengan `postId = 1`.
- El número de resultados sea correcto.
- La estructura de los datos se mantenga.


¡Buena suerte con el ejercicio! 🚀