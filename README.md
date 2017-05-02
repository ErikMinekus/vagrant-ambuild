```bash
vagrant up
vagrant ssh
bash sourcemod/tools/checkout-deps.sh
cd sourcemod
mkdir build
cd build
CC="gcc-4.8" CXX="g++-4.8" python ../configure.py
python ~/.local/bin/ambuild
```
