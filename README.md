I like discovering new things. Examples of my findings: security vulnerabilities in Kubernetes, Podman and Singularity.
I've also created a SIMD algorithm that efficiently loads and shifts columns into diagonals. Here are the three first iteration steps of the algorithm:

```
v7 = a a a a a a a a    v0 = b b b b b b b b    v1 = c c c c c c c c
v6 =			v7 = a a a a a a a a	v0 = b b b b b b b b
v5 =			v6 =		    	v7 = a a a a a a a a
v4 =			v5 =		    	v6 =		    
v3 =         a a a a	v4 =         b b b b	v5 =         c c c c
v2 =			v3 =         a a a a	v4 =         b b b b
v1 =             a a	v2 =             b b	v3 =         a a c c
v0 =               a	v1 =             a b	v2 =           a b c
```
[See](https://github.com/eriksjolund/diagonalsw#implementation-detail-loading-score-values-into-a-diagonal-vector) how the diagonals fall into place.
