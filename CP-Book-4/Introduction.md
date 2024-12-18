---
created: 18-12-2024-12:57:44
modified: 18-12-2024-12:57:44
tags: 
book: Competitive Programming 4
authors: Steven Halim, Felix Halim, Suhendry Efendy
---
## Algorithmic Analysis

**Basic time and space complexity analysis for iterative and recursive algorithms:** 
1. An algorithm with $k$-nested loops of about $n$ iterations each has $O(n^k)$ complexity
2. If your algorithm is recursive with $b$ recursive calls per level and has $L$ levels, the algorithm roughly $O(b^L)$ complexity, but this is only a rough *upper bound*. The actual complexity depends on what actions are done per level and whether pruning is possible
3. A Dynamic Programming algorithm or other iterative routine which processes a 2D $n \times n$ matrix in $O(k)$ per call runs in $O(k \times n^2)$ time.
4. Binary searching over a range of $[1..n]$ has $O(\log{n})$ complexity

**More advanced algorithm techniques:**
1. Prove the correctness of an algorithm (especially for greedy algorithms), to minimize your chance of getting 'Wrong Answer' (WA) verdict
2. Perform the **amortized analysis** to minimize the chance of getting 'Time Limit Exceeded' (TLE) verdict. Sometimes algorithms which we consider to be very slow are in fact fast enough in amortized sense
3. Do output-sensitive analysis to analyze algorithm which (also) depends on output size and minimize your chance of getting the ‘Time Limit Exceeded’ verdict. For example, the time complexity of partial sort algorithm is $O(n \log{k})$ . The time taken for this algorithm to run depends not only on the input size $n$ but also the output size—the required $k$ smallest (or largest) numbers to be sorted 

**Familiarity with these bounds:**
1. $2^{10} = 1024 \approx 10^3, 2^{20} = 1048579 \approx 10^6$
2. $10! = 3628800 \approx 3*10^6, 11! = 39916800 \approx 4*10^7$
3. Upper limits of
	- 32-bit signed integers (int): $2^{31}-1 \approx 2 \times 10^9$ (safe for up to $\approx$ 9 decimal digits) 
	- 64-bit signed integers (long long): $2^{64}-1 \approx1 \times 10^{19}$
4. To store integers $\ge 2^{64}$, use Big Integer
5. There are $n!$ permutations and $2^n$ subsets (or combinations) of $n$ distinct elements
6. The best time complexity of a comparison-based sorting algorithm is $\Omega (n \log_2 {n})$
7. The largest input size $n$ for typical programming contest problems must be $\le 1 M$. Beyond that, the Input/Output (I/O) routine will be bottleneck
8. Usually, $O(n \log_2{n})$ algorithms are sufficient to solve contest problems for a simple reason: $O(n \log_2{n})$ and the theoretically better $O(n)$ algorithms are hard to differentiate *empirically* under programming contest environment with strict time limit, $n \le 1M$, and the need to support $\gt 1$ programming languages


---
## References

1. CP4 Introduction by Steven Halim, Felix Halim, Suhendry Efendy