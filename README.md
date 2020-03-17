# 云编译N1 Openwrt固件 Docker
使用lean’s lede源代码  
主要集成插件ShadowSocksrPlus+ passwall clash openclash koolproxyrPlus+ smartdns AdGuardHome...  
默认ip已更换为192.168.2.1

# 食用方法
----①.将docker-img-openwrt-aarch64-0317.gz文件上传至N1的/root目录   
----②.导入软路由docker包：  
----gzip -dc docker-img-openwrt-aarch64-****.gz | docker load  
----或者docker pull unifreq/openwrt-aarch64:****（如果未按第①步事先下载并上传镜像包的话）  
----③运行容器：  
----docker run  -d --restart always --network macnet --ip 192.168.2.1  --privileged bobotoy/openwrt-aarch64:0317  /sbin/init  

# 鸣谢
借鉴引用以下大佬代码  
https://github.com/fyglinfo/actions-openwrt-passwall  
https://github.com/P3TERX/Actions-OpenWrt  
https://github.com/Lienol/openwrt-package  
https://github.com/coolsnowwolf/lede  
https://github.com/zorzcc/openwrt-actions  
