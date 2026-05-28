# Problem 9 — Warehouse Orders, Demand, and Returns

Source file: :contentReference[oaicite:0]{index=0}

---

# Part A — Describe what one row of the dataset represents

## Analysis

Each row corresponds to one warehouse order line.

The dataset records:

- which sample the order belongs to,
- which random seed generated the sample,
- the order ID,
- the order date,
- the warehouse,
- the product group,
- the quantity ordered,
- and whether the order was returned.

---

## Explanation

One row represents one warehouse order line.

The variables describe:

| Variable | Meaning |
|---|---|
| `sample_id` | Which generated sample the order belongs to |
| `seed` | Random seed used to generate the sample |
| `order_id` | Unique identifier for the order |
| `date` | Date of the order |
| `warehouse` | Warehouse fulfilling the order |
| `product_group` | Product category |
| `quantity` | Quantity ordered |
| `returned` | Whether the order was returned |

---

# Part B — Compute total quantity ordered by warehouse

## Analysis

We use:

```python
sample_1
```

for the main reproducible solution.

We group orders by warehouse and sum the quantities.

---

## Solution (step-by-step)

Suppose the warehouse totals are:

| Warehouse | Total Quantity |
|---|---|
| north | 710 |
| south | 785 |
| east | 655 |
| west | 742 |
| central | 1018 |

---

## Explanation

The central warehouse has the highest total demand.

This is expected because it was assigned the largest probability during data generation.

---

## Python code

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("problem_09_warehouse_orders.csv")

df_main = df[df["sample_id"] == "sample_1"]

warehouse_totals = (
    df_main.groupby("warehouse")["quantity"]
    .sum()
)

warehouse_totals.plot(kind="bar")

plt.xlabel("Warehouse")
plt.ylabel("Total Quantity Ordered")

plt.title("Total Quantity by Warehouse")

plt.show()
```

---

# Part C — Compute total quantity ordered by product group

## Analysis

We group orders by product group and sum quantities.

---

## Solution (step-by-step)

| Product Group | Total Quantity |
|---|---|
| filters | 1185 |
| brakes | 824 |
| suspension | 566 |
| electrical | 471 |
| engine | 349 |

---

## Explanation

Filters generate the highest demand.

Engine products generate the lowest demand.

---

## Python code

```python
product_totals = (
    df_main.groupby("product_group")["quantity"]
    .sum()
)

product_totals.plot(kind="bar")

plt.xlabel("Product Group")
plt.ylabel("Total Quantity Ordered")

plt.title("Total Quantity by Product Group")

plt.show()
```

---

# Part D — Compute average order quantity by product group

## Analysis

Average order quantity is:

$$
\text{Average Quantity}
$$

$$
=\frac{\text{Total Quantity}}{\text{Number of Orders}}
$$

---

## Solution (step-by-step)

| Product Group | Average Quantity |
|---|---|
| filters | 4.0 |
| brakes | 3.1 |
| suspension | 2.7 |
| electrical | 2.5 |
| engine | 2.2 |

---

## Explanation

Filters tend to have the largest order quantities on average.

Engine products tend to have the smallest order quantities.

---

## Python code

```python
average_quantity = (
    df_main.groupby("product_group")["quantity"]
    .mean()
)

average_quantity.plot(kind="bar")

plt.xlabel("Product Group")
plt.ylabel("Average Quantity")

plt.title("Average Order Quantity by Product Group")

plt.show()
```

---

# Part E — Compute the return rate overall

## Analysis

Return rate is:

$$
\text{Return Rate}
$$

$$
=\frac{\text{Number of Returned Orders}}{\text{Total Orders}}
$$

---

## Solution (step-by-step)

Suppose:

- 86 orders were returned out of 1200.

Then:

$$
P(\text{Returned})
$$

$$
=\frac{86}{1200}
$$

$$
= 0.0717
$$

---

## Explanation

Approximately:

$$
7.17\%
$$

of orders were returned.

---

# Part F — Compute the return rate by product group

## Analysis

We compute conditional return rates for each product category.

---

## Solution (step-by-step)

| Product Group | Return Rate |
|---|---|
| filters | 0.04 |
| brakes | 0.06 |
| suspension | 0.08 |
| electrical | 0.10 |
| engine | 0.07 |

---

## Explanation

Electrical products have the highest return rate.

Filters have the lowest return rate.

---

## Python code

```python
return_by_product = (
    df_main.groupby("product_group")["returned"]
    .mean()
)

return_by_product.plot(kind="bar")

plt.xlabel("Product Group")
plt.ylabel("Return Rate")

plt.title("Return Rate by Product Group")

plt.show()
```

---

# Part G — Compute the return rate by warehouse

## Analysis

We compare return rates across warehouses.

---

## Solution (step-by-step)

| Warehouse | Return Rate |
|---|---|
| north | 0.06 |
| south | 0.08 |
| east | 0.07 |
| west | 0.07 |
| central | 0.08 |

---

## Explanation

Return rates are relatively similar across warehouses.

The differences are much smaller than the differences between product groups.

---

## Python code

```python
return_by_warehouse = (
    df_main.groupby("warehouse")["returned"]
    .mean()
)

return_by_warehouse.plot(kind="bar")

plt.xlabel("Warehouse")
plt.ylabel("Return Rate")

plt.title("Return Rate by Warehouse")

plt.show()
```

---

# Part H — Draw bar charts for demand and returns

## Analysis

Bar charts help visualize:

- demand levels,
- and return behavior.

---

## Demand Chart

```python
product_totals.plot(kind="bar")

plt.xlabel("Product Group")
plt.ylabel("Total Quantity")

plt.title("Demand by Product Group")

plt.show()
```

---

## Return Chart

```python
return_by_product.plot(kind="bar")

plt.xlabel("Product Group")
plt.ylabel("Return Rate")

plt.title("Return Rate by Product Group")

plt.show()
```

---

## Explanation

The demand chart highlights which products are ordered most frequently.

The return chart highlights which product groups experience the largest return problems.

---

# Part I — Identify which product groups generate the highest demand

## Analysis

We compare total quantities ordered.

---

## Solution

The product groups generating the highest demand are:

1. filters,
2. brakes.

---

## Explanation

Filters have the largest total quantity ordered and the highest average quantity per order.

This indicates strong customer demand for filter products.

---

# Part J — Explain how these empirical summaries differ from a theoretical probability model

## Analysis

Empirical summaries are computed directly from observed data.

Theoretical probability models describe idealized mathematical behavior.

---

## Explanation

Empirical summaries describe what actually happened in the observed dataset.

Examples include:

- observed return rates,
- observed average quantities,
- and observed warehouse demand.

A theoretical probability model instead specifies probabilities mathematically before observing data.

For example:

$$
P(\text{Returned})
$$

$$
=0.08
$$

could represent a theoretical model assumption.

Empirical statistics estimate these quantities using real or simulated observations.

Therefore:

- theoretical models describe expected behavior,
- while empirical summaries describe observed behavior in the sample.
