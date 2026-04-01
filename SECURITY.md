Security Best Practices
​Key Management: Cryptographic keys must be stored in secure hardware security modules (HSMs) or managed key services. Hardcoding a 256-bit key in your script renders the encryption moot if the source code is accessed.
​Handling Decryption Failures: Notice the InvalidTag exception handling. You must never distinguish between a "wrong key" and "data tampering" in error messages returned to an end-user, as this can facilitate padding oracle or side-channel attacks.
​Data Integrity: The authentication tag ensures that even a single bit change in the ciphertext_with_tag will result in a decryption failure, preventing "bit-flipping" attacks.
​Would you like further clarification on the mathematical mechanics of the Galois field used in GCM, or would you like to see an example of how to handle Associated Data (AD) for header authentication.
