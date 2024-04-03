FROM mcr.microsoft.com/devcontainers/python:3.10

RUN sudo apt-get update \
    && sudo apt-get install -y git-lfs google-perftools bc libgl1 lshw

RUN git clone https://huggingface.co/segmind/tiny-sd \
    && cd tiny-sd \
    && git lfs pull \
    && git clone https://huggingface.co/latent-consistency/lcm-lora-sdv1-5 \ 
    && cd lcm-lora-sdv1-5 \
    && git lfs pull \
    && mv pytorch_lora_weights.safetensors ../stable-diffusion-webui-directml/models/Lora/lcm_lora_sdv15.safetensors

# RUN git clone https://github.com/lshqqytiger/stable-diffusion-webui-directml

# RUN pip install xformers torch torchvision