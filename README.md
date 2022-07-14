# object-detection-telemetry
## 项目介绍
> 本项目主要用以对遥感图像的目标检测与分类。效果如下图：

![1](https://user-images.githubusercontent.com/56541797/178707501-f7feaecb-723d-4f76-bb4c-21aeb6ee3c3a.png)
![2](https://user-images.githubusercontent.com/56541797/178707514-ebad1851-b769-40f3-9e96-a02a5f68ea5f.png)
## 目录结构
```
|-- README.md                      # 项目说明文件
|-- main                           # 主文件
    |-- imgs                       # 测试图片目录
    |-- results                    # 结果保存目录
    |-- image_demo.py              # 识别脚本
    |-- config.sh                  # 配置脚本
|-- mmrotate-main                  # 模型相关文件
```
## 环境配置
- Python 3.7.7

- cuda 11.1

- torch 1.9.0
## 使用方法
### 1. 下载模型文件
下载地址：链接：https://pan.baidu.com/s/1BdO5Q-igHF_ZndDxwsk-PQ 
提取码：xw1o

下载完成后将checkpoints文件夹放置mmrotate-main目录下
### 2. 环境配置
- 进入main目录下，打开config.sh文件，按自己的版本修改如下命令（此处默认cuda==11.1，torch==1.9.0）

pip install mmcv-full -f https://download.openmmlab.com/mmcv/dist/cu111/torch1.9.0/index.html
- 修改完成后运行 sh config.sh 
### 3. 图像识别
在main目录下，执行如下命令：
python image_demo.py {input_path} {output_path}

例：python image_demo.py imgs/0.jpg results/0.png

然后会在output_path路径看到输出的结果
## 参考仓库
https://github.com/open-mmlab
