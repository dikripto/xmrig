## Tutorial Compile sampai Penggunaan XMRig

- Install termux
  - Download di Google Play   
- Adjust Termux
  - Perbaiki repositori yang rusak `termux-change-repo`   
  - Install package yang dibutuhkan `pkg install wget cmake`
- Download Miner
  - `wget https://github.com/dikripto/xmrig/archive/refs/heads/master.zip`   
- Build Miner
  - `cd master`
  - `mkdir build`
  - `cmake .. -DWITH_HWLOC=OFF`
  - `make`
- Konfigurasi Miner
  - Download config.json `wget https://gist.github.com/dytra/5b17acdd38fcabba83e6411f38cce5ad/raw/9214159292a479ec5c27ac7ea28d0da00ca99d4f/config.json`
  - Tampilkan full keyboard di termux. `mkdir $HOME/.termux/ ;echo "extra-keys = [['ESC','/','-','HOME','UP','END'],['TAB','CTRL','ALT','LEFT','DOWN','RIGHT']]" >> $HOME/.termux/termux.properties && termux-reload-settings && sleep 1 && logout`
  - Edit wallet address di config.json `nano config.json`
- Jalankan miner
  - `chmod +x xmrig`
  - `./xmrig`   
