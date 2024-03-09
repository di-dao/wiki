# Identity System



The Sonr`x/identity`module is responsible for providing self-sovereign identity to any internet capable user in the world. The goals of its design was to provide a identity primitive that retains a privacy-preserved, fully encrypted state and can leverage the further IBC Ecosystem. The solution employs Multi-Party Computation, Zero-Knowledge Accumulators, and Decentralized Identifiers to provide a robust system of digital identity and asset management.

# Overview of Data Types

> The following data types are commonly used between clients and nodes running the Sonr daemon.

## `Account`

Accounts represent Sonr controller derived wallet accounts for users on the network. They leverage the MPC Protocol to generate new identities based off authenticated user requests over WebAuthn.

```proto
// Account is the root sonr account table which contains all sub-identities.
message Account {
  option (cosmos.orm.v1.table) = {
    id : 1
    primary_key : {fields : "sequence" auto_increment : true}
    index : {id : 1 fields : "address" unique : true}
    index : {id : 2 fields : "public_key" unique : true}
  };

  uint64 sequence = 1;
  string controller = 2;
  CoinType coin_type = 3;
  bytes public_key = 4;
  string network = 5;
  string address = 6;
  string chain_id = 7;
}

```

## `Controller`

Controllers are the root identities in the Sonr network. The represent the Account of a Sonr user and are designed to accumulate all associated identifiers anonymously with hashing.

```proto
// Controller is the root sonr controller table which contains all sub-identities.
message Controller {
  option (cosmos.orm.v1.table) = {
    id: 2
    primary_key : {fields : "sequence" auto_increment : true}
    index : {id : 1 fields : "address" unique : true}
    index : {id : 2 fields : "public_key" unique : true}
    index : {id : 3 fields : "peer_id" unique : true}
    index : {id : 4 fields : "ipns" unique : true}
  };

  uint64 sequence = 1;
  string peer_id = 2;
  string address = 3;
  bytes public_key = 4;
  string ipns = 5;
  bytes accumulator_key = 6;
  string network = 7;
  string chain_id = 8;
}

```
