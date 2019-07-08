---

copyright:
  years: 2017
lastupdated: "2018-11-30"

keywords: bypass, firewall, rules,

subcollection: hardware-firewall-dedicated

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:note: .note}
{:important: .important}

# Hardware Firewall (Dedicated) 규칙 무시
{: #bypassing-hardware-firewall-dedicated-rules}

방화벽 규칙을 무시하려면 다음을 수행하십시오.

1. 브라우저에서 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window}을 열고 계정에 로그인하십시오.
2. 고객 포털 탐색에서 **네트워크 > IP 관리 > VLAN**으로 이동하여 무시하려는 방화벽 디바이스를 클릭하십시오.
3. **디바이스 세부사항** 페이지에서 **조치** 드롭 다운 메뉴를 사용하여 **규칙 무시 설정**을 선택하거나 **상태** 섹션에서 **규칙 무시** 단추를 클릭할 수 있습니다. 어느 방법이든 확인 대화 상자가 표시됩니다. **예**를 클릭하여 조치를 확인하십시오. 규칙을 무시하는 조치가 적용되려면 약 2분이 소요됩니다. 무시 모드에 있는 동안 "상태"는 "모든 규칙 무시 중"이 됩니다. 

	또 다른 옵션은 문제점 해결 등을 수행할 때 방화벽을 라우트 어라운드하는 것입니다. **조치** 드롭 다운 메뉴를 사용하여 **라우트 무시 설정**을 선택하거나 **상태** 섹션에서 **라우트 어라운드**를 클릭할 수 있습니다. 

## 규칙을 다시 사용으로 설정
{: #enable-the-rules-again}

규칙을 다시 사용으로 설정하려면 위의 지시사항에 따라 **디바이스 세부사항** 페이지로 이동하여 **조치** 드롭 다운 메뉴를 클릭하고 **라우트 무시 설정**을 선택하십시오. 확인 대화 상자가 표시됩니다. **예**를 클릭하여 조치를 확인하십시오. 2분 이내에 "상태"가 "방화벽 라우트 쓰루 중"으로 다시 변경됩니다.
