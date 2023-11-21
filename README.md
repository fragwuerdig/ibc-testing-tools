## IBC Testing Tools

Collection of tools to quickly launch two local Terra Classic chains + relayer between them and try out some ibc-related stuff.

### Requirements

- Ubuntu/Debian flavor OS (dunno about Darwin OS)
- git, build-essential, jq
- valid rust installation
- valid go v1.20 installation
- terrad installation
- hermes relayer installation

### Initalization/Usage:

- `git clone https://github.com/fragwuerdig/ibc-testing-tools`
- `cd ibc-testing-tools`
- `./setup # setup chains and relayer`
- `./start # run the setup`

### Establish IBC Transfer Channel

This initiates a channel between the first two local terra chains:

- `./create_transfer_channel`

### Deploy (Modified) Reflect Contract

This script deploys and instantiates a modified reflect contract on the second local terra chain and outputs the resulting contract address:

- `./deploy_reflect`


