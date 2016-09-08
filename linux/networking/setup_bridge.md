

Install Bridge Utils

```bash
sudo apt-get install bridge-utils
```

setup bridge 

```bash
# create a bridge interface
sudo brctl addbr br0

# add the 2 interfaces to bridge to the bridge
sudo brctl addif eth0
sudo brctl addif eth1

# remove any ip addresses from the bridged interfaces
sudo ifconfig eth0 0.0.0.0
sudo ifconfig eth1 0.0.0.0

# bring bridge interface up
sudo ifconfig br0 up
```
destroy bridge

```bash
# take bridge interface down
sudo ifconfig br0 down

# delete bridge interface
sudo brctl delbr br0
```

