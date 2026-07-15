# cryptography
Cryptography Algorithms

Implementations of classic cryptographic algorithms written from scratch in Python, with no external crypto libraries (`cryptography`, `pycryptodome`, `hashlib`, etc.) — every table, S-box, and transformation is coded by hand.

## AES (Advanced Encryption Standard)

A complete AES-128 implementation following the standard round structure: SubBytes, ShiftRows, MixColumns, AddRoundKey, built on a 4x4 byte-matrix state (no Feistel structure).

**Includes:**
- Key expansion (Rijndael key schedule) generating K0–K10 from a 128-bit key
- Single-block encryption/decryption with full round-by-round tracing
- PKCS#7 padding + ECB mode for encrypting messages of arbitrary length
- Self-test against the official FIPS-197 test vector

**Run it:**
```bash
python3 aes.py
```

Running the script prints:
1. A FIPS-197 test vector check (verifies the implementation against the official known-answer test)
2. The full key schedule (K0 through K10)
3. A round-by-round trace of a sample block through all 10 rounds
4. Encryption/decryption of a plaintext message using PKCS#7 padding

## Requirements

Pure Python 3, no dependencies.

## Notes

Built for coursework in Cryptography & Network Security. Intended for learning the internals of AES — not for production use.
