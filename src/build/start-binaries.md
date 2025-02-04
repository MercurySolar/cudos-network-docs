---
title: Start the pre-built Binaries
---

## Start and build binaries

You can build and start the docker image that has already been built and contains the Cudos binary by following these steps (skip the steps 1,2, and 3 if you have [setup your environment](/build/prerequisites.html) before):
1. Create a directory to use as your workspace
```
mkdir ~/cudos
cd ~/cudos
```
2. Make sure that you are in the correct directory (cudos directory in this example)
3. Clone the correct branches from the [CudosNode](https://github.com/CudoVentures/cudos-node), [CudosBuilders](https://github.com/CudoVentures/cudos-builders), and [CudosGravityBridge](https://github.com/CudoVentures/cosmos-gravity-bridge) repositories with renaming the folders accordingly to exactly _CudosNode_, _CudosBuilders_, and _CudosGravityBridge_:
```
git clone --depth 1 --branch v0.3 https://github.com/CudoVentures/cudos-node.git CudosNode
git clone --depth 1 --branch v0.3.2  https://github.com/CudoVentures/cudos-builders.git CudosBuilders
git clone --depth 1 --branch v0.3 https://github.com/CudoVentures/cosmos-gravity-bridge.git CudosGravityBridge
```
4. Navigate to the directory _CudosBuilders/docker/binary-builder_ directory
5. Build and start the binaries by running this command:
```
sudo docker-compose --env-file binary-builder.arg -f binary-builder.yml -p cudos-binary-builder up --build --detach
```
6. If you would like to start the docker image that has already been built and contains the cudos binary then run the following command:
```
sudo docker-compose --env-file binary-builder.arg -f binary-builder.yml -p cudos-binary-builder up
```
