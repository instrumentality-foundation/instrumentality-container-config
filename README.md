# Instrumentality examples

It contains: docker-compose file, genesis block, docker config for iroha, 
ed25519/sha3 keys compatible with iroha, example of private configs for python API

**DO NOT USE THOSE VALUES IN PRODUCTION!!!**

## How to start the containers

0. Have docker and docker-compose installed and functional.
1. Clone this repo.
2. `cd instrumentality-container-config`
3. `docker-compose -f docker-orchestra.yaml up`

## Batteries included

Inside you'll find:

- **Sonata:** The landing site of Instrumentality: running on [localhost:8080](http://localhost:8080)
- **Overture:** The main app (aka. Instrumentality): running on [localhost:8000](http://localhost:8000)
- **Minuet:** The Python(Flask) API responsible for communicating with the Iroha ledger: running on [localhost:9000](http://localhost:9000)
- **Scherzo:** A PostgreSQL database used by Iroha to store data. Communicates only with **Minuet** and **Rondo**
- **Rondo:** The Hyperledger Iroha distributed ledger. Communicates only with **Minuet** and **Scherzo**.

## Instrumentality containers

The first three services are Instrumentality containers and their Dockerfiles are available here:

- **Sonata -- [Dockerfile](https://codeberg.org/instrumentality-foundation/instrumentality-landing-perf/src/branch/master/Dockerfile)**
- **Overture -- [Dockerfile](https://codeberg.org/instrumentality-foundation/instrumentality/src/branch/master/Dockerfile)**
- **Minuet -- [Dockerfile](https://codeberg.org/instrumentality-foundation/instrumentality-blockchain-api/src/branch/master/Dockerfile)**