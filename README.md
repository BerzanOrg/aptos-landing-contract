# aptos-landing-contract
Move module for Aptos Landing dApp.


## Setup a development environment
You can use [`Dev Containers`](https://code.visualstudio.com/docs/devcontainers/containers) to setup a development environment.

## Initialize an Aptos account
Run the command below to initialize an Aptos account. 

It will create `.aptos/config.yaml` file.
```sh
aptos init
```

## Change the address
Copy the address for `account` in `.aptos/config.yaml` file.

In `Move.toml` file, change `aptos_landing_contract` under `[addresses]` to the address you copied.

## Publish
Run the command below to publish the module on Aptos Devnet.
```sh
aptos move publish
```

## Interact
You can run the command below to setup a page for yourself.

```sh
aptos move run --function-id <address-you-copied>::landing::setup_page --args '<name>' '<website>' '<twitter>' '<facebook>' '<instagram>' '<youtube>' '<tiktok>'
```

Don't forget to include the types for each argument like `string:foobar`.


## See the resources
You can run the command below to see the resources.
```sh 
aptos account list
```