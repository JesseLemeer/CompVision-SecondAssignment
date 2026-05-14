# Computer Vision Second Assignment

This repository contains our work for the second Computer Vision assignment.

The goal of the project is to summarize videos from the TVSum dataset. We first use a Vision-Language Model to find important events in each video. Then we use pretrained moment retrieval models to find the video timestamps that match those events. In the end, we create short video summaries from the selected moments.

## Main Notebook

The complete pipeline is in:

```text
notebooks/end_to_end_pipeline.ipynb
```

This notebook contains both main parts of the project:

1. Step 3: event prediction with a VLM.
2. Step 4: moment retrieval with pretrained models.

The older separated notebooks are kept in:

```text
notebooks/archive/
```

## Repository Structure

```text
data/TVSum/                              Input videos used in the assignment.
data/annotations/                        Human annotations for the videos.
models/                                  Pretrained model checkpoints.
cache/                                   Generated video chunks.
outputs/intermediate/vlm_outputs/        Raw VLM experiment outputs.
outputs/intermediate/vlm_outputs/vlm_final_prediction/
                                         Final Step 3 event predictions.
outputs/intermediate/retrieval_outputs/  Step 4 retrieval CSV outputs.
outputs/final/                           Final text and video summaries.
notebooks/                               Main and archived notebooks.
requirements.txt                         Python package requirements.
```

## Setup

Use Python `<3.10`, for example Python 3.9. The Python version requirement is documented here instead of in `requirements.txt` because `pip` cannot install or enforce the interpreter version from that file.

Install the required packages with:

```powershell
pip install -r requirements.txt
```

## How to Run

1. Open `notebooks/end_to_end_pipeline.ipynb`.
2. Run the setup cells first.
3. Run the Step 3 cells to generate or inspect the VLM event predictions.
4. Run the Step 4 cells to perform moment retrieval.
5. Check the final text and video summaries in `outputs/final/`.

The final summary files are named like this:

```text
outputs/final/video_5_retrieval_summary.txt
outputs/final/video_5_retrieval_summary.mp4
```

The same format is used for videos 6, 7, and 8.
