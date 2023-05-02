# Monero DAppNode package

[![DAppNodeStore Available](https://img.shields.io/badge/DAppNodeStore-Available-brightgreen.svg)](http://my.admin.dnp.dappnode.eth/#/installer/monero.dnp.dappnode.eth)

[![Website dappnode.io](https://img.shields.io/badge/Website-dappnode.io-brightgreen.svg)](https://dappnode.io/)
[![Documentation Wiki](https://img.shields.io/badge/Documentation-Wiki-brightgreen.svg)](https://github.com/dappnode/DAppNode/wiki)
[![GIVETH Campaign](https://img.shields.io/badge/GIVETH-Campaign-1e083c.svg)](https://beta.giveth.io/campaigns/5b44b198647f33526e67c262)
[![Twitter Follow](https://img.shields.io/twitter/follow/espadrine.svg?style=social&label=Follow)](https://twitter.com/DAppNode?lang=es)

A Private Digital Currency
Monero is cash for a connected world. It’s fast, private, and secure. With Monero, you are your own bank. You can spend safely, knowing that others cannot see your balances or track your activity.

You can use your own monero node and connect it to [monero gui wallet](https://web.getmonero.org/downloads/#gui) to execute transactions untraceble, privately, safely and much more.

monerod is the daemon software that ships with the Monero tree. It is a console program, and manages the blockchain.

Dappnode package responsible for providing the monero chain ( based on monero v0.17.1.9)

Aragon Package Manager Repo at [0xe8332e80951c3020a5a8e529df01c12aa87f482f ](https://etherscan.io/address/0xe8332e80951c3020a5a8e529df01c12aa87f482f)

You can use this package without installing it in your DAppNode following these instructions:

## Prerequisites

- git

  Install [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) commandline tool.

- docker

  Install [docker](https://docs.docker.com/engine/installation). The community edition (docker-ce) will work. In Linux make sure you grant permissions to the current user to use docker by adding current user to docker group, `sudo usermod -aG docker $USER`. Once you update the users group, exit from the current terminal and open a new one to make effect.

- docker-compose

  Install [docker-compose](https://docs.docker.com/compose/install)

**Note**: Make sure you can run `git`, `docker ps`, `docker-compose` without any issue and without sudo command.

## Building

`docker-compose build`

## Running

### Start

`docker-compose up -d`

### View logs

`docker-compose logs -f`

### Stop

`docker-compose down`

## Connect using monero gui

address: http://monero.dappnode
port: 18081

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details
