# 🧠 Spectral Analysis of Alpha Power

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter)
![Data Analysis](https://img.shields.io/badge/Data-Analysis-green?style=for-the-badge)

---

## 📖 About The Project

This project explores the processing and analysis of **electroencephalogram (EEG) signals** using various spectral analysis techniques. The primary objective is to investigate and quantify the changes in brain wave activity—specifically within the Alpha band—between two distinct physiological states:
*   **Eyes Closed (EC)**
*   **Eyes Open (EO)**

By analyzing these states, the project demonstrates the well-known neurological phenomenon of **Alpha Desynchronization** (or Alpha Blocking), where alpha wave amplitude significantly decreases when the eyes are opened and visual processing begins.

---

## 🛠️ Project Structure & Methodology

The analysis is structured into four main phases, taking the raw EEG data from initial loading to advanced time-frequency visualization:

### 1️⃣ Loading and Visualizing the EEG Signal 📊
*   **Data Import:** Loading the raw EEG dataset.
*   **Initial Inspection:** Plotting the raw signal in the time domain to understand baseline characteristics, identify obvious artifacts, and visualize the transition between EC and EO states.

### 2️⃣ Preprocessing & Band-Pass Filtering 🎛️
*   **Noise Reduction:** Real-world EEG data is noisy. This step applies a **Band-Pass Filter (2-40 Hz)**.
*   **Isolating Frequencies:** This specific frequency range effectively removes slow-wave drifts (below 2 Hz) and high-frequency noise/muscle artifacts (above 40 Hz), isolating the crucial Alpha (8-13 Hz) and Beta (14-30 Hz) rhythms.

### 3️⃣ Spectral Analysis and IAF Calculation 📈
This core section compares three distinct mathematical approaches to calculate the **Power Spectral Density (PSD)** and pinpoint the **Individual Alpha Frequency (IAF)**:
*   **Standard FFT (Fast Fourier Transform):** The raw frequency spectrum.
*   **Smoothed FFT:** Applying smoothing windows to reduce variance and make the alpha peak more distinguishable.
*   **Welch's Method:** Averaging modified periodograms to provide a highly robust, low-variance estimate of the PSD.

### 4️⃣ Time-Frequency Analysis (Spectrogram) ⏱️
*   **Dynamic Visualization:** Moving beyond static frequency analysis, a spectrogram is generated to show how the frequency content of the EEG signal evolves *over time*.
*   **State Transitions:** This clearly visualizes the exact moments the subject opens or closes their eyes, represented by shifts in color intensity around the ~10 Hz mark.

---

## 💡 Key Expectations & Findings
Through this pipeline, we expect to clearly observe a prominent **Alpha peak (~10 Hz)** during the Eyes Closed (EC) segments, which rapidly attenuates or completely disappears during the Eyes Open (EO) segments. 

---

## 💻 Technologies Used
*   **Python**
*   **NumPy / SciPy** (Signal Processing & Filtering)
*   **Matplotlib / Seaborn** (Data Visualization)
*   **Pandas** (Data Manipulation)
