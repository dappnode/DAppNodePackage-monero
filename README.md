# Monero DAppNode package

[![DAppNodeStore Available](https://img.shields.io/badge/DAppNodeStore-Available-brightgreen.svg)](http://my.admin.dnp.dappnode.eth/#/installer/monero.dnp.dappnode.eth)

[![Website dappnode.io](https://img.shields.io/badge/Website-dappnode.io-brightgreen.svg)](https://dappnode.io/)
[![Documentation Wiki](https://img.shields.io/badge/Documentation-Wiki-brightgreen.svg)](https://github.com/dappnode/DAppNode/wiki)
[![GIVETH Campaign](https://img.shields.io/badge/GIVETH-Campaign-1e083c.svg)](https://beta.giveth.io/campaigns/5b44b198647f33526e67c262)
[![ELEMENT DAppNode](https://img.shields.io/badge/ELEMENT-DAppNode-blue.svg)](https://app.element.io/#/room/#DAppNode:matrix.org)
[![Twitter Follow](https://img.shields.io/twitter/follow/espadrine.svg?style=social&label=Follow)](https://twitter.com/DAppNode?lang=es)

monerod is the daemon software that ships with the Monero tree. It is a console program, and manages the blockchain.

Dappnode package responsible for providing the monero chain ( based on monero v0.15.0.0)

Aragon Package Manager Repo at [0xe8332e80951c3020a5a8e529df01c12aa87f482f ](https://etherscan.io/address/0xe8332e80951c3020a5a8e529df01c12aa87f482f )

ou can use this package without installing it in your DAppNode following these instructions:

## Prerequisites

- git

   Install [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) commandline tool.

- docker

   Install [docker](https://docs.docker.com/engine/installation). The community edition (docker-ce) will work. In Linux make sure you grant permissions to the current user to use docker by adding current user to docker group, `sudo usermod -aG docker $USER`. Once you update the users group, exit from the current terminal and open a new one to make effect.

- docker-compose

   Install [docker-compose](https://docs.docker.com/compose/install)
   
**Note**: Make sure you can run `git`, `docker ps`, `docker-compose` without any issue and without sudo command.


## Buidling

`docker-compose build`

## Running

### Start

`docker-compose up -d`

### View logs

`docker-compose logs -f`

### Stop

`docker-compose down`

## Connect using monero gui

address: my.monero.dnp.dappnode.eth 
port:    18081

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details
