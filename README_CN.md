<p align="center">
  <img src="assets/realesrgan_logo.png" height=120>
</p>

## <div align="center"><b><a href="README.md">English</a> | <a href="README_CN.md">简体中文</a></b></div>

[![download](https://img.shields.io/github/downloads/xinntao/Real-ESRGAN/total.svg)](https://github.com/xinntao/Real-ESRGAN/releases)
[![PyPI](https://img.shields.io/pypi/v/realesrgan)](https://pypi.org/project/realesrgan/)
[![Open issue](https://img.shields.io/github/issues/xinntao/Real-ESRGAN)](https://github.com/xinntao/Real-ESRGAN/issues)
[![Closed issue](https://img.shields.io/github/issues-closed/xinntao/Real-ESRGAN)](https://github.com/xinntao/Real-ESRGAN/issues)
[![LICENSE](https://img.shields.io/github/license/xinntao/Real-ESRGAN.svg)](https://github.com/xinntao/Real-ESRGAN/blob/master/LICENSE)
[![python lint](https://github.com/xinntao/Real-ESRGAN/actions/workflows/pylint.yml/badge.svg)](https://github.com/xinntao/Real-ESRGAN/blob/master/.github/workflows/pylint.yml)
[![Publish-pip](https://github.com/xinntao/Real-ESRGAN/actions/workflows/publish-pip.yml/badge.svg)](https://github.com/xinntao/Real-ESRGAN/blob/master/.github/workflows/publish-pip.yml)

:fire: 更新动漫视频的小模型 **RealESRGAN AnimeVideo-v3**. 更多信息在 [[动漫视频模型介绍](docs/anime_video_model.md)] 和 [[比较](docs/anime_comparisons_CN.md)] 中.

1. Real-ESRGAN的[Colab Demo](https://colab.research.google.com/drive/1k2Zod6kSHEvraybHl50Lys0LerhyTMCo?usp=sharing) | Real-ESRGAN**动漫视频** 的[Colab Demo](https://colab.research.google.com/drive/1yNl9ORUxxlL4N0keJa2SEPB61imPQd1B?usp=sharing)
2. **支持Intel/AMD/Nvidia显卡**的绿色版exe文件： [Windows版](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-windows.zip) / [Linux版](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-ubuntu.zip) / [macOS版](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-macos.zip)，详情请移步[这里](#便携版（绿色版）可执行文件)。NCNN的实现在 [Real-ESRGAN-ncnn-vulkan](https://github.com/xinntao/Real-ESRGAN-ncnn-vulkan)。

Real-ESRGAN 的目标是开发出**实用的图像/视频修复算法**。<br>
我们在 ESRGAN 的基础上使用纯合成的数据来进行训练，以使其能被应用于实际的图片修复的场景（顾名思义：Real-ESRGAN）。

:art: Real-ESRGAN 需要，也很欢迎你的贡献，如新功能、模型、bug修复、建议、维护等等。详情可以查看[CONTRIBUTING.md](docs/CONTRIBUTING.md)，所有的贡献者都会被列在[此处](README_CN.md#hugs-感谢)。

:milky_way: 感谢大家提供了很好的反馈。这些反馈会逐步更新在 [这个文档](docs/feedback.md)。

:question: 常见的问题可以在[FAQ.md](docs/FAQ.md)中找到答案。（好吧，现在还是空白的=-=||）

---

如果 Real-ESRGAN 对你有帮助，可以给本项目一个 Star :star: ，或者推荐给你的朋友们，谢谢！:blush: <br/>
其他推荐的项目：<br/>
:arrow_forward: [GFPGAN](https://github.com/TencentARC/GFPGAN): 实用的人脸复原算法 <br>
:arrow_forward: [BasicSR](https://github.com/xinntao/BasicSR): 开源的图像和视频工具箱<br>
:arrow_forward: [facexlib](https://github.com/xinntao/facexlib): 提供与人脸相关的工具箱<br>
:arrow_forward: [HandyView](https://github.com/xinntao/HandyView): 基于PyQt5的图片查看器，方便查看以及比较 <br>

---

<!---------------------------------- Updates --------------------------->
<details>
<summary>🚩<b>更新</b></summary>

- ✅ 更新动漫视频的小模型 **RealESRGAN AnimeVideo-v3**. 更多信息在 [anime video models](docs/anime_video_model.md) 和 [comparisons](docs/anime_comparisons.md)中.
- ✅ 添加了针对动漫视频的小模型, 更多信息在 [anime video models](docs/anime_video_model.md) 中.
- ✅ 添加了ncnn 实现：[Real-ESRGAN-ncnn-vulkan](https://github.com/xinntao/Real-ESRGAN-ncnn-vulkan).
- ✅ 添加了 [*RealESRGAN_x4plus_anime_6B.pth*](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.2.4/RealESRGAN_x4plus_anime_6B.pth)，对二次元图片进行了优化，并减少了model的大小。详情 以及 与[waifu2x](https://github.com/nihui/waifu2x-ncnn-vulkan)的对比请查看[**anime_model.md**](docs/anime_model.md)
- ✅支持用户在自己的数据上进行微调 (finetune)：[详情](docs/Training.md#Finetune-Real-ESRGAN-on-your-own-dataset)
- ✅ 支持使用[GFPGAN](https://github.com/TencentARC/GFPGAN)**增强人脸**
- ✅ 通过[Gradio](https://github.com/gradio-app/gradio)添加到了[Huggingface Spaces](https://huggingface.co/spaces)（一个机器学习应用的在线平台）：[Gradio在线版](https://huggingface.co/spaces/akhaliq/Real-ESRGAN)。感谢[@AK391](https://github.com/AK391)
- ✅ 支持任意比例的缩放：`--outscale`（实际上使用`LANCZOS4`来更进一步调整输出图像的尺寸）。添加了*RealESRGAN_x2plus.pth*模型
- ✅ [推断脚本](inference_realesrgan.py)支持: 1) 分块处理**tile**; 2) 带**alpha通道**的图像; 3) **灰色**图像; 4) **16-bit**图像.
- ✅ 训练代码已经发布，具体做法可查看：[Training.md](docs/Training.md)。

</details>

<!---------------------------------- Projects that use Real-ESRGAN --------------------------->
<details>
<summary>🧩<b>使用Real-ESRGAN的项目</b></summary>

&nbsp;&nbsp;&nbsp;&nbsp;👋 如果你开发/使用/集成了Real-ESRGAN, 欢迎联系我添加

- NCNN-Android: [RealSR-NCNN-Android](https://github.com/tumuyan/RealSR-NCNN-Android) by [tumuyan](https://github.com/tumuyan)
- VapourSynth: [vs-realesrgan](https://github.com/HolyWu/vs-realesrgan) by [HolyWu](https://github.com/HolyWu)
- NCNN: [Real-ESRGAN-ncnn-vulkan](https://github.com/xinntao/Real-ESRGAN-ncnn-vulkan)

&nbsp;&nbsp;&nbsp;&nbsp;**易用的图形界面**

- [Waifu2x-Extension-GUI](https://github.com/AaronFeng753/Waifu2x-Extension-GUI) by [AaronFeng753](https://github.com/AaronFeng753)
- [Squirrel-RIFE](https://github.com/Justin62628/Squirrel-RIFE) by [Justin62628](https://github.com/Justin62628)
- [Real-GUI](https://github.com/scifx/Real-GUI) by [scifx](https://github.com/scifx)
- [Real-ESRGAN_GUI](https://github.com/net2cn/Real-ESRGAN_GUI) by [net2cn](https://github.com/net2cn)
- [Real-ESRGAN-EGUI](https://github.com/WGzeyu/Real-ESRGAN-EGUI) by [WGzeyu](https://github.com/WGzeyu)
- [anime_upscaler](https://github.com/shangar21/anime_upscaler) by [shangar21](https://github.com/shangar21)
- [RealESRGAN-GUI](https://github.com/Baiyuetribe/paper2gui/blob/main/Video%20Super%20Resolution/RealESRGAN-GUI.md) by [Baiyuetribe](https://github.com/Baiyuetribe)

</details>

<details>
<summary>👀<b>Demo视频（B站）</b></summary>

- [大闹天宫片段](https://www.bilibili.com/video/BV1ja41117zb)

</details>

### :book: Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data

> [[论文](https://arxiv.org/abs/2107.10833)] &emsp; [项目主页] &emsp; [[YouTube 视频](https://www.youtube.com/watch?v=fxHWoDSSvSc)] &emsp; [[B站视频](https://www.bilibili.com/video/BV1H34y1m7sS/)] &emsp; [[Poster](https://xinntao.github.io/projects/RealESRGAN_src/RealESRGAN_poster.pdf)] &emsp; [[PPT](https://docs.google.com/presentation/d/1QtW6Iy8rm8rGLsJ0Ldti6kP-7Qyzy6XL/edit?usp=sharing&ouid=109799856763657548160&rtpof=true&sd=true)]<br>
> [Xintao Wang](https://xinntao.github.io/), Liangbin Xie, [Chao Dong](https://scholar.google.com.hk/citations?user=OSDCB0UAAAAJ), [Ying Shan](https://scholar.google.com/citations?user=4oXBp9UAAAAJ&hl=en) <br>
> Tencent ARC Lab; Shenzhen Institutes of Advanced Technology, Chinese Academy of Sciences

<p align="center">
  <img src="assets/teaser.jpg">
</p>

---

我们提供了一套训练好的模型（*RealESRGAN_x4plus.pth*)，可以进行4倍的超分辨率。<br>
**现在的 Real-ESRGAN 还是有几率失败的，因为现实生活的降质过程比较复杂。**<br>
而且，本项目对**人脸以及文字之类**的效果还不是太好，但是我们会持续进行优化的。<br>

Real-ESRGAN 将会被长期支持，我会在空闲的时间中持续维护更新。

这些是未来计划的几个新功能：

- [ ] 优化人脸
- [ ] 优化文字
- [x] 优化动画图像
- [ ] 支持更多的超分辨率比例
- [ ] 可调节的复原

如果你有好主意或需求，欢迎在 issue 或 discussion 中提出。<br/>
如果你有一些 Real-ESRGAN 中有问题的照片，你也可以在 issue 或者 discussion 中发出来。我会留意（但是不一定能解决:stuck_out_tongue:）。如果有必要的话，我还会专门开一页来记录那些有待解决的图像。

---

### 便携版（绿色版）可执行文件

你可以下载**支持Intel/AMD/Nvidia显卡**的绿色版exe文件： [Windows版](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-windows.zip) / [Linux版](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-ubuntu.zip) / [macOS版](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-macos.zip)。

绿色版指的是这些exe你可以直接运行（放U盘里拷走都没问题），因为里面已经有所需的文件和模型了。它不需要 CUDA 或者 PyTorch运行环境。<br>

你可以通过下面这个命令来运行（Windows版本的例子，更多信息请查看对应版本的README.md）：

```bash
./realesrgan-ncnn-vulkan.exe -i 输入图像.jpg -o 输出图像.png -n 模型名字
```

我们提供了五种模型：

1. realesrgan-x4plus（默认）
2. reaesrnet-x4plus
3. realesrgan-x4plus-anime（针对动漫插画图像优化，有更小的体积）
4. realesr-animevideov3 (针对动漫视频)

你可以通过`-n`参数来使用其他模型，例如`./realesrgan-ncnn-vulkan.exe -i 二次元图片.jpg -o 二刺螈图片.png -n realesrgan-x4plus-anime`

### 可执行文件的用法

1. 更多细节可以参考 [Real-ESRGAN-ncnn-vulkan](https://github.com/xinntao/Real-ESRGAN-ncnn-vulkan#computer-usages).
2. 注意：可执行文件并没有支持 python 脚本 `inference_realesrgan.py` 中所有的功能，比如 `outscale` 选项) .

```console
Usage: realesrgan-ncnn-vulkan.exe -i infile -o outfile [options]...

  -h                   show this help
  -i input-path        input image path (jpg/png/webp) or directory
  -o output-path       output image path (jpg/png/webp) or directory
  -s scale             upscale ratio (can be 2, 3, 4. default=4)
  -t tile-size         tile size (>=32/0=auto, default=0) can be 0,0,0 for multi-gpu
  -m model-path        folder path to the pre-trained models. default=models
  -n model-name        model name (default=realesr-animevideov3, can be realesr-animevideov3 | realesrgan-x4plus | realesrgan-x4plus-anime | realesrnet-x4plus)
  -g gpu-id            gpu device to use (default=auto) can be 0,1,2 for multi-gpu
  -j load:proc:save    thread count for load/proc/save (default=1:2:2) can be 1:2,2,2:2 for multi-gpu
  -x                   enable tta mode"
  -f format            output image format (jpg/png/webp, default=ext/png)
  -v                   verbose output
```

由于这些exe文件会把图像分成几个板块，然后来分别进行处理，再合成导出，输出的图像可能会有一点割裂感（而且可能跟PyTorch的输出不太一样）

---

## :wrench: 依赖以及安装

- Python >= 3.7 (推荐使用[Anaconda](https://www.anaconda.com/download/#linux)或[Miniconda](https://docs.conda.io/en/latest/miniconda.html))
- [PyTorch >= 1.7](https://pytorch.org/)
- 如果要使用 `inference_realesrgan_video.py`，需要保证 `ffmpeg` 在 `PATH` 中

#### 安装

1. 把项目克隆到本地

    ```bash
    git clone https://github.com/xinntao/Real-ESRGAN.git
    cd Real-ESRGAN
    ```

2. 安装各种依赖

    ```bash
    # 安装 basicsr - https://github.com/xinntao/BasicSR
    # 我们使用BasicSR来训练以及推断
    pip install basicsr
    # facexlib和gfpgan是用来增强人脸的
    pip install facexlib
    pip install gfpgan
    pip install -r requirements.txt
    python setup.py develop
    ```

## :zap: 快速上手

Real-ESRGAN 提供两个 Python 入口脚本：

- `inference_realesrgan.py`：处理单张图片或图片文件夹
- `inference_realesrgan_video.py`：处理视频、序列帧或文件夹

脚本会在需要时自动把缺失的模型下载到 `weights/`。默认也会自动选择当前机器上最合适的推理设备：

- 优先使用 Nvidia GPU 的 CUDA
- Apple Silicon / Metal 环境使用 MPS
- 最后回退到 CPU

`--fp32` 可以在 CUDA 上强制使用 fp32；如果当前设备不支持 half precision，程序会自动回退到 fp32。

### 常用模型

- `RealESRGAN_x4plus`：通用照片、真实场景图片
- `RealESRGAN_x4plus_anime_6B`：动漫、插画、二次元图片
- `RealESRGAN_x2plus`：通用 2 倍放大
- `realesr-general-x4v3`：更轻量的通用模型，可通过 `-dn` 调整去噪强度
- `realesr-animevideov3`：动漫视频模型

### 图片推理：`inference_realesrgan.py`

这个脚本用于处理单张图片或图片文件夹。

```console
Usage: python inference_realesrgan.py -i INPUT [options]

示例：
python inference_realesrgan.py -n RealESRGAN_x4plus -i inputs/0014.jpg -o results --outscale 3.5

主要参数：
  -i, --input             输入图片或文件夹。默认：inputs
  -o, --output            输出目录。默认：results
  -n, --model_name        模型名称。默认：RealESRGAN_x4plus
  --model_path            自定义模型路径；不传时会自动下载权重
  -s, --outscale          最终输出缩放倍率。默认：4
  -dn, --denoise_strength realesr-general-x4v3 专用去噪强度；0 保留更多噪点，1 去噪更强
  --suffix                输出文件名后缀。默认：out
  -t, --tile              分块大小；大图或显存/内存不足时建议设置为大于 0
  --tile_pad              分块之间的重叠像素。默认：10
  --pre_pad               推理前的边缘 padding。默认：0
  --face_enhance          启用 GFPGAN 人脸增强
  --fp32                  在 CUDA 上强制使用 fp32，而不是 fp16
  --alpha_upsampler       Alpha 通道放大方式：realesrgan | bicubic
  --ext                   输出扩展名：auto | jpg | png
  -g, --gpu-id            多张 CUDA 显卡时指定 GPU 编号
```

命令行示例：

```bash
# 使用默认通用 x4 模型处理单张照片
python inference_realesrgan.py -n RealESRGAN_x4plus -i inputs/0014.jpg -o results

# 处理整个文件夹，并把最终输出缩放到 3.5 倍
python inference_realesrgan.py -n RealESRGAN_x4plus -i inputs -o results --outscale 3.5

# 使用动漫模型处理插画
python inference_realesrgan.py -n RealESRGAN_x4plus_anime_6B -i inputs/OST_009.png -o results

# 使用轻量通用模型，并降低去噪强度以保留更多纹理
python inference_realesrgan.py -n realesr-general-x4v3 -i inputs/00003.png -o results -dn 0.3

# 大图分块处理，降低显存或内存压力
python inference_realesrgan.py -n RealESRGAN_x4plus -i inputs/00003.png -o results -t 512 --tile_pad 32

# 处理人像并启用人脸增强
python inference_realesrgan.py -n RealESRGAN_x4plus -i inputs/0014.jpg -o results --face_enhance
```

主要参数的使用建议：

- `--outscale`：可以输出 `2`、`3.5`、`4` 等任意最终倍率
- `-t/--tile`：大图爆显存或爆内存时优先调这个参数
- `-dn/--denoise_strength`：只对 `realesr-general-x4v3` 生效
- `--face_enhance`：会用 GFPGAN 处理检测到的人脸，背景仍由 Real-ESRGAN 处理
- `--alpha_upsampler bicubic`：透明 PNG 如果更关注速度，可以用它来处理 alpha 通道

输出默认写到 `results/`。例如 `0014.jpg` 默认会变成 `results/0014_out.jpg`，除非你修改了 `--suffix`。

### 视频推理：`inference_realesrgan_video.py`

这个脚本用于处理视频、序列帧或图片文件夹，底层依赖 `ffmpeg`。

```console
Usage: python inference_realesrgan_video.py -i INPUT [options]

示例：
python inference_realesrgan_video.py -n realesr-animevideov3 -i inputs/video/onepiece_demo.mp4 -o results

主要参数：
  -i, --input             输入视频、图片或文件夹
  -o, --output            输出目录。默认：results
  -n, --model_name        模型名称。默认：realesr-animevideov3
  -s, --outscale          最终输出缩放倍率。默认：4
  -dn, --denoise_strength realesr-general-x4v3 专用去噪强度
  --suffix                输出视频文件名后缀。默认：out
  -t, --tile              每帧的分块大小
  --tile_pad              分块之间的重叠像素。默认：10
  --pre_pad               推理前的边缘 padding。默认：0
  --face_enhance          对每一帧启用 GFPGAN 人脸增强
  --fp32                  在 CUDA 上强制使用 fp32，而不是 fp16
  --fps                   指定输出 FPS；默认沿用原视频 FPS
  --ffmpeg_bin            ffmpeg 可执行文件路径。默认：ffmpeg
  --extract_frame_first   先把视频拆成帧再处理
  --num_process_per_gpu   每张 CUDA 显卡的并行进程数。默认：1
```

命令行示例：

```bash
# 使用默认动漫视频模型处理视频
python inference_realesrgan_video.py -n realesr-animevideov3 -i inputs/video/onepiece_demo.mp4 -o results

# 使用通用 x4 模型处理视频，并启用分块
python inference_realesrgan_video.py -n RealESRGAN_x4plus -i inputs/video/onepiece_demo.mp4 -o results -t 256

# 使用轻量通用模型，并降低去噪强度以保留更多纹理
python inference_realesrgan_video.py -n realesr-general-x4v3 -i inputs/video/onepiece_demo.mp4 -o results -dn 0.2

# 启用人脸增强，并显式指定输出帧率
python inference_realesrgan_video.py -n RealESRGAN_x4plus -i inputs/video/onepiece_demo.mp4 -o results --face_enhance --fps 24

# 如果 ffmpeg 不在 PATH 中，可以手动指定路径
python inference_realesrgan_video.py -n realesr-animevideov3 -i inputs/video/onepiece_demo.mp4 -o results --ffmpeg_bin /usr/local/bin/ffmpeg
```

视频参数的使用建议：

- `--fps`：用于覆盖输出视频帧率
- `--extract_frame_first`：当某些平台直接管道处理不稳定时很有用，但会占用更多磁盘空间
- `--num_process_per_gpu`：主要给 CUDA 多进程并行使用，MPS 和 CPU 一般不需要调整
- `-t/--tile`：单帧分辨率太大时，优先调这个参数

输出默认写到 `results/`。例如 `onepiece_demo.mp4` 默认会变成 `results/onepiece_demo_out.mp4`。

## :european_castle: 模型库

请参见 [docs/model_zoo.md](docs/model_zoo.md)

## :computer: 训练，在你的数据上微调（Fine-tune）

这里有一份详细的指南：[Training.md](docs/Training.md).

## BibTeX 引用

    @Article{wang2021realesrgan,
        title={Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data},
        author={Xintao Wang and Liangbin Xie and Chao Dong and Ying Shan},
        journal={arXiv:2107.10833},
        year={2021}
    }

## :e-mail: 联系我们

如果你有任何问题，请通过 `xintao.wang@outlook.com` 或 `xintaowang@tencent.com` 联系我们。

## :hugs: 感谢

感谢所有的贡献者大大们~

- [AK391](https://github.com/AK391): 通过[Gradio](https://github.com/gradio-app/gradio)添加到了[Huggingface Spaces](https://huggingface.co/spaces)（一个机器学习应用的在线平台）：[Gradio在线版](https://huggingface.co/spaces/akhaliq/Real-ESRGAN)。
- [Asiimoviet](https://github.com/Asiimoviet): 把 README.md 文档 翻译成了中文。
- [2ji3150](https://github.com/2ji3150): 感谢详尽并且富有价值的[反馈、建议](https://github.com/xinntao/Real-ESRGAN/issues/131).
- [Jared-02](https://github.com/Jared-02): 把 Training.md 文档 翻译成了中文。
