# MadRabbit（今天心情好，临时发布）
# 强调一下，rabbit后端与Ark后端无任何关系，魔改个屁啊，Ark源码都没得
# 发现新bug，关镜像修复中
# 1.1.0 更新最新验证码识别(同样的，只支持自动，5次过不去的自行调高次数)
## 注意，只支持阿里，腾讯ip

# 1.0.1 修复大量bug，适配Ark备注，增加部分功能

## 外面很多魔改Rabbit，拉了镜像多注意，别ck被偷了，烟雨版魔改Ark(烟雨的和rabbit没关系，仅此声明)属于正版，其他的都有偷ck的可能

# 目前功能：自动过魔方和拼图验证获取ck，wsck提交，未对接芝士，xdd等，不要来问我

# 配置:
1、新建一个项目
```
cd /root && mkdir -p  Rabbit && cd Rabbit
```
2、创建一个目录放配置
```
cd /root/Rabbit && mkdir -p  Config
```
3、下载config.json 配置文件 并且修改自己的配置 不能缺少
```
cd /root/Rabbit/Config && wget -O Config.json  https://raw.githubusercontent.com/ht944/MadRabbit/main/Config.json
```
国内用
```
cd /root/Rabbit/Config && wget -O Config.json  https://ghproxy.com/https://raw.githubusercontent.com/ht944/MadRabbit/main/Config.json
```
4、配置完后
```
cd /root/Rabbit
```

# 安装：(ARM架构的机器自己将latest改成arm)
## 方案一：自行构建镜像(由于有人魔改Rabbit，不再开源)
### 先下载源码，上传到此文件夹，再运行接下来的命令
```
docker build -t rabbit .
```
### 启动
```
docker run --name rabbit -d  -v "$(pwd)"/Config:/usr/src/Project/Config -p 5701:1234 rabbit:latest
```
## 方案二：使用我的镜像
```
docker pull ht944/rabbit:latest
```
### 启动
```
docker run --name rabbit -d  -v "$(pwd)"/Config:/usr/src/Project/Config -p 5701:1234 ht944/rabbit:latest
```

## 非阿里和腾讯服务器可以忽略这一步:
  ### 使用稳定的http或socks代理，不能有账号密码
  格式为：http://xxx.xxx.xxx.xxx:xxxx或socks://xxx.xxx.xxx.xxx:xxxx
  设置配置文件中的proxy即可

# 强调一遍
## 配置文件修改后，重新启动容器

## 特别声明:

* 本仓库涉仅用于测试和学习研究，禁止用于商业用途，不能保证其合法性，准确性，完整性和有效性，请根据情况自行判断.

* 本项目内所有资源文件，禁止任何公众号、自媒体进行任何形式的转载、发布。

* ht944对任何代码问题概不负责，包括但不限于由任何脚本错误导致的任何损失或损害.

* 间接使用本仓库搭建的任何用户，包括但不限于建立VPS或在某些行为违反国家/地区法律或相关法规的情况下进行传播, ht944对于由此引起的任何隐私泄漏或其他后果概不负责.

* 请勿将本项目的任何内容用于商业或非法目的，否则后果自负.

* 如果任何单位或个人认为该项目的脚本可能涉嫌侵犯其权利，则应及时通知并提供身份证明，所有权证明，我们将在收到认证文件后删除相关代码.

* 任何以任何方式查看此项目的人或直接或间接使用本仓库项目的任何脚本的使用者都应仔细阅读此声明。ht944 保留随时更改或补充此免责声明的权利。一旦使用并复制了任何本仓库项目的规则，则视为您已接受此免责声明.

**您必须在下载后的24小时内从计算机或手机中完全删除以上内容.**  </br>
> ***您使用或者复制了本仓库且本人制作的任何脚本，则视为`已接受`此声明，请仔细阅读***

## 多谢
