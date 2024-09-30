# AITQE

### Requirements

```bash
pip install -r requirements.txt
```

### Usage

The aitqe model can be downloaded from [here](https://huggingface.co/No9242/aitqe).

```bash
python inference.py --image_path ./test.png --caption "Some random text to the image like this is a test" --model_path ./path/to/aitqe --gpu_id 0
```

If you want to use aitqe to output only overall score (and possiblely the rewritten caption), you can use the following command:

```bash
python inference.py --image_path ./test.png --caption "Some random text to the image like this is a test" --model_path ./path/to/aitqe --gpu_id 0 --overall_only
```

You may need to download the language model used in the aitqe, and vision encoder used in the aitqe, 

```bash
https://huggingface.co/Qwen/Qwen2-7B
https://huggingface.co/google/siglip-so400m-patch14-384
```

and specify the path to the language model and vision encoder in the config.json file in the aitqe model folder.

