# Embodied-R1: Reinforced Embodied Reasoning for General Robotic Manipulation

## 📖 Overview

**Embodied-R1** is a 3B vision-language model (VLM) designed for general robotic manipulation. Through an innovative **"Pointing"** mechanism and **Reinforced Fine-tuning (RFT)** training methodology, it effectively bridges the "seeing-to-doing" gap in robotics, achieving remarkable zero-shot generalization capabilities.

![Embodied-R1 Framework](assets/r1_framework_readme.jpg)
*Figure 1: Embodied-R1 framework overview, comprehensive performance evaluation, and zero-shot robotic manipulation demonstrations.*

---

## 🛠️ Setup

1.  **Clone the repository**:
    
    ```bash
    git clone https://github.com/iclr-submission-15454/Embodied-R1.git
    cd Embodied-R1
    ```
    
2.  **Create and activate Conda environment**:
    ```bash
    conda create -n embodied_r1 python=3.11 -y
    conda activate embodied_r1
    ```

3.  **Install dependencies for inference**:
    ```bash
    pip install transformers==4.51.3 accelerate
    pip install qwen-vl-utils[decord]
    ```

3.  **Install dependencies for training (optional)**:
    ```bash
    pip install -r requirements.txt
    ```

---

## 🚀 Inference

**Run the example code:**

~~~python
cd Embodied-R1/
python inference_example.py
~~~

### VTG Example

Task instruction: put the red block on top of the yellow block

**Before prediction (original image):**

<img src="assets/put the red block on top of the yellow block.png" width="400" alt="Original input image">

**After prediction (visualization result):**

<img src="assets/put the red block on top of the yellow block_visualized.png" width="400" alt="Visualization result with predicted points">



### RRG Example

Task instruction: put pepper in pan

**Before prediction (original image):**

<img src="assets/put pepper in pan.png" width="400" alt="Original input image">

**After prediction (visualization result):**

<img src="assets/put pepper in pan_visualized.png" width="400" alt="Visualization result with predicted points">



### REG Example

Task instruction: bring me the camel model

**Before prediction (original image):**

<img src="assets/roborefit_18992.png" width="400" alt="Original input image">

**After prediction (visualization result):**

<img src="assets/roborefit_18992_visualized.png" width="400" alt="Visualization result with predicted points">



### OFG Example

Task instruction: loosening stuck bolts

**Before prediction (original image):**

<img src="assets/handal_090002.png" width="400" alt="Original input image">

**After prediction (visualization result):**

<img src="assets/handal_090002_visualized.png" width="400" alt="Visualization result with predicted points">





---

## 📊 Evaluation

```bash
cd eval
python hf_inference_where2place.py
python hf_inference_vabench_point.py
...
```

## 🧠 Training

We plan to release the complete training code, datasets, and detailed guidelines soon. Stay tuned!
