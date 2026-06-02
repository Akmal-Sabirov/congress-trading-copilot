# Database Design

## people

Stores politicians and spouses.

| Column      | Type         |
| ----------- | ------------ |
| id          | SERIAL       |
| full_name   | VARCHAR(200) |
| person_type | VARCHAR(20)  |
| related_to  | VARCHAR(200) |
| chamber     | VARCHAR(20)  |
| party       | VARCHAR(20)  |
| state       | VARCHAR(10)  |
| is_active   | BOOLEAN      |
| created_at  | TIMESTAMP    |

---

## trades

Stores congressional disclosures.

| Column          | Type         |
| --------------- | ------------ |
| id              | SERIAL       |
| person_id       | INTEGER      |
| ticker          | VARCHAR(20)  |
| asset_name      | VARCHAR(200) |
| asset_type      | VARCHAR(20)  |
| trade_type      | VARCHAR(20)  |
| trade_date      | DATE         |
| disclosure_date | DATE         |
| amount_text     | VARCHAR(100) |
| amount_min      | NUMERIC      |
| amount_max      | NUMERIC      |
| source          | VARCHAR(100) |
| created_at      | TIMESTAMP    |

---

## signals

Stores generated trading signals.

| Column              | Type         |
| ------------------- | ------------ |
| id                  | SERIAL       |
| trade_id            | INTEGER      |
| congress_score      | NUMERIC      |
| consensus_score     | NUMERIC      |
| stock_score         | NUMERIC      |
| trade_quality_score | NUMERIC      |
| price_change_pct    | NUMERIC      |
| status              | VARCHAR(50)  |
| rejection_reason    | VARCHAR(100) |
| approval_status     | VARCHAR(50)  |
| created_at          | TIMESTAMP    |

---

## orders

Stores executed buy/sell orders.

| Column          | Type         |
| --------------- | ------------ |
| id              | SERIAL       |
| signal_id       | INTEGER      |
| ticker          | VARCHAR(20)  |
| side            | VARCHAR(10)  |
| quantity        | NUMERIC      |
| order_price     | NUMERIC      |
| order_status    | VARCHAR(50)  |
| broker_order_id | VARCHAR(100) |
| created_at      | TIMESTAMP    |

---

## positions

Stores current portfolio holdings.

| Column       | Type        |
| ------------ | ----------- |
| id           | SERIAL      |
| ticker       | VARCHAR(20) |
| quantity     | NUMERIC     |
| average_cost | NUMERIC     |
| opened_date  | DATE        |
| last_updated | TIMESTAMP   |
