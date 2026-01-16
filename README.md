# System Requirements: Linux (any distribution), a dedicated GPU with at least 24GB VRAM, and CUDA version 11.8.
# Basic Environment Setup: Follow the steps below to reproduce our results.  
    conda create -n reid python=3.8 # advice linux system
    pip install torch torchvision torchaudio pytorch-ignite==0.2.1 --extra-index-url https://download.pytorch.org/whl/cu118
    pip install yacs
# clone our code：
    git clone https://github.com/Syk0802/Person-reidentification.git
# download data and address it!!!, e.g. Market
    cd dataset
    download market1501 dataset from google dirve [[link]](https://drive.google.com/file/d/1SMx9IBJORLyNZJbWG_f95Id3nYrU_XR_/view?usp=drive_link)
    unzip Market-1501-v15.09.15.zip
    mv * Market
    cd ..
# download init weight
    download model init weight file [[link]](https://drive.google.com/drive/folders/1lcctJBmWwj0wIN5C-gYscYHyTMndjINr?usp=drive_link)

# Train:
## Train baseline method:
    bash base.sh #for base
## Train our method:
    bash idea.sh # for our method
## All results will be display after training in the training log 