# MBR
```markdown


额这是一个压缩包，附带 MEMZ 修改的 MBR 汇编文件和图像音频，以及转换它们为 bin 格式的 Python 脚本。
```
## 文件说明

- `kernel.asm` - 主引导记录汇编代码，包含启动、动画和音乐播放逻辑
- `decompress.asm` - 实时解压缩模块，用于在内存中解压图像数据
- `png2bin.py` - PNG 转 MBR 格式工具，将图片转换为 DOS 16 色字符画数据
- `midi2bin.py` - MIDI 转 MBR 音乐工具，将 MIDI 音符转换为 PC 扬声器频率数据

## 依赖安装

```bash
pip install Pillow python-midi
```

## 使用方法

### 音频（单个 MIDI 文件）

```bash
python midi2bin.py YOUR_MIDI.mid music.bin
```

### 图像（可以是多个）

```bash
python png2bin.py image0.png image1.png ... output.bin
```

## 数据格式

- 图像数据：每 2 个垂直像素打包成 1 字节（高 4 位 = 上像素，低 4 位 = 下像素）
- 音乐数据：每个音符占 2 字节（低字节 = 频率，高字节 = 时长 + 频率高位）

懒 ~(￣▽￣)~
```

这样你复制出去，直接粘贴到 `README.md` 文件里就是格式正确的。
