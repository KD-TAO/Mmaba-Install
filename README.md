# Mamba Install

### :rage:Problem:

```
1. `Building wheel for causal-conv1d (setup.py) ... error`
2. `RuntimeError: Error compiling objects for extension`
3. `Connection timed out> [end of output]`
4.  Building wheel for mamba-ssm (setup.py) ... error
...
```

### :smirk_cat: solution:

```
conda create -n mamba python=3.8
conda activate mamba
conda install cudatoolkit==11.7 -c nvidia
conda install pytorch==1.13.1 torchvision==0.14.1 torchaudio==0.13.1 pytorch-cuda=11.7 -c pytorch -c nvidia
conda install -c "nvidia/label/cuda-11.7.0" cuda-nvcc
conda install packaging
pip install causal-conv1d==1.1.1
pip install mamba_ssm==1.0.1
```







 