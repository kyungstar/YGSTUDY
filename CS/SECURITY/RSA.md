- First Created By KYG On 2023-05-18

# RSA
- RSA(Rivest-Shamir-Adleman)는 공개 키 암호화 방식으로 알려진 암호화 알고리즘입니다.


# Key Generation
- RSA 암호화에서는 공개 키와 개인 키를 생성합니다.
키 생성 과정은 다음과 같습니다
  - 1.1. 소수(p, q) 선택: 두 개의 큰 소수 p와 q를 선택합니다.
  - 1.2. Modulus(N) 계산: Modulus(N)을 계산합니다. N은 두 소수 p와 q의 곱으로 나타냅니다. N = p * q.
  - 1.3. Phi(φ) 계산: Phi(φ)는 (p-1)과 (q-1)의 곱으로 계산됩니다. φ = (p-1) * (q-1).
  - 1.4. 공개 키 선택: 공개 키(e)를 선택합니다. e는 1보다 크고 φ보다 작으며, φ와 서로소인 수여야 합니다.
  - 1.5. 개인 키 계산: 개인 키(d)를 계산합니다. d는 (e * d)를 φ로 나눈 나머지가 1이 되도록 선택됩니다.

# Encryption
- 암호화 과정에서는 공개 키를 사용하여 원본 메시지를 암호화합니다.
암호화 과정은 다음과 같습니다
  - 2.1. 공개 키와 메시지 선택: 암호화할 메시지를 선택하고, 암호화에 사용할 공개 키를 획득합니다.
  - 2.2. 메시지 변환: 선택한 메시지를 숫자로 변환합니다.
  - 2.3. 암호화: 숫자로 변환된 메시지를 공개 키로 암호화합니다. 암호화된 결과는 암호문(Ciphertext)입니다.

# Decryption
복호화 과정에서는 개인 키를 사용하여 암호문을 해독하여 원본 메시지를 복원합니다.
복호화 과정은 다음과 같습니다
  - 3.1. 개인 키와 암호문 선택: 복호화에 사용할 개인 키와 암호문을 획득합니다.
  - 3.2. 복호화: 암호문을 개인 키로 복호화하여 원본 메시지를 얻습니다.

# Digital Signature
RSA는 또한 디지털 서명에도 사용될 수 있습니다.
디지털 서명은 메시지의 인증과 무결성을 보장하기 위해 사용됩니다.


# 보안 통신을 위한 HTTPS
- HTTP는 웹에서 데이터를 전송하기 위한 프로토콜이지만, 통신 과정에서 데이터가 암호화되지 않습니다. 
- 따라서, 민감한 정보(예: 로그인 정보, 신용카드 번호 등)를 주고받을 때 보안 문제가 발생할 수 있습니다.
-> 이를 해결하기 위해 HTTP에 암호화 기능을 추가한 것이 HTTPS(HTTP Secure)입니다. 
- HTTPS는 보안 소켓 계층(SSL) 또는 전송 계층 보안(TLS) 프로토콜을 사용하여 통신을 암호화합니다.
- RSA는 공개 키 암호화 방식 중 하나이며, TLS/SSL에서 사용되는 암호화 알고리즘 중 하나입니다. 
- HTTPS는 RSA와 같은 암호화 알고리즘을 사용하여 데이터의 기밀성과 안전성을 보장합니다.


# 여기서 잠깐!! SSL과 TLS의 프로토콜이란?
- 보안 소켓 계층(SSL, Secure Sockets Layer) 및 전송 계층 보안(TLS, Transport Layer Security)은 네트워크 통신에서 보안을 제공하기 위해 사용되는 프로토콜입니다.
- 이들은 암호화와 인증을 통해 데이터의 기밀성과 무결성을 보호하며, 안전한 통신을 가능하게 합니다. 
- 아래에서 SSL 및 TLS에 대해 자세히 설명하겠습니다.

# 사진 추가

SSL (Secure Sockets Layer)
- SSL은 처음에 넷스케이프(Netscape)에서 개발한 보안 프로토콜로, 웹 통신에서 데이터 보호를 위해 사용됩니다.
- SSL은 암호화, 인증 및 데이터 무결성을 제공하는 프로토콜로서, 클라이언트와 서버 간의 안전한 통신을 확립합니다.
- SSL은 대칭 키 암호화와 공개 키 암호화를 조합하여 데이터를 암호화하고 복호화하며, 디지털 인증서를 사용하여 신뢰할 수 있는 인증을 수행합니다.

# 사진 추가

TLS (Transport Layer Security)
- TLS는 SSL의 후속 버전으로, 현재 널리 사용되는 프로토콜입니다.
- SSL 3.0 버전을 기반으로 개발되었으며, 보안 통신에서 일반적으로 사용됩니다.
- TLS는 SSL과 동일한 목적으로 개발되었으며, 데이터 보호와 안전한 통신을 위한 암호화 및 인증을 제공합니다.
- TLS는 SSL과의 호환성을 유지하면서 보안 강화 및 알고리즘 업데이트를 포함한 여러 개선 사항을 제공합니다.

