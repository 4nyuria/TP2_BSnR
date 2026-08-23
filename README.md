Resuelva los siguientes ejercicios en un único archivo de texto (o repositorio) organizado por punto. Cada
documento JSON entregado debe ser sintácticamente válido: verifique su validez con un validador online (por
ejemplo jsonlint.com) o con la extensión de su editor antes de entregar.

Ejercicio 1 — JSON mal formado — detección y corrección
El siguiente fragmento contiene varios errores de sintaxis. Identifique cada error, explique por qué es inválido y
reescriba una versión corregida.

{
 nombre: 'Carlos Ruiz',
 "activo": True,
 "puntaje": 8.5,
 "tags": ["vip", "mayorista",],
 "ultimaCompra": 2026-01-15,
}

Entregue: (a) el listado de errores encontrados con una breve justificación de cada uno, y (b) el JSON corregido.

Ejercicio 2 — Modelado de una entidad simple
Diseñe un documento JSON para representar un "estudiante" de la materia Bases de Datos Avanzadas, utilizando
al menos cinco atributos y empleando obligatoriamente los seis tipos de datos JSON (string, number, boolean,
null, object, array) en algún punto del documento.
• Incluya un atributo de tipo array (por ejemplo, materias cursadas).
• Incluya un atributo de tipo object anidado (por ejemplo, datos de contacto).
• Incluya explícitamente un valor null justificando en qué caso ese campo sería desconocido.

Ejercicio 3 — Documento con anidamiento profundo
Modele un pedido de e-commerce ("orden de compra") que contenga: datos del cliente (anidado), una lista de
productos comprados (array de objetos, cada uno con nombre, cantidad y precio unitario), una dirección de envío
(objeto anidado) y el estado del pedido. Calcule y agregue un campo total coherente con los ítems.

Ejercicio 4 — Array de subdocumentos — caso biblioteca
Diseñe el documento JSON de un "libro" que incluya un array de autores (cada autor con nombre y país) y un array
de categorías/géneros (strings simples). Justifique en un párrafo por qué los autores se modelaron como array de
objetos y las categorías como array de strings.

Ejercicio 5 — Embedding vs. referencing
Se le presenta el siguiente caso: una plataforma de streaming necesita modelar "películas" y "reseñas de usuarios".
Cada película puede tener miles de reseñas, y cada reseña pertenece a un único usuario registrado.
Proponga dos alternativas de modelado (una embebida y otra referenciada) para la relación película–reseña,
mostrando el/los documento(s) JSON de ejemplo de cada alternativa. Redacte además un párrafo de al menos 5
líneas justificando cuál de las dos alternativas recomendaría para este caso puntual y por qué, mencionando
explícitamente el riesgo del antipatrón de "array ilimitado".

Ejercicio 6 — Definición de un JSON Schema
Tome el documento que diseñó en el Ejercicio 3 (orden de compra) y escriba su JSON Schema correspondiente. El
esquema debe exigir como mínimo: campos obligatorios (required), tipos de dato correctos para cada propiedad,
un enum para el campo estado (por ejemplo: "pendiente", "pagado", "enviado", "entregado", "cancelado"), y una
validación de mínimo (minimum) para las cantidades y precios (no pueden ser negativos).
Bases de Datos Avanzadas · MongoDB

Ejercicio 7 — Caso integrador — modelado de un e-commerce
Diseñe el modelo de datos en JSON para una tienda en línea simplificada, compuesto por tres tipos de
documentos: usuarios, productos y pedidos. Para cada uno:
• Muestre un documento de ejemplo válido.
• Indique explícitamente qué relaciones modeló como embebidas y cuáles como referenciadas, y justifique
cada decisión con el criterio visto en la sección 3.5.
• Adjunte el JSON Schema de al menos una de las tres colecciones.
