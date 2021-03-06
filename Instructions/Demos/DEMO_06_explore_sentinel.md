---
Demo:
    title: 'Microsoft Sentinel'
    module: '모듈 3 단원 3: Microsoft 보안 솔루션의 기능 설명: Microsoft Sentinel의 보안 기능 설명'
---


# 데모: Microsoft Sentinel 

### 데모 시나리오
이 데모에서는 Microsoft Sentinel 인스턴스를 만드는 프로세스를 단계별로 진행합니다.  그리고 Microsoft Sentinel을 지원하기 위해 배포할 리소스에 액세스할 수 있도록 관련 권한도 설정합니다.  이러한 기본 설정을 완료한 후에는 데이터 원본에 Microsoft Sentinel을 연결하고, 기본 제공 분석 기능을 사용하여 의심스러운 활동의 알림을 받도록 설정하는 단계를 진행합니다. 그리고 마지막으로 자동화 기능을 살펴봅니다.  

#### 데모 1부:  Microsoft Sentinel 인스턴스 만들기

1. 브라우저 탭에서 **홈 - Microsoft Azure**를 엽니다.  이전에 해당 탭을 닫았다면 브라우저 페이지를 열고 주소 표시줄에 portal.azure.com을 입력하여 다시 로그인합니다.

1. 검색 상자(페이지 위쪽의 'Microsoft Azure' 옆에 있는 파란 막대)에 **Microsoft Sentinel**을 입력하고 검색 결과에서 **Microsoft Sentinel**을 선택합니다.

1. Microsoft Sentinel 페이지에서 **Microsoft Sentinel 만들기**를 선택합니다.

1. 작업 영역에 Microsoft Sentinel 추가 페이지에서 **새 작업 영역 만들기**를 선택합니다.

1. Log Analytics 작업 영역 만들기의 기본 탭에서 다음 정보를 입력합니다.
    1. 구독:  **Azure Pass - 스폰서쉽**
    1. 리소스 그룹: **새로 만들기**를 선택하고 이름으로 **SC900-Sentinel-RG**를 입력한 다음 **확인**을 선택합니다.
    1. 이름: **SC900-LogAnalytics-workspace**
    1. 지역: **미국 동부**(기본값 유지)
    1. **다음: 가격 책정 계층 >을 선택합니다.**

1. 가격 책정 계층은 기본 설정인 **종량제(GB당 2018)** 를 그대로 유지하고 **다음: 태그 >** 를 선택합니다.

1. 태그는 비워 두어도 됩니다. **검토 + 만들기**를 선택합니다.

1. 입력한 정보를 확인하고 **만들기**를 선택합니다.

1. 새 작업 영역이 목록에 표시되려면 1~2분 정도 걸릴 수 있습니다. 2분이 지났는데 작업 영역이 표시되지 않으면 **새로 고침**, **추가**를 차례로 선택합니다.

1. 새 작업 영역이 추가되면 Microsoft Sentinel | 뉴스 및 가이드 페이지가 표시됩니다.  시작 페이지에는 3단계가 표시됩니다.

1. 다음 작업에서 사용할 것이므로 이 페이지를 열어 두세요.

#### 데모 2부:  Microsoft Sentinel 인스턴스를 만든 후에는 Microsoft Sentinel을 지원하기 위해 배포할 리소스에 필요한 액세스 권한을 설정해야 합니다.  이 작업에서는 Microsoft Sentinel 인스턴스를 사용하여 만든 리소스 그룹의 액세스 제어(IAM) 페이지로 이동하여 사용 가능한 역할을 확인한 후 자신(MOD 관리자)에게 필요한 역할을 할당합니다. 리소스 그룹 수준에서 역할을 할당하면 Microsoft Sentinel을 지원하기 위해 배포하는 모든 리소스에 해당 역할이 적용됩니다.

1. 검색 상자(페이지 위쪽의 'Microsoft Azure' 옆에 있는 파란 막대)에 **리소스 그룹**을 입력하고 검색 결과에서 **리소스 그룹**을 선택합니다.

1. 리소스 그룹 페이지에서 Microsoft Sentinel을 사용하여 만든 리소스 그룹인 **SC900-Sentinel-RG**를 선택합니다.

1. SC900-Sentinel-RG 페이지의 왼쪽 탐색 패널에서 **액세스 제어(IAM)** 를 선택합니다.

1. 액세스 제어 페이지에서 **내 액세스 권한 보기**를 선택합니다.  현재 역할은 서비스 관리자입니다.  창 오른쪽 위에서 **X**를 선택하여 MOD 관리자 할당 창을 닫습니다.

1. 액세스 제어 페이지에서 **+ 추가**를 선택하고 **역할 할당 추가**를 선택합니다.

1. 역할 할당 추가 창이 열립니다.  역할 선택 필드의 드롭다운 화살표를 선택하여 사용 가능한 역할을 표시합니다. 역할 선택 검색 상자에 **Microsoft Sentinel**을 입력하여 Microsoft Sentinel과 연관된 역할 4개를 확인합니다. 모범 사례에 따라 역할에 필요한 최소 권한을 할당해야 합니다.  이 랩에서는 편의상 검색 상자에 **Owner**를 입력하고 결과에서 **Owner**를 선택합니다.  참고로 Microsoft Sentinel의 권한은 다음 페이지에서 검토할 수 있습니다.  https://docs.microsoft.com/ko-kr/azure/sentinel/roles

1. 표시되는 사용자 목록에서 **MOD 관리자**를 선택합니다.

1. 페이지 아래쪽의 **저장**을 선택합니다.

1. 액세스 제어 페이지에서 **내 액세스 권한 보기**를 선택하여 역할이 추가되었는지를 확인한 후에 창 오른쪽 위에서 **X**를 선택하여 창을 닫습니다.

#### 데모 3부:  데모의 3부에서는 데이터 수집을 시작하기 위해 데이터 원본에 Microsoft Sentinel을 연결하는 프로세스를 진행합니다.  참고: 커넥터의 연결된 상태가 표시되려면 시간이 다소 걸릴 수도 있습니다(테넌트에 따라 최대 30분).

1. 검색 상자(페이지 위쪽의 'Microsoft Azure' 옆에 있는 파란 막대)에 **Microsoft Sentinel**을 입력하고 검색 결과에서 **Microsoft Sentinel**을 선택합니다.

1. Microsoft Sentinel 페이지에서 Microsoft Sentinel 인스턴스를 사용하여 만든 작업 영역인 **SC900-LogAnalytics-workspace**를 선택합니다.

1. Microsoft Sentinel과 관련하여 가장 먼저 수행해야 하는 단계는 데이터 수집이 가능하도록 설정하는 것입니다. 왼쪽 탐색 패널에서 구성 아래의 **데이터 커넥터**를 선택합니다.

1. 데이터 커넥터 페이지에서 주 창 아래쪽으로 스크롤하여 사용 가능한 커넥터의 광범위한 목록을 확인합니다. 데이터 커넥터 페이지의 검색 상자에 **Azure**를 입력하고 목록에서 **Azure Active Directory**를 선택합니다.

1. 그러면 Azure Active Directory 커넥터 창이 열립니다.  **커넥터 페이지 열기**를 선택합니다.

1. Azure Active Directory 커넥터 페이지에서 설명을 검토하고 통합 문서, 쿼리, 분석 규칙 템플릿 등의 관련 콘텐츠를 살펴봅니다.  

1. 주 창의 지침 탭에서는 Azure Active Directory와 Microsoft Sentinel을 통합하려면 충족해야 하는 필수 구성 요소가 제공됩니다.   구성 아래에서 **로그인 로그**를 선택하고 변경 내용 적용을 선택합니다(여러 커넥터를 선택할 수 있음).  참고: 커넥터의 연결된 상태가 표시되려면 시간이 다소 걸릴 수도 있습니다(최대 30분 정도).  다음 링크에서 참조 정보를 확인할 수 있습니다.
    1. Microsoft Sentinel의 권한 검토:  https://docs.microsoft.com/ko-kr/azure/sentinel/roles
    1. Azure Active Directory에 연결:  https://docs.microsoft.com/ko-kr/azure/sentinel/connect-azure-active-directory

1. 다음 단계 탭에서 권장 통합 문서 목록을 확인합니다.   권장 통합 문서 아래에서 **Azure 로그인 로그**를 선택합니다(추가 통합 문서를 선택할 수 있음).

1. 통합 문서 페이지에서 템플릿 탭을 선택한 상태로(밑줄이 표시됨) **Azure 로그인 로그**를 선택합니다.

1. Azure AD 로그인 로그 창이 열리면 설명을 검토하고 **템플릿 보기**를 선택합니다.  화면 오른쪽 위에서 X를 선택하여 템플릿을 종료합니다.  페이지 아래쪽에서 저장을 선택한 후 확인을 선택하여 기본 위치에 통합 문서를 저장합니다.

1. 통합 문서 페이지 왼쪽 위의 '통합 문서' 위에서 **Microsoft Sentinel**을 선택합니다. 그러면 Microsoft Sentinel 데이터 커넥터 페이지로 돌아갑니다.

1. 데이터 커넥터 페이지 위쪽에 1개 연결됨이 표시됩니다. 즉, 이제 Azure Active Directory에 연결된 것입니다.

1. 왼쪽 탐색 패널에서 **통합 문서**를 선택합니다.

1. 통합 문서 페이지에서 검색 상자 위에 있는 **내 통합 문서** 탭을 선택합니다.  방금 저장한 통합 문서가 나열됩니다. 이 통합 문서에서 데이터를 확인 및 모니터링할 수 있습니다.  해당 통합 문서에는 후속 로그인이 반영되므로 로그인 정보를 표시하도록 선택할 수 있습니다.

1. 다음 작업에서 사용할 것이므로 이 페이지를 열어 두세요.

#### 데모 4부(선택 사항):  데모의 4부에서는 기본 제공 분석 규칙 템플릿을 사용하여 의심스러운 활동이 수행되면 알림을 제공하는 규칙을 만드는 프로세스를 진행합니다.

1. 왼쪽 탐색 패널에서 **분석**을 선택합니다.

1. 분석 페이지에는 활성 규칙(기본적으로는 고급 다단계 공격 검색이 사용하도록 설정됨)이 표시되며, 규칙 템플릿 액세스 옵션도 제공됩니다.  **규칙 템플릿** 탭을 선택합니다.  사용 가능한 템플릿 목록과 해당 목록을 템플릿하는 여러 가지 방법을 확인합니다.  Microsoft Sentinel 작업 영역 내에서 기본 제공되는 분석 경고를 사용하는 경우 의심스러운 상황 발생 시 알림이 제공됩니다.

1. 검색 창에 **Azure Portal**을 입력합니다.  **Azure Portal에 대한 로그인 시도 실패**를 선택합니다.  

1. 그러면 열리는 창에서 설명을 확인하고 템플릿 관련 정보를 검토합니다.  페이지 아래쪽의 **규칙 만들기**를 선택합니다.
    1. 분석 규칙 마법사에서 정보를 검토하고 **다음: 규칙 논리 설정 >** 을 선택합니다.
    1. 규칙 논리 설정 페이지에서 새 분석 규칙의 논리를 정의합니다. 템플릿에 일부 논리 및 미리 정의된 설정이 이미 제공되어 있습니다.  페이지를 스크롤하여 사용 가능한 설정을 확인합니다.  기본값을 그대로 둡니다. **다음: 인시던트 설정(미리 보기)>** 을 선택합니다.
    1. 인시던트 설정 옵션을 사용하면 Microsoft Sentinel 경고를 확인해야 하는 인시던트로 그룹화할 수 있습니다. 이 분석 규칙에서 경고가 트리거되면 인시던트를 생성해야 하는지 여부를 설정할 수 있습니다.  기본 설정을 그대로 두고 **다음: 자동화된 응답 >** 을 선택합니다.
    1. 자동화된 응답 탭에서는 플레이북을 추가하여 응답을 자동화할 수 있습니다.  마찬가지로 인시던트 자동화 규칙도 만들 수 있습니다.  인시던트 자동화 아래에서 **+ 새로 추가**를 선택합니다.  그러면 새 자동화 규칙을 만드는 창이 열립니다.  이 페이지에서 만든 모든 자동화 규칙은 처음에 선택한 분석 규칙에 의해 트리거됩니다(이 경우 Azure Portal에 대한 로그인 시도 실패).  여기서도 이전 단계와 마찬가지로 규칙의 조건을 추가하고 작업을 설정할 수 있습니다.   **취소**를 선택하여 창을 종료합니다.
    1. **다음: 검토>** 를 선택하여 선택한 템플릿을 기반으로 하는 규칙과 연관된 모든 세부 정보를 검토합니다. 이 시점에서 **만들기**를 선택하여 규칙을 만들어도 되고, 페이지 오른쪽 위에서 **X**를 선택하여 규칙을 만들지 않고 규칙 만들기를 종료할 수도 있습니다.

1. 다음 작업에서 사용할 것이므로 이 페이지를 열어 두세요.

#### 데모 5단계(선택 사항):  이전 단계에서는 의심스러운 활동의 경고를 받을 수 있도록 분석 규칙을 만들었습니다.  해당 마법사에는 특정 규칙을 기반으로 인시던트에 대한 응답을 자동화하는 옵션이 포함되어 있습니다.  자동화 구성 옵션으로 직접 이동하여 자동화 규칙을 만들 수도 있습니다.

1. 왼쪽 탐색 패널에서 **자동화**를 선택합니다.  

1. **+ 만들기**를 선택합니다. 드롭다운에서 새 플레이북 추가 또는 새 규칙 추가를 선택할 수 있습니다.  **새 규칙 추가**를 선택합니다.  
    1. 그러면 새 자동화 규칙을 만드는 창이 열립니다.  여기서도 이전 단계와 마찬가지로 규칙의 조건을 추가하고 작업을 설정할 수 있습니다.  이전 단계와 다른 점은, 첫 번째 조건이 이 자동화 규칙을 적용할 분석 규칙을 연결하는 것이라는 것뿐입니다.  이전 작업에서는 이 조건이 회색으로 표시되었습니다. 특정 규칙에 대해 자동화를 구성했기 때문입니다.  **취소**를 선택하여 새 자동화 규칙 만들기 창을 종료합니다.

1. 다음 작업에서 사용할 것이므로 이 페이지를 열어 두세요.

#### 6단계: 리소스 정리 - 강사가 수업 후에 단계 수행 Microsoft Sentinel 리소스 그룹을 삭제합니다.  Microsoft Sentinel의 대금은 Microsoft Sentinel에서 분석용으로 수집되는 데이터의 양을 기준으로 청구됩니다. 이 랩에서 수집되는 데이터의 양은 미미한 수준이지만, Microsoft Sentinel의 기능을 모두 살펴본 후에는 Microsoft Sentinel 리소스 그룹을 삭제하는 것이 좋습니다.

1. Microsoft Sentinel 페이지 왼쪽 위의 'Microsoft Sentinel' 위에서 **모든 서비스**를 선택합니다.

1. 서비스 필터 상자에 리소스 그룹을 입력한 후 제공되는 목록에서 **리소스 그룹**을 선택합니다.

1. 리소스 그룹 페이지에서 Microsoft Sentinel을 사용하여 만든 리소스 그룹인 **SC900-Sentinel-RG**를 선택합니다.

1. 페이지 위쪽 가운데의 **리소스 그룹 삭제**를 선택합니다.  경고를 검토합니다.  리소스 그룹 이름 **SC900-Sentinel-RG**를 입력하고 페이지 아래쪽에서 **삭제**를 선택합니다.  리소스 그룹을 삭제하려면 몇 분 정도 걸립니다.

1. 리소스 그룹이 삭제되었음을 확인한 후 브라우저 페이지를 닫습니다. 

#### 복습

이 데모에서는 Microsoft Sentinel 인스턴스를 만드는 프로세스를 살펴보았습니다.  그리고 Microsoft Sentinel 인스턴스와 연결된 리소스에 액세스할 수 있도록 권한을 설정하는 방법도 살펴보았습니다.  Microsoft Sentinel 인스턴스를 만든 후에는 데이터 원본에 Microsoft Sentinel을 연결하고, 기본 제공 분석 규칙을 사용하여 의심스러운 활동의 알림을 받도록 설정하는 단계를 진행했습니다. 그리고 마지막으로 자동화 기능을 살펴보았습니다. 데모의 단계를 종료한 후에는 이 데모에서 만든 Microsoft Sentinel 인스턴스와 연결된 리소스 그룹을 삭제했습니다.
