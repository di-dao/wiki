# Decentralized Services

The Sonr`x/service`module is responsible for allowing developers to seamlessly authorize user Wallet Accounts from any Internet capable source. The idea is to leverage the local key generation algorithms provided by the client device in order to form an associated relation anonymously with their Sonr Identity. This process uses Zero-knowledge accumulators and witnesses to provide an efficient solution.

# Overview of Data Types

> The following data types are commonly used between clients and nodes running the Sonr daemon.

## `ServiceRecord`

The service record is an on-chain pointer to an authorized domain on the Sonr network. This Record is used to produce the Credential Request/Creation options for a given Passkey or Local Credential.

```proto
// ServiceRecord is the balance of an account.
message ServiceRecord {
  option (cosmos.orm.v1.table) = {
    id : 1
    primary_key : {fields : "id" auto_increment : true}
    index : {id : 1 fields : "origin" unique : true}
    index : {id : 2 fields : "controller"}
  };

  uint64 id = 1;
  string origin = 2;
  string name = 3;
  string description = 4;
  string controller = 5;
  ServicePermissions permissions = 6;
}

```

## `Credential`

Credentials in the Service Module mirror the`CredentialDescriptor`struct provided by the WebAuthn implementation in order to seamlessly authorize users provided some evidence of ownership over their Identity.

```proto
// Credential is the total supply of the module.
message Credential {
  option (cosmos.orm.v1.table) = {
    id : 2
    primary_key : {fields : "id" auto_increment : true}
    index : {id : 1 fields : "handle"}
    index : {id : 2 fields : "origin,handle" unique : true}
    index : {id : 3 fields : "credential_id" unique : true}
    index : {id : 4 fields : "public_key" unique : true}
  };

  uint64 id = 1;
  string handle = 2;
  repeated string transport = 3;
  bytes public_key = 4;
  string attestation_type = 5;
  bytes credential_id = 6;
  string origin = 7;
}

```

## `Identifier`

Identifiers are Zero-knowledge witnesses which are used by ServiceRecord’s in order to keep a record of which Services have authorized which users. This primitive was created so that Services themselves would need to have the required permissions in order to access further user data.

```proto
// Identifier is a psuedo-anonomyous representation of a unique id on the Sonr blockchain. Used as
// authorizer to the underlying wallet interface.
message Identifier {
  option (cosmos.orm.v1.table) = {
    id : 3
    primary_key : {fields : "index" auto_increment : true}
    index : {id : 1 fields : "origin,key" unique : true}
  };

  uint64 index = 1;
  string origin = 2;
  string key = 3;
  string value = 4;
}

```

