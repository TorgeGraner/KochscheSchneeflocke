# Koch Snowflake
Draws the Koch Snowflake fractal of (theoretically) any given recursion depth in $\LaTeX$. Since $\LaTeX$ does not permit recursion, this is done iteratively.

## Theory
This is achieved by partitioning the curve into four sectors, labeled 0-3, corresponding to the left segment (0), the left leg (1), the right leg (2) and the right segment (3). To get the coordinates of the $n$-th point $p_n$, calculate the 4-ary expansion of $n$. The digits describe, in which sector the $p_n$ lies in a given recursion depth. 

Reset the start and end point accordingly until max_depth is reached. The peak of a line segment can be calculated by

$$p=p_{start}+\frac{1}{2}\left(p_{end}-p_{start}\right)+\frac{1}{2\sqrt{3}}Rot_{90}\cdot(p_{end}-p_{start}).$$

E.g. $11=23_4$ , implying $p_{11}$ lies in sector 3 of depth 2 of sector 2 of depth 1. With max_depth=2, $p_{11}$ is the starting point of precisely that segment.

![alt text](https://github.com/TorgeGraner/KochscheSchneeflocke/blob/main/koch.PNG)

## Notes
For compiler reasons this only works for max_depth less than 6.
