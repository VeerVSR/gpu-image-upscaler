<h1>🚀 GPU Image Upscaler (Real-ESRGAN)</h1>

<p>
A <strong>GPU-based image upscaling project</strong> built using
<strong>Real-ESRGAN</strong>, <strong>PyTorch CUDA</strong>, and
<strong>BasicSR</strong>.  
This project focuses on <em>stable, reproducible, and beginner-friendly</em>
GPU inference on Windows systems.
</p>

<hr/>

<h2>✨ Features</h2>
<ul>
  <li>✅ GPU-accelerated image upscaling (CUDA)</li>
  <li>✅ Real-ESRGAN <strong>x4</strong> super-resolution</li>
  <li>✅ Tested on NVIDIA GTX 1650 (4 GB VRAM)</li>
  <li>✅ Safe tiling to prevent VRAM crashes</li>
  <li>✅ Jupyter Notebook workflow</li>
  <li>✅ Clean virtual environment & dependency pinning</li>
</ul>

<hr/>

<h2>📁 Project Structure</h2>

<pre>
gpu-image-upscaler/
│
├── input/
│   └── test.jpg
│
├── output/
│   └── (generated images)
│
├── models/
│   └── RealESRGAN_x4plus.pth   (download separately)
│
├── upscalar_GPU.ipynb
├── requirements.txt
├── .gitignore
└── README.md
</pre>

<hr/>

<h2>🖼️ Sample Input</h2>

<p>
The repository includes a sample input image:
</p>

![Input Image](https://raw.githubusercontent.com/VeerVSR/gpu-image-upscaler/HEAD/input/test.jpg)
<hr/>

<h2>🧰 Requirements</h2>

<ul>
  <li>Python <strong>3.10</strong></li>
  <li>NVIDIA GPU (tested on GTX 1650)</li>
  <li>CUDA <strong>11.8</strong></li>
  <li>Windows 10 / 11</li>
</ul>

<hr/>

<h2>⚙️ Setup Instructions</h2>

<h3>1️⃣ Create Virtual Environment</h3>

<pre>
python -m venv venv
venv\Scripts\activate
</pre>

<h3>2️⃣ Install Dependencies</h3>

<pre>
pip install -r requirements.txt
</pre>

<hr/>

<h2>📥 Download Model</h2>

<p>
Download the official Real-ESRGAN x4 model:
</p>

<p>
<a href="https://github.com/xinntao/Real-ESRGAN/releases" target="_blank">
https://github.com/xinntao/Real-ESRGAN/releases
</a>
<a href="https://huggingface.co/lllyasviel/Annotators/blob/main/RealESRGAN_x4plus.pth" target="_blank">
https://huggingface.co/lllyasviel/Annotators/blob/main/RealESRGAN_x4plus.pth
</a>
</p>

<p>
Place the file here:
</p>

<pre>
models/RealESRGAN_x4plus.pth
</pre>

<hr/>

<h2>▶️ Run the Upscaler</h2>

<p>
Open the Jupyter notebook:
</p>

<pre>
upscalar_GPU.ipynb
</pre>

<p>
Run the cells in order:
</p>

<ol>
  <li>Verify CUDA availability</li>
  <li>Load the Real-ESRGAN model</li>
  <li>Upscale the input image</li>
  <li>Save output to the <code>output/</code> folder</li>
</ol>

<p>
During execution, GPU usage can be verified using:
</p>

<pre>
nvidia-smi
</pre>

<hr/>

<h2>⚠️ Important Notes</h2>

<ul>
  <li>FP16 (<code>half=True</code>) is <strong>disabled</strong> to avoid black outputs on GTX 1650</li>
  <li>NumPy is pinned to <strong>1.26.4</strong> for compatibility</li>
  <li>Model files (<code>.pth</code>) are ignored by Git</li>
  <li>Each project should use its own virtual environment</li>
</ul>

<hr/>

<h2>📌 Why This Project Exists</h2>

<p>
This repository documents a <strong>real-world, end-to-end journey</strong> of:
</p>

<ul>
  <li>Setting up CUDA correctly on Windows</li>
  <li>Handling NumPy / PyTorch compatibility issues</li>
  <li>Using Real-ESRGAN correctly (no fake APIs)</li>
  <li>Building a reproducible AI project</li>
</ul>

<p>
It is intentionally <strong>explicit and verbose</strong> to help beginners avoid
common pitfalls.
</p>

<hr/>

<h2>🛣️ Future Improvements</h2>

<ul>
  <li>Batch folder upscaling</li>
  <li>x4 → x8 safe multi-pass pipeline</li>
  <li>Command-line interface</li>
  <li>Windows GUI application</li>
  <li>Video upscaling</li>
</ul>

<hr/>

<h2>👤 Author</h2>

<p>
<strong>Veer VSR</strong><br/>
GitHub: <a href="https://github.com/VeerVSR" target="_blank">@VeerVSR</a>
</p>

<hr/>

<p>
⭐ If you found this project useful, consider starring the repository!
</p>
