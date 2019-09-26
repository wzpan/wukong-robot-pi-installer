# wukong-robot-pi-installer

<p align="center">
  <a href="https://github.com/users/wzpan/projects/1"><img alt="wukong-project" src="https://img.shields.io/badge/project-wukong-informational.svg?style=flat-square"></a>
</p>

使用 docker 实现为树莓派自动化安装 [wukong-robot](https://github.com/wzpan/wukong-robot) 。理论上也能支持其他能跑 docker 的板子。

## 使用方法

``` bash
git clone https://github.com/wzpan/wukong-robot-pi-installer.git
cd wukong-robot-pi-installer
sudo ./pi_installer
```

然后使用如下命令启动 docker 镜像：

``` bash
docker run -it -p 5000:5000 --device /dev/snd -e LANG=C.UTF-8 wzpan/wukong-robot:latest
```

完成后可以参考 [运行](https://wukong.hahack.com/#/run) 一节，启动 wukong-robot。
