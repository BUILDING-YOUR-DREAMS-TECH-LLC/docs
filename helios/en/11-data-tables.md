---
title: "Data Tables"
---

## Objective

Create structured data tables that your AI agents can query using natural language. Perfect for customer databases, inventory tracking, order management and more.

## Access

Sidebar -> Data Tables
Path: `/app/{tenant}/sql-tables`

## Roles with access

- owner, admin, agent

## Limits per plan

| Plan | Tables | Maximum rows |
|------|--------|---------------|
| Free | 1 | 100 |
| Starter | 3 | 5,000 |
| Growth | 5 | 20,000 |
| Business | 10 | 50,000 |
| Enterprise | Unlimited | Unlimited |

---

## Create a table

1. Press **Create Table**
2. Complete the form
3. Press **Create Table**

### Form fields

| Field | Mandatory | Format | Example | Note |
|-------|-------------|---------|--------|------|
| Table Name (Internal) | Yes | lowercase + _ | customer_orders | Internal identifier |
| Display Name | Yes | text | Customer Orders | Visible in UI |
| Description | No | text | Customer orders | Help agents |
| Schema | Yes | field list | order_id: TEXT | Define structure |
| Allowed Operations | Yes | multiple selection | SELECT, INSERT | Limit operations |

### Available field types

| Type | Description | Example |
|------|-------------|---------|
| TEXT | Free text | "Juan García", "ABC123" |
| NUMBER | Whole numbers or decimals | 100, 99.99 |
| BOOLEAN | True/False | true, false |
| DATE | Date only | 2024-01-15 |
| TIMESTAMP | Date and time | 2024-01-15T14:30:00 |

---

## View and manage data

Path: `/app/{tenant}/sql-tables/{id}`

### Available Features

- **Add Row**: Add a new record
- **Edit Row**: Edit an existing record
- **Delete Row**: Delete a record
- **Natural Language Query**: Query with AI
- **Pagination**: Navigate between data pages

### Add a row (Add Row)

The form generates a field for each column of the schema.

Notes by type:
- **NUMBER**: Accepts decimal numbers (ex: 99.99)
- **BOOLEAN**: Yes/No selector
- **DATE**: Date picker
- **TIMESTAMP**: Date and time selector

---

## Consultations in Natural Language

This is the most powerful feature of Data Tables. Write a question in Spanish or English and the agent translates it into a query.

### Queries that work very well

| Type | Sample question |
|------|----------|
| **Count records** | "How many clients do I have?" |
| | "How many orders are there?" |
| **Sum (SUM)** | "What is the total sales?" |
| | "What is the total revenue?" |
| **Average (AVG)** | "What is the average order value?" |
| | "What is the average order value?" |
| **Maximum (MAX)** | "What is the highest sale?" |
| | "What is the highest sale amount?" |
| **Minimum (MIN)** | "What is the smallest order?" |
| | "What is the minimum order?" |
| **Filter by value** | "Show orders over $100" |
| | "Find customers from Mexico" |
| **Filter by date** | "Orders for January 2024" |
| | "Orders after January 1st, 2024" |
| **Sort results** | "Shows the last 10 orders ordered by date" |
| | "Show orders sorted by amount descending" |
| **Combinations** | "What is the total sales for orders over $50?" |
| | "Average price of products added this month" |

### Practical examples per use case

#### For an Orders table
```
"¿Cuántos pedidos hay en total?"
"¿Cuál es el monto total de ventas?"
"Muestra los pedidos mayores a $500"
"Pedidos del último mes ordenados por fecha"
"¿Cuál es el pedido más grande?"
```

#### For a Customers table
```
"¿Cuántos clientes tenemos?"
"Clientes de México"
"Clientes registrados después del 1 de enero"
"Muestra los últimos 5 clientes agregados"
```

#### For a Products table
```
"¿Cuántos productos hay?"
"¿Cuál es el precio promedio?"
"Productos con precio mayor a $100"
"Producto más caro"
"Producto más barato"
```### Features not supported (yet)

| Operation | Status | Note |
|-----------|--------|------|
| GROUP BY | In development | "Sales by region" does not work yet |
| JOIN | Not supported | Tables cannot be related |
| OR conditions | Not supported | Just AND to combine filters |
| Subqueries | Not supported | Simple queries only |

### Technical notes

- **COUNT** works with any number of records (100% accuracy)
- **SUM, AVG, MAX, MIN** are calculated on a maximum of 500 records
- Results are limited to 100 rows per query
- Dates must be in ISO format (YYYY-MM-DD)

---

## Assign tables to agents

For an agent to query a table:

1. Go to **Agents** -> select the agent
2. In the **Tools** section, activate **Data Tables**
3. Select the tables that the agent can query
4. Save changes

The agent will now be able to answer questions about those tables in chat, email, or voice conversations.

---

## Good practices

1. **Descriptive names**: Use clear names for tables and fields
2. **Fields in English**: Keep field names in English for better compatibility
3. **Limit operations**: Only enable INSERT/UPDATE/DELETE if necessary
4. **Useful descriptions**: Add descriptions that help the agent understand the data
5. **Correct Types**: Use NUMBER for numeric values, DATE for dates

---

## Troubleshooting

### "No results found"
- Verify that there is data in the table
- Check the spelling of the searched values
- Try a simpler query first

### "Query failed"
- Avoid using OR in your questions
- Do not ask to group by category (GROUP BY)
- Make sure the fields exist in the schema

### The agent does not respond about the table
- Verify that the table is assigned to the agent
- Confirm that the agent has the "Data Tables" tool enabled
- Check that "Allowed Operations" includes SELECT

---

## Related

- [03-agents.md](./03-agents.md) - Agent configuration
- [09-tools.md](./09-tools.md) - Available tools

---

## Suggested screenshots

### Main View
![Main View](../../images/helios/en/data-tables/datatables-main-stats.png)

### Create Table
![Create Table](../../images/helios/en/data-tables/datatables-create-modal.png)

### Table Data View
![Table Data View](../../images/helios/en/data-tables/datatables-view-data.png)

### Natural Language Query
![Natural Language Query](../../images/helios/en/data-tables/datatables-nl-query.png)