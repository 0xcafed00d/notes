

Install Bridge Utils

```bash
sudo apt-get install bridge-utils
```

setup bridge 

```bash
sudo brctl addbr br0
sudo brctl addif eth0
sudo brctl addif eth1
sudo ifconfig eth0 0.0.0.0
sudo ifconfig eth1 0.0.0.0
sudo ifconfig br0 up
```
destroy bridge

```bash
sudo ifconfig br0 down
sudo brctl delbr br0
```

