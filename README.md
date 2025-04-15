
#  MelodAI - MIDI Music Generation with GPT

This project uses a GPT-style transformer to generate symbolic music based on MIDI data, using the `miditok` library and Magenta's classical datasets. This guide walks you through setting up the environment using **WSL (Windows Subsystem for Linux)**.

---

##  WSL Setup Instructions

### 1. Install WSL (if not already installed)

Open PowerShell as Administrator and run:

```bash
wsl --install
```

> If you're already using WSL1, you can upgrade to WSL2 with:
> ```bash
> wsl --set-default-version 2
> ```

Then restart your machine if prompted.

### 2. Open WSL and Update Your Linux Distro

```bash
sudo apt update && sudo apt upgrade -y
```

---

##  Python Environment Setup

### 3. Install Python and pip (if not available)

```bash
sudo apt install python3 python3-pip python3-venv -y
```

### 4. Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 5. Create and Activate a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

> If you see permission errors, try:  
> `chmod +x venv/bin/activate`

---

##  Install Dependencies

### 6. Install Python Packages

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

---

##  Directory Structure (Typical)

```
project/
├── data/                  # MIDI files
├── outputs/               # Model outputs
├── checkpoints/           # Saved models
├── tokenizer_configs/     # Miditok tokenizer files
├── venv/                  # Python virtual environment
├── .gitignore
├── requirements.txt
└── main.ipynb             # Training or generation notebook
```
---
##  Download the MAESTRO Dataset

Download the **MAESTRO** dataset from the official Magenta site:

🔗 [https://magenta.tensorflow.org/datasets/maestro](https://magenta.tensorflow.org/datasets/maestro)

Once downloaded, extract the contents into the following directory path:

```bash
MelodAI/
└── data/
    └── maestro/
        └── maestro-v3.0.0/
            ├── 2004/
            │   ├── MIDI-Unprocessed_04_R1_2004_01.mid
            │   └── ...
            ├── 2006/
            └── ...
```
---

##  Running the Project

Use Jupyter, VS Code, or run scripts directly in terminal.

### Launch Jupyter (inside venv):

```bash
pip install notebook
jupyter notebook
```

---

##  Notes

- Ensure all MIDI files are placed in the `data/` folder.
- Use `tokenizer.train()` if building a new tokenizer from scratch.
- Save your trained tokenizer and model for reuse.

---

##  Deactivating the Environment

```bash
deactivate
```

---

##  License

MIT License. See `LICENSE` for details.
```

