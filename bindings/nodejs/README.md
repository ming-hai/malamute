# Node.js Binding for Malamute

This is a development kit.

## Prerequisites

### Node.js

* You need Python (v2.7 recommended, v3.x not supported)
* You need (I recommend) nvm and Node.js.
* If your Linux has an existing 'node' command, `sudo apt-get remove node`.
* In every terminal, or .bashrc: `nvm use v5.5.0`

To install the necessary Node tools:

```
sudo apt-get update
sudo apt-get install build-essential libssl-dev
curl https://raw.githubusercontent.com/creationix/nvm/v0.11.1/install.sh | bash
# close terminal, re-open
nvm ls-remote
nvm install v5.5.0
npm install -g node-ninja
npm install -g prebuild
npm install -g bindings
```

To build:

```
mkdir -p $HOME/temp
cd $HOME/temp
git clone https://github.com/zeromq/malamute
cd malamute/bindings/nodejs
#   Clones dependencies, builds everything
./build.sh
```

## API

This is a wrapping of the native C libmlm library. See binding.cc for the code.

We get these classes:

* MlmProto - Set the content field, transferring ownership from caller
* MlmClient - 
