# Ex.No.5 — Comparing Prompting Techniques Through Engineering Problem-Solving Scenarios

# NAME: JANDA HEMANTH

# REGISTER NUMBER: 212223030015

# AIM

To compare different prompting techniques and evaluate their effectiveness in solving a real-world engineering problem using an AI-based Smart Traffic Management System.

---

# AI TOOLS REQUIRED

- ChatGPT

---

# EXPERIMENT OVERVIEW

In this experiment, an engineering problem related to an **AI-Based Smart Traffic Management System** is selected. The same problem is provided to ChatGPT using different prompting techniques.

The generated responses are compared based on:

- Quality
- Accuracy
- Depth
- Relevance
- Completeness
- Clarity
- Feasibility
- Usefulness

The purpose of the experiment is to understand how changing the prompt structure affects the quality of the AI-generated engineering solution.

---

# SELECTED ENGINEERING SCENARIO

## Project Title

**AI-Based Smart Traffic Management System**

## Problem Statement

Traditional traffic signals generally use fixed timing and may not respond effectively to changing traffic conditions. This can result in unnecessary waiting time, congestion, and inefficient traffic flow.

The proposed system uses cameras or sensors to collect real-time traffic information. AI techniques can then analyze vehicle density and assist in dynamically adjusting traffic signal timings.

---

# STEP 1 – BASE PROBLEM

> How can AI be used to reduce traffic congestion?

This is the basic engineering problem given to ChatGPT.

---

# STEP 2 – NAÏVE PROMPT

## Prompt

> Tell me about AI traffic systems.

## ChatGPT Output

AI traffic systems use technologies such as sensors, cameras, machine learning, and data analysis to monitor and manage traffic. They can detect vehicles, estimate traffic density, control traffic signals, identify congestion, and support intelligent transportation.

## Evaluation

| Criteria | Rating |
|---|---|
| Quality | Good |
| Accuracy | Good |
| Depth | Low |
| Relevance | Moderate |

## Observation

The response provides general information but does not focus on a specific engineering solution. The prompt is too broad.

---

# STEP 3 – BASIC PROMPT

## Prompt

> Suggest a method for using AI to detect traffic density and dynamically control traffic signals at a city intersection. Explain the main steps involved.

## ChatGPT Output

An AI-based traffic management system can use cameras or sensors to collect information about the number of vehicles on each road. Computer vision techniques can detect and count vehicles, while an AI or rule-based decision system can estimate traffic density.

The system can classify traffic as low, medium, or high density and assign different signal durations. For example, roads with higher traffic density can receive longer green-signal durations.

## Evaluation

| Criteria | Rating |
|---|---|
| Quality | Very Good |
| Accuracy | Very Good |
| Depth | Good |
| Relevance | Excellent |

## Observation

The basic prompt gives ChatGPT clearer information about the required task and therefore produces a more relevant engineering response.

---

# STEP 4 – STRAIGHTFORWARD PROMPT

## Prompt

> Explain how an AI-based Smart Traffic Management System can reduce traffic congestion. Include vehicle detection, traffic-density estimation, and dynamic signal control.

## ChatGPT Output

The system can use cameras to detect and count vehicles at an intersection. The collected information is processed to estimate traffic density. Based on the density, the AI system can determine appropriate signal timings and provide longer green times to roads with higher traffic.

## Evaluation

| Criteria | Rating |
|---|---|
| Quality | Very Good |
| Accuracy | Excellent |
| Depth | Good |
| Clarity | Excellent |

---

# STEP 5 – ROLE-BASED PROMPT

## Prompt

> Act as an experienced intelligent transportation systems engineer. Design a practical approach for an AI-based traffic management system that detects vehicle density and dynamically controls traffic signals. Explain the sensors, AI processing, decision-making process, and expected benefits.

## ChatGPT Output

A practical system can use traffic cameras or roadside sensors to collect real-time vehicle information. A computer vision module can detect and count vehicles, while the processing unit estimates traffic density for each lane.

The control algorithm can assign signal duration according to traffic conditions. The system should also consider minimum and maximum green times to prevent starvation of low-traffic lanes.

## Evaluation

| Criteria | Rating |
|---|---|
| Quality | Excellent |
| Accuracy | Excellent |
| Depth | Excellent |
| Clarity | Very Good |

## Observation

Assigning an engineering persona makes the response more domain-focused and introduces practical considerations.

---

# STEP 6 – CONSTRAINT-BASED PROMPT

## Prompt

> Design an AI-based Smart Traffic Management System for a four-road intersection. Use traffic cameras as the primary input. The solution must operate in near real time, avoid permanently prioritizing one road, maintain minimum and maximum signal durations, and provide a simple implementation approach suitable for an undergraduate engineering project.

## ChatGPT Output

The system can process camera feeds to estimate vehicle counts for each road. Traffic density can then be classified into different levels. The controller can allocate green time according to density while maintaining predefined minimum and maximum limits.

To prevent one road from being ignored, the system can include a maximum waiting-time constraint. A prototype can be implemented using Python, computer vision, and a microcontroller-based traffic signal interface.

## Evaluation

| Criteria | Rating |
|---|---|
| Quality | Excellent |
| Accuracy | Excellent |
| Depth | Excellent |
| Feasibility | Excellent |

---

# STEP 7 – STRUCTURED PROMPT

## Prompt

> Design an AI-based Smart Traffic Management System using the following structure:
>
> **Problem:** Traffic congestion caused by fixed signal timing.
>
> **Input:** Camera-based vehicle detection.
>
> **Processing:** Vehicle counting and traffic-density estimation.
>
> **Decision:** Determine signal duration according to traffic density.
>
> **Constraints:** Maintain minimum and maximum green times and prevent excessive waiting on other roads.
>
> **Output:** Dynamic traffic signal timing.
>
> Explain the architecture, working process, algorithm, advantages, limitations, and future improvements.

## ChatGPT Output

### Architecture

```text
Traffic Cameras
      ↓
Image Processing
      ↓
Vehicle Detection
      ↓
Traffic Density Estimation
      ↓
AI Decision Module
      ↓
Signal Controller
      ↓
Traffic Signals
```

### Working

The cameras continuously collect traffic information. The system detects vehicles and estimates the traffic density of each road. The decision module calculates suitable signal timings while respecting predefined constraints.

### Advantages

- Adaptive signal control
- Reduced unnecessary waiting
- Real-time monitoring
- Better traffic management

### Limitations

- Camera quality affects detection.
- Poor weather may affect computer vision.
- Real-world deployment requires extensive testing.

### Future Improvements

- Emergency vehicle priority
- Traffic prediction
- Cloud-based monitoring
- Multi-intersection coordination

## Evaluation

| Criteria | Rating |
|---|---|
| Quality | Excellent |
| Accuracy | Excellent |
| Depth | Excellent |
| Structure | Excellent |

---

# STEP 8 – COMPARISON TABLE

| Prompt Type | Quality | Accuracy | Depth | Relevance | Overall |
|---|---|---|---|---|---|
| Naïve Prompt | Good | Good | Low | Moderate | Good |
| Basic Prompt | Very Good | Very Good | Good | Excellent | Very Good |
| Straightforward | Very Good | Excellent | Good | Excellent | Very Good |
| Role-Based | Excellent | Excellent | Excellent | Excellent | Excellent |
| Constraint-Based | Excellent | Excellent | Excellent | Excellent | Excellent |
| Structured | Excellent | Excellent | Excellent | Excellent | Excellent |

---

# NAÏVE VS BASIC PROMPT ANALYSIS

## Naïve Prompt

> Tell me about AI traffic systems.

The prompt is broad and does not define the exact engineering task, expected output, constraints, or target application.

Therefore, ChatGPT provides a general explanation.

## Basic Prompt

> Suggest a method for using AI to detect traffic density and dynamically control traffic signals at a city intersection. Explain the main steps involved.

The basic prompt clearly defines:

- The engineering problem
- The AI task
- The system environment
- The expected explanation

Therefore, ChatGPT produces a more focused and useful engineering response.

---

# DOES A BASIC PROMPT ALWAYS PERFORM BETTER?

Not necessarily.

For simple questions, a naïve prompt may produce an adequate response.

However, when the engineering problem requires specific requirements, constraints, architecture, or implementation details, a clearer prompt generally produces more relevant and complete results.

Therefore, prompt complexity should match task complexity.

---

# FINAL SELECTED PROMPTING TECHNIQUE

## Selected Technique

**Structured + Constraint-Based Prompting**

This combination was selected because it provides:

- Clear problem definition
- Specific inputs and outputs
- Engineering constraints
- Organized response structure
- Better implementation guidance
- Greater consistency

---

# REFINED / FINAL PROMPT

> Act as an intelligent transportation systems engineer. Design a practical AI-based Smart Traffic Management System for a four-road city intersection.
>
> **Problem:** Fixed-time traffic signals cause unnecessary waiting and congestion.
>
> **Input:** Real-time camera-based vehicle detection and vehicle counts.
>
> **Processing:** Detect vehicles, estimate traffic density, and classify each road as low, medium, or high traffic.
>
> **Decision:** Dynamically assign signal durations based on traffic density.
>
> **Constraints:** Maintain minimum and maximum green times, prevent starvation of low-traffic roads, and provide a feasible solution for an undergraduate engineering project.
>
> **Output:** Explain the system architecture, working principle, algorithm, hardware/software requirements, advantages, limitations, and future scope. Present the architecture and algorithm clearly using headings and tables where appropriate.

---

# ENGINEERING VALIDATION

The proposed approach should be validated using simulated or real traffic data.

### Validation Parameters

- Vehicle detection accuracy
- Traffic-density estimation accuracy
- Average waiting time
- Queue length
- Signal response time
- Traffic throughput

### Validation Process

```text
Traffic Data
     ↓
Vehicle Detection
     ↓
Density Calculation
     ↓
Dynamic Signal Decision
     ↓
Measure Waiting Time
     ↓
Compare With Fixed Signals
```

The AI-generated solution should be treated as a design proposal and validated through simulation, testing, or real-world engineering measurements before deployment.

---

# ANALYSIS AND OBSERVATIONS

- The naïve prompt produced a general response because it lacked specific requirements.
- The basic prompt produced a more relevant engineering solution.
- Role-based prompting improved domain-specific reasoning.
- Constraint-based prompting introduced practical engineering limitations.
- Structured prompting produced the clearest and most organized response.
- Combining structure with constraints resulted in the most useful solution for the selected engineering problem.
- AI-generated solutions still require engineering validation before practical implementation.

---

# RESULT

The same Smart Traffic Management problem was successfully evaluated using different prompting techniques. The experiment demonstrated that prompt clarity, context, role definition, constraints, and output structure significantly influence the quality, accuracy, and depth of ChatGPT's engineering responses.

---

# CONCLUSION

The experiment shows that better-designed prompts generally produce more focused and useful engineering solutions. Naïve prompts are suitable for simple general questions, while structured and constraint-based prompts are more effective for complex engineering problems. For the selected Smart Traffic Management System, **Structured + Constraint-Based Prompting** produced the most comprehensive and practical response.

## Output / Result

**RESULT:** The prompts for the selected engineering problem (Crop Disease Detection using Computer Vision) were executed successfully across naive, basic, and four advanced prompting techniques. The responses were compared and evaluated on relevance, accuracy, completeness, clarity, feasibility, and usefulness, and Chain of Thought was identified as the most effective technique for this design-oriented engineering problem. A prompt-chaining sequence was also demonstrated, successfully carrying the project from problem definition through to documentation.
