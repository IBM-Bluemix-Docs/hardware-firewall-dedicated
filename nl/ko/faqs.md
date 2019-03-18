---

copyright:
  years: 2017
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:faq: data-hd-content-type='faq'}

# Hardware Firewall (Dedicated)에 대한 FAQ
{: #faqs-for-hardware-firewall-dedicated-}

다음은 Fortigate Security Appliance 1g 방화벽에 대한 작업을 할 때 자주 묻는 질문(FAQ)입니다.

## 방화벽이란 무엇입니까?
{:faq}

방화벽은 서버의 업스트림에 연결되어 있는 네트워크 디바이스입니다. 방화벽은 원치 않는 트래픽이 서버에 도달하기 전에 서버에서 트래픽을 차단합니다.

## 방화벽을 사용해야 하는 이유는 무엇입니까?
{:faq}

방화벽을 사용할 때의 기본적인 장점은 서버에서 “안전한” 트래픽만 처리하면 된다는 것입니다. 원치 않는 트래픽도 처리해야 하는 것이 아니라 의도한 목적에 대해서만 리소스가 사용된다는 것을 의미합니다.

## IBM©에서 제공하는 방화벽 제품
{:faq}

이 [주제](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-exploring-firewalls)를 검토하여 IBM Cloud에서 제공되는 모든 방화벽 제품에 대한 상세한 비교를 볼 수 있습니다. 

## Hardware Firewall (Dedicated)는 IBM의 로드 밸런서 제품과 호환 가능합니까?
{:faq}

예. Hardware Firewall (Dedicated)는 표준 및 전용 로드 밸런서, Citrix Netscaler VPX 및 MPX와 호환 가능합니다.

## 전용 하드웨어 방화벽 및 네트워크 게이트웨이를 동일한 VLAN과 연관시킬 수 있습니까?
{:faq}

아니오. 방화벽 서비스(공유 또는 전용) 및 네트워크 게이트웨이 디바이스를 동일한 VLAN에 연관시킬 수 없습니다. 

## 공용 트래픽이 내 로드 밸런서 또는 Hardware Firewall을 먼저 통과합니까?
{:faq}

공용 인터넷에서 오는 경우 Local Load Balancer, Dedicated Load Balancer 또는 Enterprise Load Balancer 제품이 첫 번째이고, Hardware Firewall 제품이 그 다음, 그리고 NetScaler 제품이 (고객 서버와 함께) 마지막입니다.

## SoftLayer는 방화벽 대역폭의 비용을 청구합니까?
{:faq}

Hardware Firewall (Shared), Hardware Firewall (Dedicated) 및 Fortigate Security Appliance는 대역폭에 대해 측정되지 않습니다.  또한 이러한 제품들은 해당 서버가 응답해야 하는 트래픽을 제한함으로써 전체 대역폭 이용도를 줄일 수 있습니다.

## 내 Windows 방화벽에서 회색으로 표시되는 포트는 무엇입니까?
{:faq}

SoftLayer는 Evault, SNMP 및 Nagios 모니터링을 포함하여 서버와 함께 이용할 수 있는 다양한 여러 서비스를 제공합니다. 이러한 서비스를 이용하려면 IBM의 내부 시스템이 사용자 서버와 어느 정도 통신할 수 있어야 합니다. 예외 목록에서 회색으로 표시되는 포트는 내부 네트워크 포트 전용으로 열린 포트입니다. 이러한 포트는 공용 (인터넷) 네트워크 연결에서 계속 차단됩니다. 내부 네트워크는 보안이 설정된 네트워크이므로 이러한 포트가 열려 있는 것을 안전하다고 간주합니다.

일반적으로 이러한 포트는 수정할 수 없습니다. 그러나 방화벽 규칙을 재설정하는 경우 예외 목록에서 포트가 지워집니다. 방화벽 규칙을 재설정하면 이러한 추가적인 서비스에 부정적인 영향을 줄 수 있을 뿐만 아니라 현재 구성에 따라 서버에 다른 문제가 발생할 수도 있다는 점에 주의하십시오.

## 10Gbps 서버에 사용 가능한 Hardware Firewall 옵션은 무엇입니까?
{:faq}

(데이터베이스, 백업, 스토리지 등에 대해) 사설 네트워크에 10Gbps만 필요한 경우 고객이 공용 업링크만 다운그레이드를 요청할 수 있으며 Hardware Firewall 제품 중에 주문할 수 있습니다. 공용 네트워크에서 10Gbps가 필요한 경우 네트워크 게이트웨이 또는 Fortigate Security Appliance 10Gbps가 필요합니다.

## 방화벽에서 허용되는 IP 범위는 어떻게 됩니까?
{:faq}

방화벽에서 허용되는 IP 주소 및 IP 범위 목록은 [여기](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-ibm-cloud-ip-ranges)로 이동하십시오. 

## Hardware Firewall (Dedicated) 또는 Fortigate Security Appliance가 보호하는 최대 서버 수는 어떻게 됩니까?
{:faq}

Hardware Firewall Dedicated와 Fortigate Security Appliance 모두 공용 VLAN의 모든 서버를 보호할 수 있습니다.  그러나 이러한 FW 디바이스가 2Gbps 업링크와 연결되어 있으므로 사용자 앱의 성능 요구를 충족하도록 방화벽 인스턴스의 수를 스케일링하는 것이 좋습니다. 고객들은 추가적인 방화벽 및 연관된 컴퓨팅 리소스를 추가할 수 있도록 Pod 내에 추가적인 공용 VLAN 방화벽을 배치하여 이 작업을 간단하게 수행할 수 있습니다.

## 각 방화벽 제품에 포함되는 VPN 옵션은 무엇입니까?
{:faq}

모든 방화벽에서 VPN을 제공하는 것은 아니며 모든 VPN 옵션이 동일하지는 않습니다.  VPN에 대한 일반 옵션은 다음과 같습니다.

* 각 고객은 사설 네트워크에 대한 무제한 SSL VPN 연결을 수신합니다. 고객 포털에 로그인되어 있는 동안 페이지의 맨 위에 있는 VPN 링크를 클릭하여 이러한 연결을 설정할 수 있습니다.
* 또한 고객은 계정 당 하나의 PPTP VPN을 수신합니다. $5/월에 5씩 추가하여 계정에 PPTP VPN 사용자를 추가할 수 있습니다.
* 또한 SoftLayer는 월 $99부터 기본 멀티 테넌트 IPSec VPN 서비스를 제공합니다.
* Fortigate Security Appliance는 공용 네트워크 액세스 전용으로 SSL 및 IPSec VPN 옵션을 제공합니다(SoftLayer 사설 네트워크에 액세스할 수 없음).
* 네트워크 게이트웨이는 공용 또는 사설 네트워크에서 SSL, IPSec 및 OpenVPN 기능을 제공합니다.
* NetScaler 제품에서는 공용 또는 사설 네트워크에서 SSL 및 IPSec VPN을 제공할 수 있습니다.
* 또한 고객은 VPN 솔루션을 SoftLayer 환경 내의 서버에 배치할 수 있습니다.

## Hardware Firewall (Dedicated) 또는 Fortigate Security Appliance에 대한 고가용성 옵션을 선택하는 경우 이 기능을 활용하기 위해 어떤 단계를 수행해야 합니까?
{:faq}

없음. HA에서 주문한 경우 SoftLayer는 HA 구성으로 어플라이언스를 자동으로 프로비저닝합니다.  기본 디바이스가 실패하는 경우 보조 수동 디바이스에서 기본 활성 인스턴스 역할을 맡게 되고 트래픽을 전달하기 시작합니다.  이 장애 복구 작업은 보통 자동으로 수행되지만 서버를 모니터하고 트래픽이 성공적으로 전달되고 있는지 확인하는 것이 좋습니다.

## 어떤 방화벽 제품이 공용 대 사설 NAT 및/또는 사설 VLAN 세그먼트화를 지원합니까?
{:faq}

Fortigate Security Appliance 10Gbps가 공용 대 사설 NAT 및 사설 VLAN 세그먼트화를 지원합니다. 
