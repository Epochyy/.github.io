## 更新 python 版本
### 卸载旧版本
+ 删除python framework

` sudo rm -rf /Library/Frameworks/Python.framework/Versions/3.6 `

+ 删除python应用目录

` sudo rm -rf "/Applications/Python 3.6" `

+ 删除usr/loacl/bin 下指向的python连接

```
1. cd /usr/local/bin/ 
2. ls -l /usr/local/bin | grep '../Library/Frameworks/Python.framework/Versions/3.6' | awk '{print $9}' | tr -d @ | xargs rm ```

### 配置新版本环境
+ 更新配置文件中的路径

`open ~/.bash_profile`

+ 让配置文件生效

`source ~/.bash_profile`
