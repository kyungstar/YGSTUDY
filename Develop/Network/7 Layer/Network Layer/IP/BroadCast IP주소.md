

# BroadCast

---

## BroadCast IP?
- 브로드캐스트 IP 주소는 네트워크 상의 모든 호스트에게 동시에 메시지를 전송하기 위해 사용되는 특수한 IP 주소입니다.
- 브로드캐스트 IP 주소는 특정 네트워크 주소에서 호스트 식별자를 모두 1로 설정한 형태로 구성됩니다.

### IPv4애서의 브로드캐스트 IP주소의 형태 
**A 클래스 네트워크** 
- 첫 번째 옥텟이 네트워크 식별자인 경우, 호스트 식별자 모두 1로 설정하여 브로드 캐스트 주소를 생성합니다.
- 예를 들어, 10.**255.255.255**는 10.0.0.0/8 네트워크의 브로드 캐스트 IP 주소입니다.

**B 클래스 네트워크**
- 첫 번째 **두 옥텟**이 네트워크 식별자인 경우, 마지막 옥텟을 모두 1로 설정하여 브로드캐스트 주소를 생성합니다.
- 예를 들어, 172.16.255.255는 172.16.0.0./16 네트워크의 브로드캐스트 IP 주소입니다.

**C 클래스 네트워크**
- 첫 번째 **세 옥텟**이 네트워크 식별자인 경우, 마지막 옥텟을 1로 설정하여 브로드캐스트 주소를 생성합니다.
- 예를 들어, 192.168.0.255는 192.168.0.0/25 네트워크의 브로드캐스트 IP 주소입니다.


--- 

## 정리 ❗
- 브로드캐스트 IP 주소를 사용하면 네트워크 상의 모든 호스트에게 메시지를 전송할 수 있습니다.
- 예를 들어, DHCP 서버가 네트워크에 있는 모든 호스트에게 IP 주소를 할당하려면 브로드캐스트 메시지를 사용할 수 있습니다. 
- 브로드캐스트 IP 주소는 네트워크 관리 및 통신에 유용하게 사용될 수 있습니다.


---
* 참고자료
> [1] [Broadcast IP주소](https://sjaqjnjs22.tistory.com/40)


