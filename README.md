# docker-spruned-lightning

Basic compose to get started with [LND](https://github.com/lightningnetwork/lnd) and [Spruned](https://github.com/gdassori/spruned).

Compose directly uses [thorie7912/docker-spruned](https://github.com/thorie7912/docker-spruned)

## Getting started

```
$ git clone https://github.com/Auronmatrix/docker-spruned-lightning.git

$ cd docker-spruned-lightning

# Make shell scripts executable
$ chmod +x lncli-create.sh
$ chmod +x lncli-unlock.sh
$ chmod +x lncli-sh

$ docker-compose up -d
```

Running LND for the first time requires wallet creation.

```
$ ./lncli-create.sh
```

Whenever starting the LND node, you need to unlock the wallet

```
$ ./lncli-unlock.sh
```

## Interacting with LND

You can execute lncli commands using the `lncli.sh` script just passing your arguments.

This will execute lncli inside the lnd container.

