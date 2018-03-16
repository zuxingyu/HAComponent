
## 说明：
 - 本组件使用[frp](https://github.com/fatedier/frp)作为建立隧道的工具
 - 本组件仅实现了http虚拟主机，用于在INTERNET上访问homeassistant开放的端口
 
 
## 下载frp：
https://github.com/fatedier/frp/releases

找到您homeassistant所在的操作系统，下载对应的文件。
**我们仅需要其中的frpc程序。**

如果是树莓派，使用`frp_0.16.0_linux_arm.tar.gz`，解压缩后获得frpc文件（可能需要增加可执行权限`chmod +x frpc`），在下面的配置文件中配置其地址。


## 配置HomeAssistant：
 - （适用于python3.5环境用户）将`tunnel2local.pyc`与`tunnel2local.xx`放置在`~/.homeassistant/custom_components/`目录下
 - 配置文件：
 
```yaml
tunnel2local:
  # frpc命令位置
  frpc_bin: "C:/local/frp_0.16.0_windows_amd64/frpc.exe"

```