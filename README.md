# Trabajo Práctico — Bases de Datos Avanzadas · MongoDB

## Consigna general

Resolver los siguientes ejercicios en un único archivo de texto o repositorio, organizando el contenido por punto.

Todos los documentos JSON entregados deben ser **sintácticamente válidos**. Antes de realizar la entrega, verificar la validez de cada documento utilizando un validador online, como [JSONLint](https://jsonlint.com/), o mediante una extensión del editor utilizado.

---

## Ejercicio 1 — JSON mal formado: detección y corrección

El siguiente fragmento contiene varios errores de sintaxis.

```json
{
  nombre: 'Carlos Ruiz',
  "activo": True,
  "puntaje": 8.5,
  "tags": ["vip", "mayorista",],
  "ultimaCompra": 2026-01-15,
}
```

### Actividades

1. Identificar cada error encontrado.
2. Explicar brevemente por qué cada elemento hace que el documento sea inválido.
3. Reescribir el documento en una versión JSON correctamente formada.

### Entrega

* **a)** Listado de errores encontrados y justificación.
* **b)** JSON corregido.

---

## Ejercicio 2 — Modelado de una entidad simple

Diseñar un documento JSON que represente a un **estudiante de la materia Bases de Datos Avanzadas**.

El documento debe:

* Contener al menos cinco atributos.
* Utilizar obligatoriamente los seis tipos de datos JSON:

  * `string`
  * `number`
  * `boolean`
  * `null`
  * `object`
  * `array`
* Incluir al menos un atributo de tipo `array`, por ejemplo, `materiasCursadas`.
* Incluir al menos un `object` anidado, por ejemplo, `datosContacto`.
* Incluir explícitamente un valor `null`.
* Justificar en qué situación el campo que contiene `null` tendría un valor desconocido.

---

## Ejercicio 3 — Documento con anidamiento profundo

Modelar en JSON un **pedido de e-commerce (orden de compra)**.

El documento debe contener:

* Datos del cliente mediante un objeto anidado.
* Una lista de productos comprados.
* La lista de productos debe ser un `array` de objetos.
* Cada producto debe contener:

  * Nombre.
  * Cantidad.
  * Precio unitario.
* Una dirección de envío mediante un objeto anidado.
* Estado del pedido.
* Un campo `total` coherente con los productos incluidos.

El total debe calcularse a partir de las cantidades y precios unitarios de los productos.

---

## Ejercicio 4 — Array de subdocumentos: caso biblioteca

Diseñar un documento JSON que represente un **libro**.

El documento debe incluir:

* Un `array` de autores.
* Cada autor debe ser un objeto que contenga:

  * Nombre.
  * País.
* Un `array` de categorías o géneros utilizando strings simples.

### Justificación

Redactar un párrafo explicando:

* Por qué los autores fueron modelados como un `array` de objetos.
* Por qué las categorías fueron modeladas como un `array` de strings.

---

## Ejercicio 5 — Embedding vs. Referencing

Una plataforma de streaming necesita modelar **películas** y **reseñas de usuarios**.

Las condiciones del caso son:

* Cada película puede tener miles de reseñas.
* Cada reseña pertenece a un único usuario registrado.

### Actividades

Proponer dos alternativas de modelado para la relación entre **película y reseña**:

1. **Modelo embebido (Embedding).**
2. **Modelo referenciado (Referencing).**

Para cada alternativa se debe mostrar uno o más documentos JSON de ejemplo.

Además, redactar un párrafo de **al menos 5 líneas** justificando cuál de las dos alternativas se recomienda para este caso particular.

La justificación debe mencionar explícitamente:

* El volumen potencial de reseñas.
* Las ventajas y desventajas de cada alternativa.
* El riesgo del antipatrón de **"array ilimitado"**.

---

## Ejercicio 6 — Definición de un JSON Schema

Tomar como base el documento desarrollado en el **Ejercicio 3 (Orden de Compra)** y crear su correspondiente **JSON Schema**.

El esquema debe exigir como mínimo:

* Campos obligatorios mediante `required`.
* Tipos de datos correctos para cada propiedad.
* Un `enum` para el campo `estado`.

Los posibles valores de `estado` pueden ser:

```text
pendiente
pagado
enviado
entregado
cancelado
```

Además, se debe utilizar `minimum` para validar que:

* Las cantidades no sean negativas.
* Los precios no sean negativos.

---

## Ejercicio 7 — Caso integrador: modelado de un e-commerce

Diseñar el modelo de datos en JSON para una **tienda en línea simplificada**.

El modelo debe estar compuesto por tres tipos de documentos:

1. **Usuarios**
2. **Productos**
3. **Pedidos**

Para cada tipo de documento se debe:

* Mostrar un documento JSON de ejemplo válido.
* Indicar explícitamente qué relaciones fueron modeladas como **embebidas**.
* Indicar qué relaciones fueron modeladas como **referenciadas**.
* Justificar cada decisión utilizando los criterios vistos en la sección **3.5**.

### JSON Schema

Adjuntar el **JSON Schema de al menos una de las tres colecciones**:

* Usuarios
* Productos
* Pedidos

---

## Requisitos de entrega

* Todos los documentos JSON deben ser sintácticamente válidos.
* La resolución debe estar organizada por ejercicio.
* Los ejemplos deben respetar los requisitos específicos de cada punto.
* Los JSON deben ser validados antes de la entrega.
* Los ejercicios deben incluir las justificaciones solicitadas.
* El trabajo puede presentarse mediante un único archivo de texto o mediante un repositorio.

**Materia:** Bases de Datos Avanzadas
**Tema:** MongoDB

