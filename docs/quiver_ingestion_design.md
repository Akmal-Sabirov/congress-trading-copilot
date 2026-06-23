# Quiver Ingestion Design

## Source

Primary Source: Quiver API

## Import Process

1. Request trades from Quiver API.
2. For each trade:

   * Find person in people table.
   * If person does not exist, create person.
   * Check whether trade already exists.
   * If trade is new, insert into trades table.
   * If trade already exists, skip.

## Duplicate Detection Key

Representative + Ticker + TransactionDate + Transaction + Amount

## Future Enhancements

* Telegram alerts
* Signal generation
* Congress Score calculation
* Consensus Score calculation
* Auto-trading integration
