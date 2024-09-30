# AITQE

### Requirements

```bash
pip install -r requirements.txt
```

### Usage

Download AITQE model from [here](https://huggingface.co/No9242/aitqe).

Run the following command to get the overall score (and possibly the rewritten caption):

```bash
python inference.py \
       --model_path /path/to/aitqe \
       --gpu_id 0 \
       --image_path ./test.png \
       --caption "Some random text to the image like this is a test"
```

If you want AITQE to output all scores and explanations, add '--output_all':

```bash
python inference.py \
       --model_path /path/to/aitqe \
       --gpu_id 0 \
       --output_all \
       --image_path ./test.png \
       --caption "Some random text to the image like this is a test"
```

If you encounter difficulties connecting to HuggingFace when running the code, you may manually download the [Qwen/Qwen2-7B](https://huggingface.co/Qwen/Qwen2-7B) and [google/siglip-so400m-patch14-384](https://huggingface.co/google/siglip-so400m-patch14-384) used in AITEQ, and specify the path in the 'config.json' file in the aitqe model folder.

