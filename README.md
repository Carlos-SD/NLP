# NLP

This repository contains all materials, notebooks, datasets, and projects developed throughout the NLP course.  
Each session has its own dedicated folder containing activities, practice notebooks, and mini-projects.

---

## Environment with Conda (step by step)

### 1. Have Conda on your machine

- **If you already have Conda (Anaconda or Miniconda):** run `conda --version` in a terminal. If it prints a version, go to step 2.
- **If you don't have Conda:** install [Miniconda](https://docs.conda.io/en/latest/miniconda.html): **macOS** — download the installer for your chip (Apple Silicon or Intel) and run it; **Windows** — download the Windows installer (.exe), run it, and follow the setup (you can use "Anaconda Prompt" or a terminal where Conda was added to PATH). When done, close and reopen your terminal.

### 2. Initialize Conda in the terminal

In each new terminal (especially the editor's integrated one), load Conda with one of these commands:

```bash
source ~/.zshrc
```

or, using the direct path:

```bash
source ~/miniconda3/etc/profile.d/conda.sh
```

(On Windows with Anaconda Prompt this is not needed; Conda is already active.)

### 3. Create the environment from `environment.yaml`

From the repository root (where `environment.yaml` is):

```bash
conda env create -f environment.yaml
conda activate icesi-nlp
```

### 4. If the environment kernel doesn't show up in the editor

In some editors (e.g. Cursor) the environment kernel may not appear in the list. With **icesi-nlp** activated (`conda activate icesi-nlp`), run:

```bash
python -m ipykernel install --user --name=icesi-nlp --display-name="Python (icesi-nlp)"
```

Then in the notebook choose **Select Kernel** → **Python (icesi-nlp)**. If it still doesn't appear, use **Enter interpreter path...** and paste the path to the env's Python (e.g. `~/miniconda3/envs/icesi-nlp/bin/python`).

---

## Running the notebooks

You can run the notebooks in two ways:

### Option A: From your editor (Cursor, VS Code, etc.)

1. Open a `.ipynb` file in the editor.
2. Select the **icesi-nlp** kernel: **Select Kernel** → **Python (icesi-nlp)** (or pick the interpreter for that environment if it appears in the list).
3. Run cells as usual. The editor uses the Conda environment kernel.

### Option B: In the browser with Jupyter

With the **icesi-nlp** environment activated:

**JupyterLab** (included in the environment):

```bash
conda activate icesi-nlp
jupyter lab
```

The browser will open; navigate to the session folder (e.g. `1-Sesion-activity`) and open the notebook. Choose the kernel **Python (icesi-nlp)** if prompted.

**Jupyter Notebook** (classic interface; install first if needed):

```bash
conda activate icesi-nlp
pip install notebook
jupyter notebook
```

Then open the notebook in the browser and select the **icesi-nlp** kernel.

---

## 📁 Repository Structure

```
├── 1-Sesion-activity
│   ├── 6-Practice-NLP-Basics.ipynb
│   ├── ProductsReview.csv
│   ├── Sentiment-Analysis.ipynb
│   └── three_little_pigs.txt
│
├── 2-Sesion-activity
│   └── Languages_LSTM.ipynb
│
├── 3-sesion-activity
│   └── transformer_lang_id.ipynb
│
├── 4-sesion-activity
│   └── BERT_Classification.ipynb
│
├── 5-sesion-activity
│   └── GPT-2_Text_Generation.ipynb
│
├── 6-sesion-activiy
│   └── Qwen-Hotpot-RAG.ipynb
│
├── README.md
├── environment.yaml
└── requirements.txt
```

---
