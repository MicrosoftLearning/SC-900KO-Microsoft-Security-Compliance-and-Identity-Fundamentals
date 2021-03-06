---
lab:
    title: 'Microsoft 365의 내부 위험 관리 기능 살펴보기'
    module: '모듈 4 단원 3: Microsoft 규정 준수 솔루션의 기능 설명: Microsoft 365의 내부 위험 기능 설명'
---


# 랩: Microsoft 365의 내부 위험 관리 기능 살펴보기

## 랩 시나리오
이 랩에서는 내부 위험 정책을 설정하는 프로세스를 단계별로 진행하고, 내부 위험 관리 정책을 구성 및 사용하려면 충족해야 하는 기본적인 필수 구성 요소를 살펴봅니다.  참고:  이 랩에서는 내부 위험 관리를 설정하려면 수행해야 하는 작업 및 정책 작성과 연관된 옵션만 파악합니다.  즉, 정책을 트리거하는 작업은 포함되어 있지 않습니다. 정책이 트리거되려면 많은 이벤트가 발생해야 하는데, 이 연습에서는 그렇게 많은 이벤트를 발생시키기는 어렵기 때문입니다.


**소요 시간**: 25-30분

#### 작업 1: 이 작업에서는 전역 관리자로 로그인하여 내부 위험 관리용 권한을 사용하도록 설정합니다.  구체적으로는 내부 위험 관리 역할 그룹에 사용자를 추가합니다. 그러면 지정된 사용자의 내부 위험 관리 기능 액세스 및 관리가 가능해집니다.  조직 전체에 사용자에게 역할 그룹 권한을 적용하려면 최대 30분이 걸릴 수 있습니다. 

1. Microsoft Edge를 엽니다. 주소 표시줄에 **admin.microsoft.com**을 입력합니다.

1. 관리자 자격 증명으로 로그인합니다.
    1. 로그인 창에 **admin@WWLxZZZZZZ.onmicrosoft.com**을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) **다음**을 선택합니다.
    
    1. 랩 호스팅 공급자가 제공한 관리자 암호를 입력합니다. **로그인**을 선택합니다.
    1. 로그인 상태를 유지할지 묻는 메시지가 표시되면 **예**를 선택합니다. 그러면 Microsoft 365 관리 센터 페이지로 이동됩니다.

1. Microsoft 365 관리 센터의 왼쪽 탐색 창에서 **모두 표시**를 선택합니다.

1. 관리 센터 아래에서 규정 준수를 선택합니다.  새 브라우저 페이지가 열리고 Microsoft 365 규정 준수 센터 시작 페이지가 표시됩니다.  

1. Microsoft 365 규정 준수 센터의 왼쪽 탐색 창에서 **권한**을 선택합니다.

1. 권한 및 역할 페이지의 규정 준수 센터 아래에서 **역할**을 선택합니다.

1. 검색 필드에 **내부 위험**을 입력하고 검색 아이콘(돋보기)을 선택합니다.  그러면 표시되는 여러 역할을 살펴봅니다.  각 역할의 액세스 수준은 서로 다릅니다.  **내부 위험 관리**를 선택합니다.

1. 그러면 열리는 창에서 구성원 옆에 있는 **편집**을 선택합니다.

1. 이 역할 그룹에 구성원을 추가하려면 **구성원 선택**을 선택합니다.

1. 페이지 위쪽에서 **+ 추가**를 선택합니다.

1. 이름 목록에서 **MOD 관리자**, **Megan Bowen**을 선택하고 페이지 아래쪽에서 **추가**를 선택합니다. 그런 후에 페이지 아래쪽에서 **완료**를 선택합니다.

1. 추가된 구성원이 정확한지 확인하고 **저장**을 선택합니다.

1. 내부 위험 관리 창 아래쪽에서 **닫기**를 선택합니다.

1. 왼쪽 탐색 패널에서 **홈**을 선택하여 Microsoft 365 규정 준수 센터 페이지로 돌아옵니다.

1. 후속 작업에서 다시 사용할 것이므로 이 브라우저 탭을 열어 두세요.


#### 작업 2(설정 랩 작업을 진행하여 감사 로그를 사용하도록 설정했으면 건너뛰어도 됨): 내부 위험 관리 기능은 Microsoft 365 감사 로그를 사용하여 정책 및 분석 인사이트에서 확인된 활동과 사용자 인사이트를 파악합니다. 이 작업에서는 감사 로그 검색 기능을 사용하도록 설정합니다. 참고:  감사 로그 검색을 활성화한 후에 감사 로그를 검색하여 결과가 반환될 때까지는 몇 시간 정도 걸릴 수도 있습니다.  즉, 감사 로그를 검색하려면 몇 시간이 걸릴 수도 있지만 이 랩의 다른 작업은 정상적으로 완료할 수 있습니다.

1. 레이블이 **홈 - Microsoft 365 규정 준수**인 브라우저 탭을 선택합니다.  이전에 이 브라우저 탭을 닫았다면 Microsoft Edge를 열고 주소 표시줄에 **compliance.microsoft.com**을 입력하여 관리자 자격 증명으로 로그인합니다.

1. 왼쪽 탐색 패널의 솔루션 아래에서 **감사**를 선택합니다.

1. **검색** 탭이 선택되어 있는지(밑줄이 표시되어 있는지) 확인합니다.

1. 감사 페이지가 표시되면 2~3분 정도 기다립니다.  감사가 사용하도록 설정되어 있지 않으면 페이지 위쪽에 사용자 및 관리자 활동 기록을 시작하라는 파란색 막대가 표시됩니다.  **사용자 및 관리자 활동 기록 시작**을 선택합니다.  감사가 사용하도록 설정되면 파란색 막대는 사라집니다.  파란색 막대가 없으면 감사가 이미 사용하도록 설정된 것이므로 추가로 작업을 수행할 필요가 없습니다.

1. 왼쪽 탐색 패널에서 홈을 선택하여 Microsoft 365 규정 준수 센터 홈 페이지로 돌아옵니다.

1. 다음 작업에서 사용할 것이므로 이 브라우저 탭을 열어 두세요.

#### 작업 3: 이 작업에서는 내부 위험 관리 솔루션과 연관된 설정을 살펴봅니다.  내부 위험 관리 설정은 정책 작성 시에 선택하는 템플릿에 관계없이 모든 내부 위험 관리 정책에 적용됩니다. 

1. Microsoft 365 규정 준수 센터 홈 페이지가 표시되어 있어야 합니다. 해당 페이지가 표시되어 있지 않으면 브라우저 탭에서 **홈 - Microsoft 365 규정 준수**를 엽니다.

1. 왼쪽 탐색 패널의 솔루션 아래에서 **내부 위험 관리**를 선택합니다.

1. 정책 설정을 시작하려면 몇 가지 설정을 구성해야 합니다..  내부 위험 관리 페이지 오른쪽 위의 **설정 기어 아이콘**을 선택하여 내부 위험 설정에 액세스합니다.  
    1. **개인 정보** 탭이 표시되는지 확인합니다.  내부 위험 정책 적용 대상 활동을 수행하는 사용자의 경우 이 설정에 따라 해당 사용자의 실제 이름을 표시할지, 아니면 익명 처리된 버전을 사용하여 신원을 마스킹 처리할지가 결정됩니다.  **익명 처리된 사용자 이름 표시 안 함**을 선택하고 **저장**을 선택합니다.
    
    1. **정책 표시기** 탭을 선택합니다. 정책을 트리거하는 이벤트가 발생하면 선택한 표시기에 해당되는 활동을 사용하여 해당 사용자의 위험 점수를 결정합니다. 여기서 선택하는 정책 표시기가 내부 위험 정책 템플릿에 포함됩니다.  화면을 스크롤하여 사용 가능한 모든 표시기 및 관련 정보를 확인합니다. **Office 표시기** 아래에서 **모두 선택**을 선택하고 **저장**을 선택합니다.
    1. **정책 기한** 탭을 선택합니다. 사용자가 내부 위험 정책 적용 대상 활동을 수행하여 정책이 트리거되면 여기서 선택하는 기한이 적용됩니다.   활성화 창에서 설정하는 옵션에 따라 정책이 사용자의 활동을 실제로 감지할 기간이 결정됩니다. 사용자가 정책과 일치하는 활동을 처음 수행하면 트리거됩니다. 지난 활동 감지: 정책이 사용자 활동을 소급 감지하는 기간이 결정됩니다. 사용자가 정책과 일치하는 활동을 처음 수행하면 트리거됩니다.  기본값을 그대로 둡니다.  **지능형 검색** 탭을 선택합니다.
    1. **지능형 검색** 탭을 선택합니다. 이 탭의 옵션을 검토합니다.  구체적으로는 도메인 설정, 그리고 이러한 설정과 표시기의 관계를 살펴봅니다.
    1. 설정에 나와 있는 기타 항목을 살펴봅니다. 대다수 항목은 미리 보기 상태입니다.

1. 내부 위험 관리 개요로 돌아오려면 페이지 왼쪽 위의 설정 위에 있는 **내부 위험 관리**를 선택합니다.

1. 다음 작업에서 사용할 것이므로 이 브라우저 탭을 열어 두세요.

#### 작업 4:  이 작업에서는 정책 만들기를 진행합니다.

1. 내부 위험 관리 페이지가 표시되어 있어야 합니다.  해당 페이지가 표시되어 있지 않으면 레이블이 **내부 위험 관리 - Microsoft 365 규정 준수**인 브라우저 탭을 엽니다.

1. 내부 위험 관리 개요 페이지에서 **정책** 탭을 선택한 다음 **+ 정책 만들기**를 선택합니다.  다음의 각 정책 탭을 구성합니다.

    1. 정책 템플릿:  범주 목록에서 **데이터 유출**을 선택하고 **일반 데이터 유출**을 선택합니다.  범주 내의 템플릿에 추가 필수 구성 요소가 적용될 수도 있습니다.  이 템플릿과 연관된 세부 정보를 확인하고 **다음**을 선택합니다.
    
    1. 이름 및 설명:  이름으로 **SC900-InsiderRiskPolicy**를 입력하고 **다음**을 선택합니다.
    1. 사용자 및 그룹:  정보 상자를 검토합니다.  기본 설정인 **모든 사용자 및 그룹 포함**을 그대로 유지합니다.  **다음**을 선택합니다.
    1. 우선 순위를 설정할 콘텐츠: 설명을 확인합니다. **SharePoint 사이트, 민감도 레이블 및/또는 중요한 정보 유형을 우선 순위 콘텐츠로 지정**을 선택하고 **다음**을 선택합니다.
        1. SharePoint 사이트: 이 정책 예제에서는 해당 필드를 비워 두고 **다음**을 선택합니다.
        1. 중요한 정보 유형: 이 정책 예제에서는 해당 필드를 비워 두고 **다음**을 선택합니다. 
        1. 민감도 레이블: **+ 민감도 레이블 추가 또는 편집**을 선택합니다.  목록에 나와 있는 레이블인  **Confidential Finance** 및 **Highly Confidential\Project – Falcon**을 선택하고 **추가**, **다음**을 차례로 선택합니다.
    1. 트리거: 세부 정보를 검토합니다.  사용자가 정의된 반출 활동을 수행하거나(각 글머리 기호의 정보 아이콘을 선택하면 추가 세부 정보 확인 가능), 기존 DLP(데이터 손실 방지) 정책과 일치하는 활동을 수행하면 정책이 트리거됩니다.  이 연습에서는 DLP 정책을 구성하지 않았으므로 **사용자가 반출 활동 수행**을 선택합니다.  이전 작업에서 사용하도록 설정한 정책 표시기가 선택되어 있습니다.   이러한 표시기는 정책이 트리거되어야 활성화되며, 표시기가 활성화되면 이러한 표시기에 해당하는 활동을 사용하여 해당 사용자의 위험 점수를 계산합니다. **다음**을 선택합니다.
    1. 표시기 임계값:  여기서는 표시기와 연관된 기본 임계값 또는 사용자 지정 임계값을 지정할 수 있습니다.  표시기는 정책이 트리거되어야 활성화되므로, 정책 트리거 시에는 이러한 임계값이 영향을 주지 않습니다. **사용자 지정 임계값 지정**을 선택합니다. 이 옵션을 선택하면 현재 기본값을 확인할 수 있습니다. 기본값을 그대로 적용하고 **다음**을 선택합니다.  
    1. 표시기: 이전 작업에서 선택한 모든 Office 표시기가 선택되어 있습니다.  해당 페이지를 스크롤하여 사용 가능한 기타 정책 표시기 및 자동으로 선택되는 기타 항목을 확인합니다.   시퀀스 검색도 사용하도록 설정됩니다.  즉, 정의된 활동 시퀀스가 검색되면 위험이 더욱 심각하다는 정보가 표시됩니다.  정보 아이콘 위에 마우스를 올리면 자세한 정보를 확인할 수 있습니다.  이러한 항목을 확인하려면 특정 표시기를 선택해야 하며 디바이스를 온보딩해야 합니다.  여기서는 이 테넌트에 온보딩된 디바이스가 없으므로 작업을 간단하게 진행하기 위해 **모두 선택**을 선택 취소합니다. 
    1. 마침:  설정을 검토하고 **제출**, **완료**를 차례로 선택합니다.

1. 그러면 내부 위험 관리 페이지의 정책 탭이 다시 표시됩니다.  그리고 방금 만든 정책이 표시됩니다.  

1. 방금 만든 정책에 따라 현재 위험 점수가 할당되어 있는 사용자가 "범위 내의 사용자" 필드에 표시됩니다.  정책이 트리거되면 사용자에게 위험 점수가 할당됩니다. 따라서 현재는 점수의 값이 0으로 표시됩니다.  관리자는 선택한 정책에서 검색하는 활동에 따라 특정 사용자를 대상으로 위험 점수 할당을 시작하도록 정책을 구성할 수 있습니다. 이렇게 하면 트리거 이벤트가 먼저 검색되어야 점수가 할당되는 요구 사항이 무시됩니다.  이렇게 하려면 정책 이름 옆의 빈 원을 선택하여 정책을 선택한 후 정책 테이블 위에 표시되어 있는 **사용자의 활동 채점 시작**을 선택합니다.  각 필드에 내용을 입력하고 **활동 채점 시작**을 선택합니다.  '사용자' 탭에 사용자가 표시될 때까지는 최대 24시간이 걸릴 수 있습니다. 이 시간이 지나면 해당 탭에서 사용자를 선택하여 검색된 활동을 검토할 수 있습니다.  창 아래쪽의 **닫기**를 선택합니다.

#### 복습
이 랩에서는 내부 위험 정책을 설정하는 프로세스를 단계별로 진행했으며, 내부 위험 관리 정책을 구성 및 사용하려면 충족해야 하는 기본적인 필수 구성 요소를 살펴보았습니다.
