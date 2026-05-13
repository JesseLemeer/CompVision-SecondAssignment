# Computer Vision Second Assignment

This repository contains our work for the second Computer Vision assignment.

The goal of the project is to summarize videos from the TVSum dataset. We first use a Vision-Language Model to find important events in each video. Then we use pretrained moment retrieval models to find the video timestamps that match those events. In the end, we create short video summaries from the selected moments.

## Main Notebook

The complete pipeline is in:

```text
end_to_end_pipeline.ipynb
```

This notebook contains both main parts of the project:

1. Step 3: event prediction with a VLM.
2. Step 4: moment retrieval with pretrained models.

The older separated notebooks are kept in:

```text
seperate_notebooks/
```

## Repository Structure

```text
TVSum/                 Input videos used in the assignment.
annotations/           Human annotations for the videos.
models/                Pretrained model checkpoints.
vlm_outputs/           Raw VLM experiment outputs.
vlm_final_prediction/  Final event predictions 
outputs/               retrieval and Summary results
seperate_notebooks/    Original separate notebooks 
end_to_end_pipeline.ipynb
requirements.txt
```

## Setup

We used Python with Jupyter Notebook.

Install the required packages with:

```powershell
pip install -r requirements.txt
```


## How to Run

1. Open `end_to_end_pipeline.ipynb`.
2. Run the setup cells first.
3. Run the Step 3 cells to generate or inspect the VLM event predictions.
4. Run the Step 4 cells to perform moment retrieval.
5. Check the final text and video summaries in the `outputs/` folder.

The final summary files are named like this:

```text
outputs/video_5_retrieval_summary.txt
outputs/video_5_retrieval_summary.mp4
```

The same format is used for videos 6, 7, and 8.
