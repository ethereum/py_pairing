Implements optimal ate pairings over the bn\_128 curve.

### Pairings

See (Subgroup security in pairing-based cryptography)[https://eprint.iacr.org/2015/247.pdf]

TL;DR Some elliptic curves are "pairing friendly", such as BN, KSS and, BLS. Pairing is relevant to multitude of useful cryptographic operations, such as identity-based encryption, bulletproofs, and zkSNARKs. However, when ordinary curves are paired, vulnerabilities can be introduced, specifically, so-called subgroup attacks become feasible in certain circumstances. This code base instantiates one specific subgroup-secure pairing-friendly curve family, BN (k = 12). 

Parameters are drawn from (Subgroup security in pairing-based cryptography)[https://eprint.iacr.org/2015/247.pdf], Example 1. In general, there are few ramifications for 'downstream' ECC applications, expect for a minor (2 to 13%) slowdown of pairing related computations (per Table 2 of Barreto et al.).

### Usage

```python
python3 setup.py install

cd tests && python3 test_bn128.py    
```