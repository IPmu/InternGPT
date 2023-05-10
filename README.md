**The project is still under construction, we will continue to update it and welcome contributions/pull requests from the community.**



<p align="center"><img src="./assets/gvlab_logo.png" width="600"></p>

# InternChat [[paper](https://pjlab-gvm-data.oss-cn-shanghai.aliyuncs.com/papers/ichat.pdf)]


<!-- ## Description -->
**InternChat**(short for **iChat**) is pointing-language-driven visual interactive system. The name InternChat stands for **inter**action, **n**onverbal, and **chat**bots. Different from existing interactive systems that rely on pure language, by incorporating pointing instructions, iChat significantly improves the efficiency of communication between users and chatbots, as well as the accuracy of chatbots in vision-centric tasks, especially in complicated visual scenarios. Additionally, in iChat, an auxiliary control mechanism is used to improve the control capability of LLM, and a large vision-language model termed **Husky** is fine-tuned for high-quality multi-modal dialogue (impressing ChatGPT-3.5-turbo with **93.89% GPT-4 Quality**).

## Online Demo
[InternChat](https://ichat.opengvlab.com/) is online. Let's try it!


https://github.com/OpenGVLab/InternChat/assets/8529570/dbacfe72-a40f-48cc-acff-5c7ad0f64b68



## Schedule
- [ ] Support Chinese
- [ ] Support MOSS
- [ ] More powerful foundation models based on [InternImage](https://github.com/OpenGVLab/InternImage) and [InternVideo](https://github.com/OpenGVLab/InternVideo)
- [ ] More accurate interactive experience
- [ ] Web Page & Code Generation 
- [x] Support voice assistant
- [x] Support click interaction
- [x] Interactive image editing
- [x] Interactive image generation
- [x] Interactive visual question answering
- [x] Segment Anything
- [x] Image inpainting
- [x] Image caption
- [x] image matting
- [x] Optical character recognition
- [x] Action recognition
- [x] Video caption
- [x] Video dense caption
- [x] video highlight interpretation



## System Overview
<p align="center"><img src="./assets/arch1.png" alt="Logo"></p>

## 🎁 Major Features
<!--<!-- <p align="center"><img src="./assets/online_demo.gif" alt="Logo"></p> -->  
<p align="center">(a) Remove the masked object</p>
<p align="center"><img src="./assets/demo2.gif" width="500"></p>

<p align="center">(b) Interactive image editing</center>
<p align="center"><img src="./assets/demo3.gif" width="500"></p>

<p align="center">(c) Image generation</p>
<p align="center"><img src="./assets/demo4.gif" align='justify'  width="500"></p>

<p align="center">(d) Interactive visual question answer</p>
<p align="center"><img src="./assets/demo5.gif" align='justify' width="700"></p> 


<p align="center">(e) Interactive image generation</p>
<p align="center"><img src="./assets/demo5.gif" align='justify' width="700"></p> 

<p align="center">(f) Video highlight interpretation</p>
<p align="center"><img src="./assets/demo6.jpg" align='justify' width="500"></p> 

<!-- ![alt]("./assets/demo5.gif" "title") -->


## 🛠️ Installation

### Basic requirements

- Linux
- Python 3.8+
- PyTorch 1.12+
- CUDA 11.6+ 
- GCC & G++ 5.4+
- GPU Memory >= 17G for loading basic tools (HuskyVQA, SegmentAnything, ImageOCRRecognition)

### Install Python dependencies
```shell
pip install -r requirements.txt
```

### Model zoo
Coming soon...

## 👨‍🏫 Get Started 
Running the following shell can start a gradio service:
```shell
python -u IChatApp.py --load "HuskyVQA_cuda:0,SegmentAnything_cuda:0,ImageOCRRecognition_cuda:0" --port 3456
```

if you want to enable the voice assistant, please use `openssl` to generate the certificate:
```shell
openssl req -x509 -newkey rsa:4096 -keyout ./key.pem -out ./cert.pem -sha256 -days 365 -nodes
```

and then run:
```shell
python -u iChatApp.py --load "HuskyVQA_cuda:0,SegmentAnything_cuda:0,ImageOCRRecognition_cuda:0" --port 3456 --https
```
 



## 🎫 License

This project is released under the [Apache 2.0 license](LICENSE). 

## 🖊️ Citation

If you find this project useful in your research, please consider cite:
```BibTeX
@misc{2023internchat,
    title={InternChat: Solving Vision-Centric Tasks by Interacting with Chatbots Beyond Language},
    author={Zhaoyang Liu and Yinan He and Wenhai Wang and Weiyun Wang and Yi Wang and Shoufa Chen and Qinglong Zhang and Yang Yang and Qingyun Li and Jiashuo Yu and Kunchang Li and Zhe Chen and Xue Yang and Xizhou Zhu and Yali Wang and Limin Wang and Ping Luo and Jifeng Dai and Yu Qiao},
    howpublished = {\url{https://www.shlab.org.cn}},
    year={2023}
}
```

## 🤝 Acknowledgement
Thanks to the open source of the following projects:

[Hugging Face](https://github.com/huggingface) &#8194;
[LangChain](https://github.com/hwchase17/langchain) &#8194;
[TaskMatrix](https://github.com/microsoft/TaskMatrix) &#8194;
[SAM](https://github.com/facebookresearch/segment-anything) &#8194;
[Stable Diffusion](https://github.com/CompVis/stable-diffusion) &#8194; 
[ControlNet](https://github.com/lllyasviel/ControlNet) &#8194; 
[InstructPix2Pix](https://github.com/timothybrooks/instruct-pix2pix) &#8194; 
[BLIP](https://github.com/salesforce/BLIP) &#8194;
[Latent Diffusion Models](https://github.com/CompVis/latent-diffusion) &#8194;
[EasyOCR](https://github.com/JaidedAI/EasyOCR) &#8194;


