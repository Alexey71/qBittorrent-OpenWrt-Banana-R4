qBittorrent - BitTorrent клиент на Qt6
------------------------------------------

## Как собрать
1. Скачать ```git clone https://github.com/Alexey71/qBittorrent-OpenWrt.git```
2. Скопировать ```luci-app-qbittorrent qbittorrent qt6base qt6tools rblibtorrent``` в папку проекта ```openwrt/package/```
3. Войти в меню конефига ```make menuconfig```
4. Выбрать ```LUCI``` -> ```Applications``` -> ```luci-app-qbittorrent``` -> ```Save``` -> ```OK```
5. Запустить сборку прошивки ```make -jxx``` Где ```xx``` - это количество ядер процессора

   Можно запустить отдельно сборку qBittorrent коммандой ```make -jxx package/luci-app-qbittorrent/compile```
