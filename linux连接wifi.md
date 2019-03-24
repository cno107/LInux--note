# 连接Wi-Fi

1. 进入root

2. 查看是否已连网

3. ```linux
   iw wlp2s0 link
   ```

3. 获取SSID 
   `iw wlp2s0 scan | grep SSID` 
   command failed: Network is down (-100) 

4. 激活（打开wifi）
   ifconfig wlp2s0 up
   ifconfig wlp2s0

5. 查看附近WIFI
   iw wlp2s0 scan | grep SSID

6. 连接Wi-Fi
   wpa_supplicant -B -i wlp2s0 -c <(wpa_passphrase "user" "passwd")

7. 分配IP
   dhclient wlp2s0

8. 查看是否有了IP
    ifconfig wlp2s0

   


   
   出现Operation not possible due to RF-kill
   原因：在另外的init级别下关闭了wifi 所以当前level没有权限打开
   解决；rfkill -list
              rfkill unblock all 

   

   