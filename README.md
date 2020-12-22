# The WASM/Suricata project

## Install

Clone this repository:

```
git clone --recurse-submodules https://github.com/chifflier/wasm-suricata.git
cd suricata
git clone -b 0.5.x https://github.com/OISF/libhtp.git
```

## Suricata

Build and install suricata as usual::

```
cd suricata
./autogen.sh
./configure --enable-wasm
make
```

See [Suricata's documentation](https://suricata.readthedocs.io/) for other build options, and how to install suricata.

## Build the TLS parser module

See the [module documentation](https://github.com/chifflier/wasm-tls-parser)

```
wasm-pack build --release
cp pkg/wasm_tls_parser_bg.wasm /etc/suricata/wasm-output/
```

## Developer documentation and discussion

More documentation in the [Wiki](https://github.com/chifflier/wasm-suricata/wiki)

