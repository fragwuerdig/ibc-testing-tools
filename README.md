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

### Perform IBC ICS-20 Transfer

Do a plain IBC (ICS-20) transfer from the first to the second local chain and output balances of the receiver account before and after the transfer:

- `./ibc_transfer`

### Deploy (Modified) Reflect Contract

This script deploys and instantiates a modified reflect contract on the second local terra chain and outputs the resulting contract address:

- `./deploy_reflect`

### Perform IBC ICS-20 Transfer (With WASM Hooks)

Only possible if the local chains support WASM hooks. Perform a ICS-20 Transfer from the first to the second local chain and trigger a contract execution of the second chain (via ibc-hooks). The contract address (reflect contract) will be the receiver of the transfer and forward some of the funds to a third account. Outputs the third accounts token balance before and after the transfer:

- `./ibc_transfer_hooks <contract_address>`


