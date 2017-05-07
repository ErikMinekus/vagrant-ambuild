```bash
vagrant up
vagrant ssh
bash sourcemod/tools/checkout-deps.sh
cd sourcemod
mkdir build
cd build
CC=clang CXX=clang++ python ../configure.py
python ~/.local/bin/ambuild
```
