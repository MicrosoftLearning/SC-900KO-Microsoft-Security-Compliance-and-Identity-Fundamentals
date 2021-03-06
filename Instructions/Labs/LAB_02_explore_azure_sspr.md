---
lab:
    title: '셀프 서비스 암호 재설정을 사용하는 Azure AD 인증 방식 살펴보기'
    module: '모듈 2 단원 2: Microsoft ID 및 액세스 관리 솔루션의 기능 설명: Azure AD의 다양한 인증 방법 설명'
---

# 랩: 셀프 서비스 암호 재설정을 사용하는 Azure AD 인증 방식 살펴보기

## 랩 시나리오

이 랩에서는 관리자로 로그인하여 셀프 서비스 암호 재설정을 사용하도록 설정하는 프로세스를 진행합니다. SSPR을 사용하도록 설정한 후에는 사용자 역할로 로그인하여 SSPR에 등록하고 암호를 재설정하는 프로세스를 진행합니다.  마지막으로 다시 관리자로 로그인하여 SSPR의 감사 로그 및 사용 데이터와 인사이트를 확인합니다.

**소요 시간**: 15-20분


#### 작업 1:  이 작업에서는 관리자로 로그인하여 기존 사용자인 Adele Vance를 SSPRSecurityUsers 그룹에 추가합니다.  또한 사용자로 처음 로그인하고 SSPr에 등록을 할 수 있도록 사용자 암호 재설정을 수행해야 합니다.

1. Microsoft Edge를 엽니다.

2. 주소 표시줄에 **portal.azure.com** 을 입력하고 관리자 자격 증명을 사용하여 로그인합니다.
    1. 로그인 창에 **admin@WWLxZZZZZZ.onmicrosoft.com** 을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) **다음**을 선택합니다.
    1. 랩 호스팅 공급자가 제공한 관리자 암호를 입력합니다. **로그인**을 선택합니다.
    1. 로그인 상태를 유지할지 묻는 메시지가 표시되면 **예**를 선택합니다.

3. **Azure Active Directory**를 선택합니다.  

4. 왼쪽 탐색 패널에서 **그룹**을 선택합니다.

5. 기존 그룹 목록이 표시됩니다. 그룹 검색 필드에 **SSPR**을 입력하고 검색 결과에서 **SSPRSecurityGroupUsers**를 선택합니다.  그러면 이 그룹의 구성 옵션이 표시됩니다.

6. 왼쪽 탐색 창에서 **구성원**을 선택합니다.

7. 페이지 위쪽에서 **+ 구성원 추가**를 선택합니다.  

8. 검색 상자에 **Adele**을 입력합니다.  **Adele Vance** 사용자가 검색 상자 아래에 표시되면 해당 사용자를 선택하고 페이지 아래쪽의 **선택**을 누릅니다.

9. 화면 오른쪽 위에서 **X**를 선택하여 SSPRSecurityUseres 창을 닫습니다.

10. Active Directory 페이지로 돌아옵니다. 이렇게 하려면 화면 왼쪽 위의 그룹 바로 위에 있는 **Contoso**를 선택하여 Contoso Azure Active Directory 페이지로 돌아옵니다.

11. 왼쪽 탐색 패널에서 **사용자**를 선택합니다.

12. 사용자 목록에서 **Adele Vance**를 선택합니다.

13. 페이지 위쪽에서 **암호 재설정**을 선택합니다. 이전에 Adele Vance로 로그인한 적이 없으므로 암호를 재설정해야 합니다.

14. 암호 재설정 창이 열리면 **암호 재설정**을 선택합니다.  중요: 다음 작업에서 사용자로 로그인하려면 새 암호가 필요하므로 새 암호를 적어 두세요.

15. 페이지 오른쪽 위에서 **X**를 선택하여 암호 재설정 창을 닫습니다.

16. 페이지 오른쪽 위에서 **X**를 선택하여 Adele Vance 창을 닫습니다.

17. 페이지 오른쪽 위에서 **X**를 선택하여 사용자 창을 닫습니다.

18. 후속 작업에서 사용할 것이므로 Contoso 개요 창은 열어 두세요.

#### 작업 2: 이 작업에서는 관리자로 로그인한 상태로 사용자의 암호 재설정을 구성하는 방법을 알아봅니다. 이 과정에서 사용할 인증 방법의 유형을 구성합니다.

1. 브라우저에 열려 있는 Contoso – Microsoft Azure 탭으로 이동합니다. 이전에 해당 탭을 닫았다면 브라우저 페이지를 열고 주소 표시줄에 portal.azure.com을 입력한 후에 Azure Active Directory를 선택합니다.  Azure Portal에 관리자로 로그인되어 있는 상태여야 합니다. 관리자로 로그인되어 있지 않으면 다시 로그인합니다.

2. 왼쪽 탐색 창에서 **암호 재설정**을 선택합니다.  

3. 셀프 서비스 암호 재설정의 속성이 표시됩니다.  나열되어 있는 그룹인 **SSPRSecurityUsers** 에 대해 **셀프 서비스 재설정**이 **선택**되어 있는지 확인합니다.  "그룹 선택" 옆의 정보 아이콘 위에 커서를 올립니다. 그런 후 "자신의 암호를 재설정할 수 있는 사용자 그룹을 정의함" 옵션을 확인합니다. 해당 그룹에 사용자를 포함해야 하며 사용자를 개별적으로 선택할 수는 없습니다.  그리고 그룹을 변경하면 선택하는 그룹이 현재 목록의 그룹 대신 사용됩니다.  그러므로 SSPR 그룹에만 사용자를 추가하는 것이 좋습니다.  마지막으로, "이 설정은 조직 내 최종 사용자에게 적용됩니다."라는 메시지가 표시된 연한 파란색 상자를 확인합니다. 관리자는 항상 셀프 서비스 암호 재설정을 진행할 수 있으며, 두 가지 인증 방법을 사용하여 암호를 재설정해야 합니다.

5. 암호 재설정의 왼쪽 탐색 패널에서 **인증 방법**을 선택합니다.

6. 재설정에 필요한 방법 수에서 **1**을 선택합니다. 화면에 표시되는 정보 상자에서

7. 사용자에게 제공되는 다양한 방법을 살펴봅니다.  **이메일**과 **휴대폰(SMS에만 해당)** 이 이미 선택되어 있어야 합니다. 이 두 옵션이 선택되어 있지 않으면 선택합니다.

8. 암호 재설정의 왼쪽 탐색 패널에서 **등록**을 선택합니다.  

9. 로그인 시 사용자가 등록을 해야 합니까? 설정이 **예**로 설정되어 있는지 확인합니다.  사용자에게 해당 인증 정보를 다시 확인하도록 요청하기까지의 기간은 기본값인 180으로 유지합니다.   페이지에 표시되는 정보 상자를 살펴봅니다.

10. 암호 재설정의 왼쪽 탐색 패널에서 **알림**을 선택합니다.  

11. 암호가 재설정되는 경우 사용자에게 알리시겠습니까? 설정이 **예**로 설정되어 있는지 확인합니다.  다른 관리자가 암호를 재설정하는 경우 모든 관리자에게 알리시겠습니까? 설정은 아니요로 유지합니다.

12. 암호 재설정 탐색 창에는 감사 로그 보기 옵션과 사용량 및 인사이트 옵션도 포함되어 있습니다.

13. 화면 오른쪽 위의 이메일 주소 옆에 있는 사용자 아이콘을 클릭하여 모든 브라우저 탭에서 **로그아웃**합니다. 그런 다음 브라우저 창을 모두 닫습니다.


#### 작업 3:  이 작업에서는 Adele Vance 사용자로 로그인하여 셀프 서비스 암호 재설정 등록 프로세스를 진행합니다.  이 작업을 진행하려면 문자 메시지를 받을 수 있는 모바일 디바이스 또는 액세스 가능한 개인 이메일 계정을 사용할 수 있어야 합니다.
 
1. Microsoft Edge를 엽니다.

2. 주소 표시줄에 **login.microsoftonline.com** 을 입력합니다.

3. Adele Vance로 로그인합니다.
    1. 로그인 창에 **AdedleV@WWLxZZZZZZ.onmicrosoft.com** 을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) **다음**을 선택합니다.
    1. 이전 작업에서 적어 둔 암호를 입력합니다. **로그인**을 선택합니다.
    1. 로그인 상태를 유지할지 묻는 메시지가 표시되면 **예**를 선택합니다.

4. Adele Vance로 처음 로그인했으므로 암호를 재설정하라는 메시지가 표시됩니다.  이전 암호를 입력합니다.  새 암호로는 **SC900-Lab**을 입력합니다. 암호 확인 필드에 **SC900-Lab**을 입력합니다.  **로그인**을 선택합니다.  참고: 이 암호는 랩에서 편의상 사용하는 것입니다. 일반적으로는 모범 사례에 따라 더욱 안전한 암호를 입력해야 합니다.

5. 추가 정보가 필요하다는 팝업이 표시됩니다.  Adele Vance는 SSPRSecurityUsers 그룹의 구성원인데, 그룹의 구성에 따라 해당 구성원은 로그인할 때 등록을 해야 하기 때문입니다. **다음** 단추를 선택합니다.  참고:  관리자가 사용자를 추가할 때 인증 방법을 직접 구성하여 사용자가 직접 등록을 진행하도록 할 수도 있습니다. 이렇게 하려면 관리자는 사용자가 셀프 서비스 암호 재설정을 수행하여 사용자 암호를 재설정하는 데 사용하는 전화 번호와 이메일 주소를 알고 있어야 하며 해당 정보를 설정해야 합니다.

6. "계정 보안 유지" 페이지가 열립니다.  그러면 전화 인증 방법용 창이 열립니다. 문자 메시지를 받을 수 있는 모바일 디바이스가 없으면 다음 단계로 건너뜁니다.  전화 번호를 입력하라는 메시지가 표시됩니다. **코드를 문자로 받기** 옵션이 사용하도록 설정되어 있는지 확인합니다.   문자 코드를 받을 수 있는 전화 번호를 입력하고 **다음** 단추를 선택합니다.  새 창이 열리고 입력한 전화 번호로 코드가 전송되었다는 메시지가 표시됩니다.  수신된 코드를 입력하고 **다음**을 선택합니다. 그러면 열리는 창에 인증이 정상적으로 완료되었다는 메시지와 기본 로그인 방법이 표시됩니다.  **완료**를 선택합니다.  

7. 휴대폰 번호로 SSPR을 구성할 수 있었다면 이 단계를 건너뛰세요.  창 왼쪽 아래에 나와 있는 다른 방법을 설정할 수도 있습니다.  다른 방법을 설정하기로 선택하는 경우에는 **다른 방법을 설정하고 싶습니다.** 를 선택합니다. 그러면 표시되는 팝업 창에 "어떤 방법을 사용하시겠습니까?" 메시지가 표시됩니다.  드롭다운에서 원하는 방법을 선택합니다. 여기서는 **이메일**을 선택하고 **확인** 단추를 선택합니다.  사용할 이메일을 입력하고 **다음**을 선택합니다.  새 창이 열리고 입력한 이메일로 코드가 전송되었다는 메시지가 표시됩니다.  입력한 이메일에 액세스하여 코드를 확인합니다.  수신된 코드를 입력하고 **다음**을 선택합니다. 그러면 열리는 창에 인증이 정상적으로 완료되었다는 메시지와 기본 로그인 방법이 표시됩니다.  **완료**를 선택합니다.

8. 이제 로그인을 완료할 수 있습니다. 로그인을 완료하면 Azure Portal 방문 페이지가 표시됩니다.  로그인 시간이 만료되었다는 메시지가 표시되는 경우 암호 SC900-Lab만 다시 입력하면 됩니다.

9. Azure Portal에서 로그아웃하고 브라우저 창을 닫습니다. 

#### 작업 4(선택 사항): 이 작업에서는 Adele Vance 사용자로 로그인하여 암호 재설정 프로세스를 진행합니다.

1. Microsoft Edge를 엽니다.

2. 주소 표시줄에 login.microsoftonline.com을 입력합니다.

3. **AdeleV@WWLxZZZZ.onmicrosoft.com** 이메일을 입력하여(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) Adele Vance로 로그인하고 **다음** 단추를 선택합니다. 계정 선택 창이 열릴 수도 있습니다. 그러면 Adele Vance의 계정을 선택합니다.

4. 암호 입력 창에서 **암호를 잊어버렸음**을 선택합니다. 

5. 계정으로 돌아가기 창이 열립니다.   이메일 또는 사용자 이름 상자에 Adele Vance의 이메일인 AdeleV@WWLxZZZZ.onmicrosoft.com이 표시되는지 확인합니다.  해당 이메일이 표시되지 않으면 상자에 이메일을 입력합니다.  

6. 이미지에 표시되어 있는 문자나 오디오에서 들리는 단어를 비어 있는 상자에 입력합니다. 해당 정보를 입력한 후 **다음**을 선택합니다.

7. 화면에 계정으로 돌아가기가 표시되고 확인 1단계 > 새 암호 선택이 표시됩니다. 기본 설정인 **내 휴대폰으로 문자 메시지 보내기**를 그대로 유지합니다.  휴대폰 번호를 입력하라는 메시지가 표시됩니다.  휴대폰 번호를 입력한 후 **문자** 단추를 선택합니다.  등록 중에 이메일을 선택한 경우에는 계정으로 돌아기가 창에 확인 코드가 포함된 이메일이 대체 이메일 주소로 수신되었다는 메시지가 표시됩니다.  **이메일**을 선택합니다. 

8. 확인 코드를 입력하고 **다음**을 누릅니다.

9. 다음 화면에 새 암호를 입력하고 확인하라는 메시지가 표시됩니다.  새 암호와 확인 암호를 입력하고 **마침** 단추를 선택합니다.

10. 암호가 재설정되었다는 메시지가 화면에 표시됩니다. **여기를 클릭하세요.** 를 선택하여 새 암호로 로그인합니다.

11. 계정 정보 선택 상자에 **AdeleV@WWLxZZZZZZ.onmicrosoft.com**과 새 암호를 입력하고 **로그인** 단추를 선택합니다.  로그인 상태를 유지할지 묻는 메시지가 표시되면 **아니요**를 선택합니다.

12. 이제 Azure Portal이 표시됩니다.

13. 화면 오른쪽 위의 이메일 주소 옆에 있는 사용자 아이콘을 선택한 후 **로그아웃**을 선택하여 로그아웃합니다. 그런 다음 브라우저 창을 모두 닫습니다.

#### 작업 5(선택 사항):  이 작업에서는 관리자로 로그인하여 암호 재설정과 관련된 감사 로그와 사용량 및 인사이트 데이터를 간략하게 살펴봅니다.

1. Microsoft Edge를 엽니다.

2. 주소 표시줄에 **portal.azure.com**을 입력합니다. 

3. 관리자 자격 증명으로 로그인합니다.
    1. 로그인 창에 **admin@WWLxZZZZZZ.onmicrosoft.com**을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) **다음**을 선택합니다.
    1. 랩 호스팅 공급자가 제공한 관리자 암호를 입력합니다. **로그인**을 선택합니다.
    1. 로그인 상태를 유지할지 묻는 메시지가 표시되면 **예**를 선택합니다.

4. **Azure Active Directory**를 선택합니다.  

5. 왼쪽 탐색 창에서 **암호 재설정**을 선택합니다.

6. 왼쪽 탐색 창에서 **감사 로그**를 선택합니다.  제공되는 정보와 사용 가능한 필터를 확인합니다.  로그를 다운로드할 수도 있음을 확인합니다.  

7. **다운로드**를 선택합니다.  다운로드 형식은 CSV 또는 JSON으로 지정할 수 있습니다.  화면 오른쪽 위에서 **X**를 선택하여 창을 닫습니다.

8. 왼쪽 탐색 창에서 **사용량 및 인사이트**를 선택합니다.

9. 등록과 관련하여 제공되는 정보를 확인합니다.  데이터를 새로 고친 후에도 이 데이터가 갱신되려면 시간이 다소 걸릴 수 있습니다. 그러므로 이전 작업의 등록 또는 사용량 데이터가 아직 반영되어 있지 않을 수도 있습니다.

10. 페이지 위쪽에서 **사용량**을 선택하여 셀프 서비스 암호 재설정 횟수 및 방법별 계정 잠금 해제 횟수를 확인합니다.  데이터를 새로 고친 후에도 이 데이터가 갱신되려면 시간이 다소 걸릴 수 있습니다. 그러므로 이전 작업의 사용량 데이터가 아직 반영되어 있지 않을 수도 있습니다.

11. 열려 있는 브라우저 탭을 닫습니다.


#### 복습
이 랩에서는 관리자로 로그인하여 셀프 서비스 암호 재설정을 사용하도록 설정하는 프로세스를 진행했습니다. SSPR을 사용하도록 설정한 후에는 사용자 역할로 로그인하여 SSPR에 등록하고 암호를 재설정하는 프로세스를 진행했습니다.  마지막으로 다시 관리자로 로그인하여 SSPR의 감사 로그와 사용량 및 인사이트 데이터를 확인했습니다.
