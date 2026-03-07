**Noise vs. Precision loss**  
Bootstrapping reduces accumulated noise but introduces approximation error, so the ciphertext becomes usable again but loses some precision.  

Two Different Types of Error (two sources of inaccuracy) in CKKS   
**1️⃣ RLWE Noise (Cryptographic Noise)**

This comes from the encryption scheme:
- encryption noise
- multiplication noise
- key switching noise
- ModUp noise Q0I(X)Q_0 I(X)Q0​I(X)
This noise **grows during computation** and eventually breaks decryption. Bootstrapping **reduces this noise dramatically**.

**2️⃣ Approximation Error (Numerical Error)**  
CKKS is inherently **approximate arithmetic**.  
Sources include:
- encoding/decoding rounding
- rescaling
- polynomial approximation during bootstrapping   
This type of error is **precision loss**. Bootstrapping **adds new approximation error**.

**Overall**
During normal evaluation:
- errors accumulate **slowly**, and precision decreases **gradually**
During bootstrapping:
- noise is **reset**, but **a noticeable precision drop occurs at once**