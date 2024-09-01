qBittorrent - BitTorrent клиент на Qt6
------------------------------------------

## Как собрать

Скопировать openwrt/package/

### Openwrt official SnapShots

```shell
git clone https://github.com/Alexey71/qBittorrent-OpenWrt.git
make menuconfig # выбрать LUCI -> Applications -> luci-app-qbittorrent
make -jxx
```
