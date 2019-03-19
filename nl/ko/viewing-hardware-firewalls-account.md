---

copyright:
  years: 2017,2018
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# IBM 방화벽 보기
{: #viewing-your-ibm-firewalls}

방화벽으로 어떤 VLAN이 보호되는지 확인하고 개별 방화벽에 대한 세부사항을 찾으려면, VLAN 페이지로 이동하십시오.

1. 브라우저에서 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window}을 열고 계정에 로그인하십시오.
2. 고객 포털 탐색에서 **네트워크 > IP 관리 > VLAN**을 선택하십시오.

테이블에서 각 행은 인프라에 있는 VLAN을 표시합니다. IBM© Cloud는 구성된 실제 VLAN 번호 및 라우터를 나타내는 "VLAN 번호" 및 "1차 라우터" 정보를 자동으로 채웁니다. 인식 가능한 이름을 제공하는 데 "이름" 필드를 사용할 수 있습니다(예: DMZ, 인트라넷, 공용 또는 데이터베이스).

맨 오른쪽 열 "게이트웨이/방화벽"에는 어떤 방화벽 보호가 준비되어 있는지에 대한 세부사항이 포함됩니다. 예를 들면, 다음과 같습니다.

- **방화벽 추가**는 이 VLAN의 서버에 대해 준비된 방화벽이 없음을 표시합니다.
- **개별 보호된 서버**는 하나 이상의 서버에서 Hardware Firewall (Shared)를 활용하고 있으며 Hardware Firewall (Dedicated), FortiGate Security Appliance 또는 네트워크 게이트웨이가 없음을 나타냅니다. VLAN 방화벽과 네트워크 게이트웨이는 개별 보호된 서버가 있는 VLAN에 배치할 수 없습니다.
- **Firewall-vlanXXXX.networklayer.com**은 Hardware Firewall (Dedicated) 또는 FortiGate Security Appliance가 준비되어 있음을 나타냅니다. 단 하나의 VLAN 방화벽 또는 네트워크 게이트웨이를 VLAN과 연관시킬 수 있지만, 서버를 공용 VLAN에서 VLAN 방화벽으로 보호하고 사설 네트워크에서 네트워크 게이트웨이와 연관시킬 수 있습니다.
- **GatewayName**은 VLAN이 해당 네트워크 게이트웨이와 연관되어 있음을 나타냅니다.

## 개별 보호된 서버 세부사항

"게이트웨이/방화벽" 필드에 **개별 보호된 서버**가 있는 VLAN의 경우 연관된 VLAN 번호 링크를 클릭하여 연관된 디바이스를 포함한 VLAN의 세부사항을 표시할 수 있습니다.

연관된 디바이스 목록에서 각 디바이스를 클릭하고 구성 탭의 맨 아래로 스크롤할 수 있습니다. 추가 기능 섹션에 **방화벽**이 표시되며 **설치됨** 또는 **설치되지 않음** 상태가 함께 표시됩니다.

- **설치되지 않음**은 이 디바이스에 대한 방화벽이 준비되어 있지 않음을 나타냅니다.
- **설치됨**은 방화벽이 준비되어 있음을 나타냅니다. 디바이스에서 방화벽 구성을 관리할 수 있는 **방화벽** 탭을 사용할 수 있습니다.

## 전용 방화벽 세부사항

"게이트웨이/방화벽" 필드에 **Firewall-vlanXXXX.networklayer.com**이 있는 VLAN의 경우 해당 방화벽 링크를 클릭하여 방화벽의 세부사항을 표시할 수 있습니다. 디바이스 세부사항에는 연관된 라우터, VLAN, IPv4/IPv6 서브넷, 해당 VLAN과 연관된 디바이스, 트래픽을 라우트 쓰루하거나 방화벽을 라우트 어라운드하기 위한 제어가 포함되어 있습니다.

FortiGate Security Appliance 디바이스에는 관리 IP, 사용자 이름 및 비밀번호가 있습니다.  FortiGate Security Appliances의 관리는 해당 GUI 또는 SSH 기반 콘솔을 통해 완료됩니다.

## 네트워크 게이트웨이 세부사항

"게이트웨이/방화벽" 필드에 네트워크 게이트웨이 디바이스 이름이 있는 VLAN의 경우 네트워크 게이트웨이 이름을 클릭하여 네트워크 게이트웨이의 세부사항을 표시할 수 있습니다. 디바이스 세부사항에는 연관된 프론트 엔드(FCR) 및 백엔드(BCR) VLAN 및 네트워크 게이트웨이 관리 옵션이 포함되어 있습니다.
