# CPChain ledger app

## Overview

CPChain wallet application framework for Ledger Nano S.

## Building and installing

To build and install the app on your Ledger Nano S you must set up the Ledger Nano S build environments. Please follow the `Getting Started` instructions at [ledger official document](https://ledger.readthedocs.io/en/latest/userspace/getting_started.html).

- Compile and load the app onto the device:

```bash
make load
```

- Remove the app from the device:

```bash
make delete
```

## Examples of Ledger wallet functionality

Following packages maybe needed
```sh
sudo apt install python3-pip -y
sudo apt install libudev-dev libusb-1.0-0-dev -y
pip3 install ledgerblue cpc_fusion
pip install Pillow
```
- Test functionality:

```bash
# sign transaxtions
./examples/signTx.py --nonce 2  --gasprice 18000000000 --amount 1 --to 0x4d90553e566b67e593059f9aba02941f025578cd --txtype 0

# sign message
./examples/signMessage.py --message "testtest"
```

## Documentation

This follows the specification available in the [`api.asc`](./api.asc).
