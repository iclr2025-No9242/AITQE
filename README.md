# AITQE

### Requirements

```bash
pip install -r requirements.txt
```

### Usage

Download AITQE model from [here](https://huggingface.co/No9242/aitqe), and run the following command:

```bash
python inference.py --model_path /path/to/aitqe --gpu_id 0 --image_path ./test.png --caption "Some random text to the image like this is a test"
```

If you want to use AITQE to output only overall score (and possiblely the rewritten caption), add '--overall_only':

```bash
python inference.py --model_path /path/to/aitqe --gpu_id 0 --overall_only --image_path ./test.png --caption "Some random text to the image like this is a test"
```

If you encounter difficulties connecting to Hugging Face when running the code, you may manually download the Qwen2-7B and siglip used in AITEQ, and specify the path to the language model and vision encoder in the 'config.json' file in the aitqe model folder:


```bash
https://huggingface.co/Qwen/Qwen2-7B
https://huggingface.co/google/siglip-so400m-patch14-384
```
