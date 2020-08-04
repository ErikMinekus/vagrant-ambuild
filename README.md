Building SourceMod:
```bash
vagrant up
vagrant ssh
bash sourcemod/tools/checkout-deps.sh

cd sourcemod
mkdir build
cd build
python3 ../configure.py
ambuild
```

Building an extension:
```bash
vagrant up
vagrant ssh
# If the extension requires Metamod:Source or a Half-Life 2 SDK
git clone https://github.com/alliedmodders/metamod-source.git --depth 1 -b 1.10-dev
git clone https://github.com/alliedmodders/hl2sdk.git --depth 1 -b sdk2013 hl2sdk-sdk2013

cd extension
mkdir build
cd build
python3 ../configure.py --sdks=present
ambuild
```
