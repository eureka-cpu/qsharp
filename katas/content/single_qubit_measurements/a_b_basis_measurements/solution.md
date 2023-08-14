For this problem, we follow the procedure given in the [arbitrary basis measurement section](./SingleQubitSystemMeasurements.ipynb#Arbitrary-basis-measurements-implementation) of the tutorial.
As noted in the solution of problem 6, the gate $R_x(-\theta)$, with $\theta = 2\alpha$ transforms the $\ket A/\ket B$ states to the $\ket 0/\ket 1$ states:
\begin{align}
R_x(-\theta) \ket A &= \ket 0 \\
R_X(-\theta) \ket B &= \ket 1
\end{align}
Hence, we first apply $R_x(-\theta)$ to the qubit. Next, we measure in the computational basis using the `M` operation.
If the `M` operation returned `Zero`, we get measurement outcome $A$, and if it returned `One`, we get measurement outcome $B$.

After the measurement, we apply the inverse of the $R_x(-\theta)$ gate, which is the $R_x(\theta)$ gate.
The final rotation ensures that the state of the qubit is in the state corresponding to the measurement outcome.

@[solution]({
    "id": "a_b_basis_measurements_solution",
    "exerciseId": "a_b_basis_measurements",
    "codePath": "solution.qs"
})