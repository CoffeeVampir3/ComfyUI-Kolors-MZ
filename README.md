![image](./examples/workflow_ipa.png)

## Recent changes 
* [2024-07-18] IPA相关节点已在ComfyUI_IPAdapter_plus中支持
* [2024-07-17] 新增支持IPAdapter_plus的加载器和高级应用节点 MZ_KolorsCLIPVisionLoader,MZ_IPAdapterModelLoaderKolors,MZ_IPAdapterAdvancedKolors
* [2024-07-14] 删除自动兼容ControlNet, 新增MZ_KolorsControlNetPatch节点
  ![image](https://github.com/user-attachments/assets/73ae6447-c69d-4781-9c66-94e0029709ed)



## ComfyUI上Kolors的实现

参考自 https://github.com/kijai/ComfyUI-KwaiKolorsWrapper

使用ComfyUI原生采样

工作流在examples/workflow.png中获取


unet模型放置在 models/unet/ 文件夹下
下载地址:
https://huggingface.co/Kwai-Kolors/Kolors/blob/main/unet/diffusion_pytorch_model.fp16.safetensors


chatglm3放置在 models/LLM/ 文件夹下
下载地址:
https://huggingface.co/Kijai/ChatGLM3-safetensors/blob/main/chatglm3-fp16.safetensors


### 官方IP-Adapter-Plus模型下载地址

https://huggingface.co/Kwai-Kolors/Kolors-IP-Adapter-Plus/blob/main/ip_adapter_plus_genernal.bin 下载至 models/ipadapter/

https://huggingface.co/Kwai-Kolors/Kolors-IP-Adapter-Plus/blob/main/image_encoder/pytorch_model.bin 下载至 models/clip_vision/
 

## Implementation of Kolors on ComfyUI

Reference from https://github.com/kijai/ComfyUI-KwaiKolorsWrapper

Using ComfyUI Native Sampling

The workflow is obtained in examples/workflow.png


The unet model is placed in the models/unet/ folder
Download link:
https://huggingface.co/Kwai-Kolors/Kolors/blob/main/unet/diffusion_pytorch_model.fp16.safetensors


The chatglm3 is placed in the models/LLM/ folder
Download link:
https://huggingface.co/Kijai/ChatGLM3-safetensors/tree/main


### Official IP-Adapter-Plus model download link

https://huggingface.co/Kwai-Kolors/Kolors-IP-Adapter-Plus/resolve/main/ip_adapter_plus_genernal.bin Download to models/ipadapter/

https://huggingface.co/Kwai-Kolors/Kolors-IP-Adapter-Plus/blob/main/image_encoder/pytorch_model.bin Download to models/clip_vision/

## FAQ
name 'round_up' is not defined
+ 参考:https://github.com/THUDM/ChatGLM2-6B/issues/272#issuecomment-1632164243 , 使用 pip install cpm_kernels 或者 pip install -U cpm_kernels 更新 cpm_kernels

module 'comfy.model_detection' has no attribute 'unet_prefix_from_state_dict'
+ 更新ComfyUI本体到最新版本

RuntimeError: Only Tensors of floating point dtype can require gradients
+ 尝试使用fp16版本的模型: https://huggingface.co/Kijai/ChatGLM3-safetensors/blob/main/chatglm3-fp16.safetensors

Error occurred when executing MZ_ChatGLM3Loader: 'ChatGLMModel' object has no attribute 'transformer'
+ 检查ChatGLM3Loader节点选择的模型是否已经正确下载


## Credits

- [Kolors](https://github.com/Kwai-Kolors/Kolors)
- [ComfyUI](https://github.com/comfyanonymous/ComfyUI) 
- [ComfyUI_IPAdapter_plus](https://github.com/cubiq/ComfyUI_IPAdapter_plus)


## Star History

<a href="https://star-history.com/#MinusZoneAI/ComfyUI-Kolors-MZ&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=MinusZoneAI/ComfyUI-Kolors-MZ&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=MinusZoneAI/ComfyUI-Kolors-MZ&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=MinusZoneAI/ComfyUI-Kolors-MZ&type=Date" />
 </picture>
</a>


## Contact
- 微信Wechat: minrszone
- Bilibili: [minus_zone](https://space.bilibili.com/5950992)
- 小红书: [MinusZoneAI](https://www.xiaohongshu.com/user/profile/5f072e990000000001005472)

## Sponsorship
<img src="https://github.com/user-attachments/assets/a7ef9684-4911-45b6-8071-a9b433dca6af"  width="200"/>

