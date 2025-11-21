# setting up AmneziaWG on host

1. check if kernel has `sudo modprobe amneziawg`
2. [install it in kernel](https://habr.com/ru/companies/amnezia/articles/807539/)
3. LXC container doesn't allow update kernel, since it shares with the host. You can detect lxc [`ps -p 2` has no input for `kthreadd`](https://stackoverflow.com/questions/20010199/how-to-determine-if-a-process-runs-inside-lxc-docker#answer-72136877)

## AmneziaWG-GO

```bash
git clone https://github.com/amnezia-vpn/amneziawg-go
cd amneziawg-go
make
```
