Deprecated Features
========================

The following functionality is currently deprecated, and will likely
be removed in a future release. If you think you have a good reason to
be using one of the following, contact the developers to explain your
use case if you want to make sure your code continues to work.

This is in addition to specific API calls marked with BOTAN_DEPRECATED
in the source.

- The headers ``botan.h``, ``init.h``, ``lookup.h``

- All or nothing package transform (``package.h``)

- The TLS constructors taking `std::function` for callbacks. Instead
  use the TLS::Callbacks interface.

- The Buffered_Computation base class. In a future release the class will be
  removed, and all of member functions instead declared directly on
  MessageAuthenticationCode and HashFunction. So this only affects you if you
  are directly referencing `Botan::Buffered_Computation` in some way.

- The SymmetricAlgorithm base class. Similarly to Buffered_Computation, in a
  future release the class will be removed and its member functions copied to
  classes which currently subclass it. This only affects your code if you
  are referencing `Botan::SymmetricAlgorithm` directly.

- Platform support for BeOS and NaCl (Native Client)

- Support for PathScale and HP compilers

- TLS: 3DES and SEED ciphersuites

- TLS: Anonymous DH/ECDH ciphersuites

- TLS: DSA ciphersuites/certs

- TLS: static RSA key exchange ciphersuites

- TLS: CCM_8 ciphersuites

- Block ciphers CAST-256, Kasumi, MISTY1, and DESX.

- CBC-MAC, X9.19-MAC

- PBKDF1 key derivation

- GCM support for 64-bit tags

- Old (Google specific) ChaCha20 TLS ciphersuites

- All built in ECC groups < 256 bits

- All built in MODP groups < 2048 bits

- All pre-created DSA groups

- Directly accessing the member variables of calendar_point