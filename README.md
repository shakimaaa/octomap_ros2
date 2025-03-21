# octomap_server_ros2
octomapping

#### 下载
首先需要安装[octomap](https://github.com/OctoMap/octomap.git) 
也可以二进制安装

```
sudo apt install ros-humble-octomap

```
安装pcl
```
sudo apt install ros-humble-perception-pcl

```
下载其他
```
vcs import . < deps.repos
```

### 编译项目

```
colco build --packages-up-to octomap_server2
```

### 启动
修改lacunch文件内 `cloud_in` 为真实输入点云话题
```
ros2 launch octomap_server2 octomap_server_launch.py
```