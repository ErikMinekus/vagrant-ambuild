Building SourceMod:
```bash
vagrant up
vagrant ssh
bash sourcemod/tools/checkout-deps.sh

cd sourcemod
mkdir build
cd build
python ../configure.py
python ~/.local/bin/ambuild
```

Building an extension:
```bash
vagrant up
vagrant ssh
git clone https://github.com/alliedmodders/metamod-source.git -b 1.10-dev
git clone https://github.com/alliedmodders/hl2sdk.git -b sdk2013 hl2sdk-sdk2013
git clone https://github.com/alliedmodders/ambuild.git

cd ~/ambuild
python setup.py build
sudo python setup.py install

cd ~/sourcemod
mkdir build
cd build
python ../configure.py --no-mysql --sdks=present
ambuild

cd ~/extension
mkdir build
cd build
python ../configure.py --sdks=present
ambuild
```
