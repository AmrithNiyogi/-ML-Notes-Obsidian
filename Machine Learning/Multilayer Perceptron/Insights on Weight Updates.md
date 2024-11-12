No update when ActualOutput = DesiredOutput
- Update magnitude increases as **|DesiredOutput - ActualOutput|** increases
- Update direction:
	- If AO < DO, then the update is +ve if Input is +ve else –ve → Increase AO
	- If AO > DO, then the update is -ve if Input is +ve else +ve → Decrease AO
- Input Magnitude Affects Update Size:
	- Small Input (close to 0) → Small update
	- Large Input → Large update
- Learning Factor (η) Influences Update Magnitude:
	- Large η: Fast learning, short "memory", depends on recent instances
	- Small η: Slow learning, many updates needed for convergence

$$Update = LearningFactor * (DesiredOutput - ActualOutput ) * Input$$

