# Computer Vision Second Assignment

## Python environment

Install the project dependencies into your current Python/Jupyter environment:

```powershell
pip install -r requirements.txt
```

If you use a separate Jupyter kernel, run the command from inside that kernel's environment.
To register the current environment as a Jupyter kernel:

```powershell
python -m ipykernel install --user --name compvision-secondassignment --display-name "CompVision SecondAssignment"
```

Note: `vlm_mlx.ipynb` depends on Apple's MLX stack, which is intended for Apple Silicon/macOS and is not part of the Windows requirements.
The Lighthouse moment-retrieval notebook may also need FFmpeg available on your system path for video processing.
