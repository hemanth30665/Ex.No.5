# Ex.No.5 — Comparing Prompting Techniques Through Engineering Problem-Solving Scenarios

NAME: JANDA HEMANTH

REGISTER NUMBER: 212223030015



---

## Aim

To compare different prompting techniques and evaluate their effectiveness in solving a real-world engineering problem selected from a final-year project, and to analyze how prompt structure affects relevance, accuracy, completeness, clarity, feasibility, and usefulness of AI-generated solutions.

**AI Tools Required:** ChatGPT, Claude, Gemini (any two or more available AI tools; ChatGPT used as primary for the naive-vs-basic comparison per experiment guidelines).

---

## Experiment Overview

A genuine problem from an ongoing/completed final-year project is given to an AI system using multiple prompting techniques — starting from a plain, unstructured prompt and progressing to structured, technique-driven prompts. The generated responses are compared on defined evaluation criteria, and the best-performing technique is identified and refined into a final prompt. The experiment also demonstrates **prompt chaining**, where a complex engineering problem is broken into a sequence of connected prompts, each building on the previous stage's output.

---

## Step 1 — Project Title and Problem Statement

**Project Title:** Crop Disease Detection using Computer Vision and Deep Learning

**Problem Statement:** Farmers often detect crop diseases too late, using manual visual inspection, resulting in reduced yield and excessive/incorrect pesticide use. The project aims to build a computer-vision-based system that detects crop diseases early from leaf images captured via smartphone or field camera, and recommends corrective action, enabling faster and more accurate intervention.

**Selected Engineering Scenario:** Detecting and classifying plant leaf diseases (e.g., blight, rust, mildew) from images using a CNN-based classification pipeline suitable for deployment on a low-power edge device in the field.

---

## Step 2 — Base Prompt (Naive Prompt)

> "Suggest a method to detect crop diseases using computer vision."

This prompt is short, unstructured, gives no context about the dataset, deployment environment, project scope, or constraints.

---

## Step 3 — Applying Different Prompting Techniques

### Technique 1 — Straightforward / Basic Prompt
*(Adds minimal project context but no advanced structuring)*

> "I am building a final-year project to detect crop diseases from leaf images using deep learning. Suggest a suitable computer vision method, including the model architecture and dataset considerations."

### Technique 2 — Persona Pattern

> "You are a computer vision research engineer specializing in agricultural AI applications. A final-year student wants to detect crop diseases from leaf images using a low-cost embedded camera. Recommend a complete technical approach, including model choice, dataset, and deployment considerations, explained the way you would mentor a student."

### Technique 3 — Chain of Thought Prompt

> "A final-year student wants to detect crop diseases from leaf images using a low-power embedded device with limited compute. Think step by step: first consider the type of image data and possible diseases, then compare CNN architectures suitable for low-power deployment (e.g., MobileNet vs. EfficientNet-lite), then reason about the dataset and augmentation needs, then propose an end-to-end pipeline with justification for each choice."

### Technique 4 — Few-Shot Prompt

> "Example 1 — Problem: 'Detect skin disease from photos on a mobile app.' → Approach: 'Use a MobileNetV2 transfer-learning model, train on a labeled dermatology dataset, deploy via TensorFlow Lite on-device.' Example 2 — Problem: 'Detect defective parts on a factory conveyor belt using a camera.' → Approach: 'Use a lightweight CNN (e.g., ResNet18) with real-time inference on an edge GPU, trained on labeled defect images with augmentation for lighting variation.' Now solve: Problem: 'Detect crop diseases from leaf images using a low-power embedded camera in the field.'"

### Technique 5 — Reverse Prompting

> "I want to build a crop disease detection system for my final-year project using computer vision, but I haven't finalized the dataset, hardware, or target crop yet. What are the key questions I should answer before choosing a model architecture and deployment method?"

---

## AI-Generated Outputs (Summary)

| Technique | Summary of ChatGPT/Claude Response |
|---|---|
| Naive Prompt | Gave a generic answer: "use CNNs, train on labeled leaf images, use frameworks like TensorFlow/PyTorch." No architecture recommendation, no dataset name, no deployment consideration. |
| Basic Prompt | Recommended CNN transfer learning (e.g., ResNet/VGG), mentioned the PlantVillage dataset, and briefly noted data augmentation — more specific but still generic on deployment. |
| Persona | Recommended MobileNetV2/EfficientNet-Lite for low-power devices, named PlantVillage as a starting dataset, and added mentoring-style tips on avoiding overfitting on lab-condition images vs. real field images. |
| Chain of Thought | Reasoned explicitly through: data type → model comparison (MobileNet vs. EfficientNet-lite, favoring MobileNet for lower compute) → augmentation strategy (brightness/rotation/blur to simulate field conditions) → full pipeline (capture → preprocess → inference → alert). Most technically justified response. |
| Few-shot | Correctly followed the example format and proposed a lightweight CNN (MobileNet-class model) with TensorFlow Lite deployment — consistent with the pattern shown but slightly less detailed reasoning than CoT. |
| Reverse Prompting | Produced a strong requirement-gathering checklist: target crop/disease list, image acquisition hardware, field vs. lab lighting conditions, available compute at deployment, need for offline inference, dataset availability/licensing. |

---

## Naive vs. Basic Prompt — Focused Comparison (ChatGPT)

| Criterion | Naive Prompt Output | Basic Prompt Output |
|---|---|---|
| Quality | Generic, textbook-level answer | More applied, project-specific |
| Accuracy | Technically correct but shallow | Correct and more specific (named dataset, transfer learning) |
| Depth | Low — no architecture or dataset named | Medium — architecture family and dataset named, deployment not addressed |

**Does ChatGPT consistently give better results with basic prompts?** Yes, for this scenario — adding even minimal project context (goal, data type, "final-year project") measurably improved specificity and relevance, since the naive prompt gave no constraints for the model to reason against.

**Are there scenarios where naive prompts work equally well?** Yes — for very well-defined, single-fact questions (e.g., "What is a confusion matrix?"), the naive prompt performed equally well since no additional context could change a factual definition. The gap widens specifically for **open-ended design/recommendation problems**, like this one, where missing context forces the model to answer generically.

---

## Comparison / Evaluation Table (All Techniques)

Rated 1–5 on each criterion.

| Technique | Relevance | Accuracy | Completeness | Clarity | Feasibility | Usefulness | Total (/30) |
|---|---|---|---|---|---|---|---|
| Naive Prompt | 2 | 3 | 2 | 3 | 3 | 2 | 15 |
| Basic Prompt | 3 | 4 | 3 | 4 | 4 | 3 | 21 |
| Persona | 4 | 4 | 4 | 5 | 4 | 4 | 25 |
| Chain of Thought | 5 | 5 | 5 | 4 | 5 | 5 | 29 |
| Few-shot | 4 | 4 | 4 | 4 | 4 | 4 | 24 |
| Reverse Prompting | 4 | 4 | 4 | 5 | 5 | 5 | 27 |

---

## Analysis and Observations

- Moving from the **naive prompt** to even a **basic prompt** (adding project context) produced a noticeable jump in accuracy and completeness — confirming that context, not just wording, drives output quality.
- **Chain of Thought** produced the most technically justified and feasible solution, because the problem requires comparing trade-offs (model size vs. accuracy vs. power) rather than recalling a single fact.
- **Reverse Prompting** was most useful at the *planning* stage of the project — before the architecture is even chosen — since it surfaced constraints (field lighting, compute limits, dataset licensing) the student had not yet considered.
- **Persona Pattern** improved clarity most, framing the answer as mentorship rather than a list of facts, which is valuable for a student encountering the domain for the first time.
- **Few-shot** was reliable and consistent but slightly less deep than Chain of Thought, since it optimized for matching the example format rather than reasoning from first principles.
- Across techniques, prompt clarity and specificity (stating the deployment constraint — "low-power embedded device" — explicitly) was the single biggest factor separating a generic answer from a genuinely useful, feasible engineering recommendation.

---

## Final Selected Prompting Technique

**Chain of Thought**, combined with elements of the Persona pattern for explanatory clarity, was selected as the most effective technique for this problem, since the task is a multi-factor engineering trade-off decision rather than a simple lookup.

### Refined / Final Prompt

> "You are a computer vision engineer mentoring a final-year student. The student is building a crop disease detection system that must run on a low-power embedded camera in the field (limited compute, variable lighting, no reliable internet). Think step by step: (1) identify the image characteristics and likely disease classes to handle, (2) compare at least two lightweight CNN architectures suitable for on-device inference, (3) recommend a dataset and necessary augmentation for real field conditions, (4) propose a complete pipeline from image capture to alert generation, and (5) note the main risks or failure cases to test for. Justify each choice briefly."

---

## Engineering Validation

The refined prompt's recommendation (MobileNetV2/EfficientNet-Lite with TensorFlow Lite deployment, trained on PlantVillage plus field-condition augmentation) was cross-checked against the project's actual constraints:
- **Hardware:** Confirmed the target embedded board (e.g., Raspberry Pi / ESP32-CAM class device) can run a quantized MobileNet-class model within acceptable inference latency.
- **Dataset:** Verified PlantVillage is publicly available and license-permitted for academic project use, with augmentation needed to bridge the lab-image-to-field-image gap, as the AI correctly flagged.
- **Feasibility:** The proposed pipeline (capture → preprocess → on-device inference → alert) matches the project's offline/low-connectivity requirement.

This confirms the AI-recommended approach is technically sound and implementable within the project's real-world constraints.

---

## Conclusion

Comparing prompting techniques on a genuine final-year engineering problem (crop disease detection using computer vision) showed that prompt structure has a direct, measurable effect on the quality of AI-generated engineering solutions. Naive prompts produced shallow, generic answers; adding context (basic prompt) improved specificity; and structured techniques — especially Chain of Thought and Reverse Prompting — produced solutions that were more accurate, complete, and directly usable for real project decisions. The experiment confirms that engineers should invest in prompt structuring, particularly for open-ended design problems, rather than accepting the first generic response.

---

## Prompt Chaining Demonstration

To further illustrate how a complex engineering problem can be solved through a connected sequence of prompts (prompt chaining), the same crop disease detection project was carried through the following chain:

```
Problem
   ↓
Requirement Analysis
   ↓
Architecture
   ↓
Algorithm
   ↓
Flowchart
   ↓
Python Code
   ↓
Testing
   ↓
Documentation
```

| Stage | Example Prompt |
|---|---|
| 1. Problem | "Define the problem of detecting crop diseases from leaf images for a final-year embedded computer vision project." |
| 2. Requirement Analysis | "Based on this problem, list the functional and non-functional requirements — accuracy target, inference speed, power budget, offline operation." |
| 3. Architecture | "Design a system architecture showing camera module, edge inference unit, and alert/output module for this crop disease detection system." |
| 4. Algorithm | "Propose the classification algorithm/model (e.g., MobileNetV2 transfer learning) and explain the training and inference steps." |
| 5. Flowchart | "Represent the end-to-end process — image capture, preprocessing, inference, alert generation — as a flowchart." |
| 6. Python Code | "Write Python code to load a trained MobileNetV2 model and classify a leaf image, outputting the predicted disease class." |
| 7. Testing | "Suggest a test plan to validate the model's accuracy on field-condition images, including edge cases like poor lighting and blurred images." |
| 8. Documentation | "Generate a short technical documentation summary covering the problem, architecture, model, and test results for the project report." |

**Observation:** Each stage's output was used as direct input/context for the next prompt, allowing the AI to maintain consistency across the requirement analysis, design, implementation, and testing stages — demonstrating how prompt chaining decomposes a large engineering project into manageable, connected AI-assisted steps.

---

## Output / Result

**RESULT:** The prompts for the selected engineering problem (Crop Disease Detection using Computer Vision) were executed successfully across naive, basic, and four advanced prompting techniques. The responses were compared and evaluated on relevance, accuracy, completeness, clarity, feasibility, and usefulness, and Chain of Thought was identified as the most effective technique for this design-oriented engineering problem. A prompt-chaining sequence was also demonstrated, successfully carrying the project from problem definition through to documentation.
