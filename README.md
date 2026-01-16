# System Requirements:
 Linux (any distribution), a dedicated GPU with at least 24GB VRAM, and CUDA version 11.8.
# Basic Environment Setup: Follow the steps below to reproduce our results.  
    conda create -n reid python=3.8 # advice linux system
    pip install torch torchvision torchaudio pytorch-ignite==0.2.1 --extra-index-url https://download.pytorch.org/whl/cu118
    pip install yacs
# Clone code：
    git clone https://github.com/Syk0802/Person-reidentification.git

# Prepare data, unzip, rename !!!
```cd dataset``` and download market1501 dataset from [Google Drive Link](https://drive.google.com/file/d/1SMx9IBJORLyNZJbWG_f95Id3nYrU_XR_/view?usp=drive_link)
```unzip Market-1501-v15.09.15.zip```
```cd ..```


# Download init weight
download model init weight file [Google Drive Link](https://drive.google.com/drive/folders/1lcctJBmWwj0wIN5C-gYscYHyTMndjINr?usp=drive_link)

# Train:
## Train baseline method:
    bash base.sh #for base method
## Train our method:
    bash idea.sh # for our method
## All results will be display after training in the training log 
For example：
> **Validation Results (Epoch 120):**
> * **mAP:** 87.3%
> * **CMC Rank-1:** 95.1%
> * **CMC Rank-5:** 98.4%
> * **CMC Rank-10:** 99.2%

