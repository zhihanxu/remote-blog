***Benes network***
![[Pasted image 20260228140133.png]]

- can be viewed as two back-to-back Butterfly/Omega
- 2 logN - 1 stages
- complex but rearrangeable non-blocking
- more than one possible path; all N! permutations

***Streaming permutation network***
Proposed in: *Automatic Generation of High Throughput Energy Efficient Streaming Architectures For Arbitrary Fixed Permutations* [FPL 2015]

- Fixed: permutation determined at design-time  
	- Unlike a dynamic crossbar that might change its routing every single clock cycle based on incoming metadata, this design pre-calculates the switch states and memory addresses for a specific, repeating pattern
- **Any arbitrary fixed permutation** of size $N$ can be realized. This is because the architecture is mathematically mapped from a **Benes network**, which is a "rearrangeable" multi-stage interconnection network proven to be able to realize all
