# Llama-env-test
Hugging Face + Llama 2
1.	Windows 下 Anaconda 中新建虚拟环境
2.	环境在终端打开，执行
conda install -c conda-forge huggingface_hub
3.	检查安装，执行
python -c "from huggingface_hub import model_info; print(model_info('gpt2'))"
4.	如下输出为安装正确
Model Name: gpt2
Tags: ['pytorch', 'tf', 'jax', 'tflite', 'rust', 'safetensors', 'gpt2', 'text-generation', 'en', 'doi:10.57967/hf/0039', 'transformers', 'exbert', 'license:mit', 'has_space']
Task: text-generation
5.	继续在终端执行
pip install transformers
huggingface-cli login
6.	login需要huggingface 的Access Tokens, 在Hugging Face账户个人设置界面
7.	Tokens粘贴进终端需要 CTRL + ‘Right Click’, 此处无任何显示，直接回车即可，登录有效会输出提示
8.	安装PyTorch 库
conda install pytorch torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia
9.	安装langchain 库
pip install langchain
10.	加载Llama 2 模型测试
model = "meta-llama/Llama-2-7b-chat-hf" # 模型封装体积过大，9.98G…
11.	若执行官方给出的独立下载脚本文件，则进程自动闪退，无法下载，仅创建指定文件夹。参考https://github.com/facebookresearch/llama/blob/main/README.md  中Quick Start .4 .5 部分。
12.	目前注意到，模型的在线使用都是需要付费的…
