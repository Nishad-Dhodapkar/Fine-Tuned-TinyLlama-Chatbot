# Fine-Tuned-TinyLlama-Chatbot

Project Overview
This project fine-tunes the TinyLlama-1.1B-Chat model on the Alpaca dataset using LoRA (Low-Rank Adaptation) to improve instruction-following and question-answering capabilities while keeping GPU requirements minimal.

Key Steps in This Project

1️⃣ Loaded the Pre-Trained TinyLlama Model

Used TinyLlama-1.1B-Chat as the base model, which is a small yet powerful open-source LLM optimized for efficiency.

2️⃣ Loaded and Preprocessed the Alpaca Dataset

Utilized the Alpaca dataset (a high-quality instruction-following dataset) to fine-tune the model.

Reformatted data into instruction-response pairs for supervised fine-tuning.

3️⃣ Optimized Memory Usage with FP16 Precision

Leveraged FP16 (half-precision floating point) to reduce memory consumption and speed up training.

This ensures the model runs efficiently even on consumer-grade GPUs.

4️⃣ Applied LoRA for Efficient Fine-Tuning

Instead of modifying all 1.1 billion parameters, LoRA updated only key layers (q_proj and v_proj).

This drastically reduced GPU memory usage while still improving model responses.

5️⃣ Fine-Tuned the Model with LoRA Adapters

Used Hugging Face Transformers + PEFT (Parameter-Efficient Fine-Tuning) framework to train the model efficiently.

Applied CUDA acceleration for faster training while keeping hardware requirements low.


Results & Takeaways
-The fine-tuned TinyLlama model demonstrated better instruction-following compared to the base model.

-Lower memory footprint while achieving improved responses on real-world queries.

-Showcased how LoRA fine-tuning can adapt models quickly without full retraining.
