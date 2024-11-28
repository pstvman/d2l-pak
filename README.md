# d2l-pak

dive to deep learning 的d2l预编译包，因为低版本会导致一些报错，每次在colab运行代码需要从源码编译安装，这是一个很大的时间花销。但是pypi上没有最新版本的预编译包，为了能够快速运行实验室代码，于是基于win_amd64及python=3.9重新编译了d2l-2.0.0的wheel文件。

使用方式1：使用 git clone
```
!git clone https://github.com/pstvman/d2l-pak.git
!pip install --no-deps d2l-pak/d2l-2.0.0-py3-none-any.whl
```

使用方式2：使用 wget + raw 链接
```
!wget https://raw.githubusercontent.com/pstvman/d2l-pak/main/d2l-2.0.0-py3-none-any.whl
!pip install --no-deps d2l-2.0.0-py3-none-any.whl
```

<br>

你也可以下载d2l源码([https://github.com/d2l-ai/d2l-zh](https://github.com/d2l-ai/d2l-zh))自行编译并上传colab进行安装。
```
git clone https://github.com/d2l-ai/d2l-zh.git
cd d2l-zh

conda create -n d2l-env python=3.9
conda activate d2l-env

pip install wheel setuptools
pip install jupyter==1.0.0 numpy==1.21.5 matplotlib==3.5.1 requests==2.25.1 pandas==1.2.4
python setup.py bdist_wheel --plat-name win_amd64 --python-tag cp39
```
