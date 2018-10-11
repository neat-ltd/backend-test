
Create a distributed system.


- 3 producers

Each producer sends transaction data in parallel for client accounts (min for three different accounts with a random positive balance amount) at random intervals. Transaction vary between a payment transaction for an account and a top-up.
Each transaction should update the client account balance accordingly (minus for payments, plus for top-ups).
After each transaction log the following information: producer_id, transaction_id, amount, side, balance (after an update).



- 1 consumer

Consumer receives this data and prints to a log (for added bonus, can have a small UI where data is updated on the push) 

Enable an endpoint which starts and kills a consumer. After a kill, print all processed historical transactions and latest account balance for each account.


Ruby preferably.
Bonus points for adding a queue in-between producers and a consumer.

API Documentation as a reference: https://neat-api-docs.herokuapp.com
