# recursive-ai-improver
When AI Starts Designing AI

## 1. Problem Statement

Modern AI development still relies heavily on humans to manually design algorithms, write code, and iteratively improve systems.  
As large language models become capable of writing and reasoning about code, a natural question emerges:

What happens when AI systems start improving other AI systems, or themselves, in a recursive loop?

This project explores a minimal and controlled setup where:
- One AI generates code
- Another AI evaluates that code
- The system iteratively refines the output based on explicit evaluation criteria

The purpose of this project is not to maximize performance, but to understand:
- Where recursive improvement works
- Where it breaks down
- Where human intervention remains necessary

---

## 2. System Overview

The system is composed of two distinct AI roles operating in a loop:

[Problem Specification]  
→ Generator AI  
→ Generated Code  
→ Evaluator AI  
→ Scores and Feedback  
→ Refined Code  
→ Repeat for several iterations

Humans do not intervene during each iteration.  
Instead, humans are responsible for:
- Defining the problem
- Designing the evaluation criteria
- Deciding when the improvement loop should stop

---

## 3. Evaluation Criteria

Each iteration is evaluated using human-defined criteria.  
These criteria determine what the system considers an improvement.

The evaluation focuses on:
1. Correctness  
   Whether the code solves the stated problem.
2. Efficiency  
   Time and space complexity where applicable.
3. Robustness  
   Handling of edge cases and failure scenarios.
4. Readability and maintainability  
   Whether a human can reasonably understand and maintain the code.

The evaluation criteria remain fixed throughout an experiment, highlighting the role of humans in defining what counts as progress.

---

## 4. Experiments and Iterations

The system was run for multiple improvement loops, typically between three and five iterations.

Each iteration records:
- The generated code version
- Evaluation scores
- Qualitative feedback from the evaluator
- Observed regressions or unexpected behavior

Across experiments, several patterns emerged:
- Improvements often plateau after a small number of iterations
- Optimization in one dimension may degrade performance in another
- The system can optimize for evaluation metrics without improving real robustness

Detailed iteration logs are stored in the experiments directory.

---

## 5. Results

Observed improvements include:
- Clearer code structure
- Incremental optimizations when evaluation criteria are well aligned
- Correction of obvious logical errors

Observed limitations include:
- Weak handling of rare or implicit edge cases
- Limited ability to perform long-term strategic improvements
- Difficulty understanding unstated human intent

Overall, recursive improvement appears locally effective but globally fragile.

---

## 6. Failure Modes and Risks

The experiments highlight several risks inherent in recursive AI systems:
- Metric optimization without real-world safety guarantees
- Divergence caused by small changes in evaluation criteria
- Unclear responsibility when failures occur
- Overconfidence based on superficial improvements

These risks are expected to scale as systems become more autonomous.

---

## 7. Human-in-the-Loop Considerations

While the system automates code generation and refinement, human involvement remains critical at several points:
- Problem formulation
- Evaluation design
- Stopping conditions
- Accountability for outcomes

In recursive improvement systems, the human role shifts from direct implementation to system design and governance.

---

## 8. Why This Project Matters

As AI systems increasingly generate code, design architectures, and optimize their own behavior, development moves away from human-written algorithms toward human-governed systems.

This project provides a small, concrete example of that transition and highlights the challenges involved.

---

## 9. Future Work

Potential extensions of this project include:
- Adaptive or dynamic evaluation criteria
- Multiple evaluators with different perspectives
- Explicit safety and alignment constraints
- Formal stopping rules and monitoring mechanisms

---

## 10. Disclaimer

This project is an exploratory experiment intended for research and educational purposes.  
It is not designed for production use without additional safety and governance layers.

---

## Author

Exploring recursive improvement, AI system design, and the role of humans in automated decision-making.
