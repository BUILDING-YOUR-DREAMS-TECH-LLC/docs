# Data Tables

## Objetivo

Crear tablas de datos estructurados que tus agentes de IA pueden consultar usando lenguaje natural. Perfecto para bases de datos de clientes, seguimiento de inventario, gestión de pedidos y más.

## Acceso

Sidebar -> Data Tables
Ruta: `/app/{tenant}/sql-tables`

## Roles con acceso

- owner, admin, agent

## Límites por plan

| Plan | Tablas | Filas máximas |
|------|--------|---------------|
| Free | 1 | 100 |
| Starter | 3 | 5,000 |
| Growth | 5 | 20,000 |
| Business | 10 | 50,000 |
| Enterprise | Ilimitadas | Ilimitadas |

---

## Crear una tabla

1. Pulsa **Create Table**
2. Completa el formulario
3. Pulsa **Create Table**

### Campos del formulario

| Campo | Obligatorio | Formato | Ejemplo | Nota |
|-------|-------------|---------|---------|------|
| Table Name (Internal) | Sí | minúsculas + _ | customer_orders | Identificador interno |
| Display Name | Sí | texto | Customer Orders | Visible en UI |
| Description | No | texto | Pedidos de clientes | Ayuda a los agentes |
| Schema | Sí | lista de campos | order_id: TEXT | Define estructura |
| Allowed Operations | Sí | selección múltiple | SELECT, INSERT | Limita operaciones |

### Tipos de campo disponibles

| Tipo | Descripción | Ejemplo |
|------|-------------|---------|
| TEXT | Texto libre | "Juan García", "ABC123" |
| NUMBER | Números enteros o decimales | 100, 99.99 |
| BOOLEAN | Verdadero/Falso | true, false |
| DATE | Solo fecha | 2024-01-15 |
| TIMESTAMP | Fecha y hora | 2024-01-15T14:30:00 |

---

## Ver y gestionar datos

Ruta: `/app/{tenant}/sql-tables/{id}`

### Funciones disponibles

- **Add Row**: Agregar un nuevo registro
- **Edit Row**: Editar un registro existente
- **Delete Row**: Eliminar un registro
- **Natural Language Query**: Consultar con IA
- **Paginación**: Navegar entre páginas de datos

### Agregar una fila (Add Row)

El formulario genera un campo por cada columna del schema.

Notas por tipo:
- **NUMBER**: Acepta números decimales (ej: 99.99)
- **BOOLEAN**: Selector Yes/No
- **DATE**: Selector de fecha
- **TIMESTAMP**: Selector de fecha y hora

---

## Consultas en Lenguaje Natural

Esta es la característica más poderosa de Data Tables. Escribe una pregunta en español o inglés y el agente la traduce a una consulta.

### Consultas que funcionan muy bien

| Tipo | Ejemplo de pregunta |
|------|---------------------|
| **Contar registros** | "¿Cuántos clientes tengo?" |
| | "How many orders are there?" |
| **Suma (SUM)** | "¿Cuál es el total de ventas?" |
| | "What is the total revenue?" |
| **Promedio (AVG)** | "¿Cuál es el valor promedio de los pedidos?" |
| | "What is the average order value?" |
| **Máximo (MAX)** | "¿Cuál es la venta más alta?" |
| | "What is the highest sale amount?" |
| **Mínimo (MIN)** | "¿Cuál es el pedido más pequeño?" |
| | "What is the minimum order?" |
| **Filtrar por valor** | "Muestra pedidos mayores a $100" |
| | "Find customers from Mexico" |
| **Filtrar por fecha** | "Pedidos de enero 2024" |
| | "Orders after January 1st, 2024" |
| **Ordenar resultados** | "Muestra los últimos 10 pedidos ordenados por fecha" |
| | "Show orders sorted by amount descending" |
| **Combinaciones** | "¿Cuál es el total de ventas de pedidos mayores a $50?" |
| | "Average price of products added this month" |

### Ejemplos prácticos por caso de uso

#### Para una tabla de Pedidos (Orders)
```
"¿Cuántos pedidos hay en total?"
"¿Cuál es el monto total de ventas?"
"Muestra los pedidos mayores a $500"
"Pedidos del último mes ordenados por fecha"
"¿Cuál es el pedido más grande?"
```

#### Para una tabla de Clientes (Customers)
```
"¿Cuántos clientes tenemos?"
"Clientes de México"
"Clientes registrados después del 1 de enero"
"Muestra los últimos 5 clientes agregados"
```

#### Para una tabla de Productos (Products)
```
"¿Cuántos productos hay?"
"¿Cuál es el precio promedio?"
"Productos con precio mayor a $100"
"Producto más caro"
"Producto más barato"
```

### Funcionalidades no soportadas (aún)

| Operación | Estado | Nota |
|-----------|--------|------|
| GROUP BY | En desarrollo | "Ventas por región" no funciona aún |
| JOIN | No soportado | No se pueden relacionar tablas |
| OR conditions | No soportado | Solo AND para combinar filtros |
| Subconsultas | No soportado | Consultas simples solamente |

### Notas técnicas

- **COUNT** funciona con cualquier cantidad de registros (precisión 100%)
- **SUM, AVG, MAX, MIN** se calculan sobre un máximo de 500 registros
- Los resultados se limitan a 100 filas por consulta
- Las fechas deben estar en formato ISO (YYYY-MM-DD)

---

## Asignar tablas a agentes

Para que un agente pueda consultar una tabla:

1. Ve a **Agents** -> selecciona el agente
2. En la sección **Tools**, activa **Data Tables**
3. Selecciona las tablas que el agente puede consultar
4. Guarda los cambios

El agente ahora podrá responder preguntas sobre esas tablas en conversaciones de chat, email o voz.

---

## Buenas prácticas

1. **Nombres descriptivos**: Usa nombres claros para tablas y campos
2. **Campos en inglés**: Mantén los nombres de campos en inglés para mejor compatibilidad
3. **Limitar operaciones**: Solo habilita INSERT/UPDATE/DELETE si es necesario
4. **Descripciones útiles**: Agrega descripciones que ayuden al agente a entender los datos
5. **Tipos correctos**: Usa NUMBER para valores numéricos, DATE para fechas

---

## Solución de problemas

### "No se encontraron resultados"
- Verifica que hay datos en la tabla
- Revisa la ortografía de los valores buscados
- Intenta una consulta más simple primero

### "Error en la consulta"
- Evita usar OR en tus preguntas
- No pidas agrupar por categoría (GROUP BY)
- Asegúrate de que los campos existen en el schema

### El agente no responde sobre la tabla
- Verifica que la tabla está asignada al agente
- Confirma que el agente tiene el tool "Data Tables" habilitado
- Revisa que "Allowed Operations" incluya SELECT

---

## Relacionados

- [03-agents.md](./03-agents.md) - Configuración de agentes
- [09-tools.md](./09-tools.md) - Herramientas disponibles

---

## Capturas sugeridas

- Vista principal de Data Tables con estadísticas
- Modal de crear tabla con schema
- Vista de tabla con datos y Natural Language Query
- Ejemplo de consulta en lenguaje natural con resultados
