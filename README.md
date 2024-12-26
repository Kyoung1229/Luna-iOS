# Luna-iOS
iOS를 위한 AI 에이전트

Luna는 여러 개의 단축어로 이루어진 AI 에이전트입니다. iOS의 단축어의 기능들을 사용하여, 구글, 삼성 등의 스마트폰에 탑재된 AI와 비슷한 기능들을 구현합니다.

Luna는 클라우드 AI를 사용하여 작업을 수행하며, 이를 위해 OpenAI의 API 키, 혹은 Openrouter의 API(정확히는 구글의 Gemini 모델) 키가 필요합니다. 이에 따라 Luna를 사용할 때는 특수한 경우를 제외하고는 사용량에 따른 비용이 부과됩니다.

설치
1. Luna.zip을 나의 iPhone/나의 iPad에 압축을 풀어 넣습니다(압축 파일을 해당 위치에 이동한 후 한 번 클릭하면 압축 해제가 가능합니다.)
2. 아래 기재된 iCloud 링크를 모두 클릭해 단축어를 추가하고, 필요한 경우 이를 하나의 단축어 폴더에 이동시킵니다. (권장)
3. 'Luna 초기 설정' 단축어를 실행하고, API 키를 붙여넣은 뒤 확인을 누릅니다.
- 설치 완료!

실행법
시리로 실행된 경우와 아닌 경우를 구분하기 위해 Luna는 세 가지의 실행 단축어를 제공합니다.
Siri로 실행하지 않는 경우, '루나 부르기'를 통해 실행합니다.
Siri로 실행하는 경우, '루나' 혹은 'Luna'를 통해 실행합니다. (Siri로 실행되는 두 단축어는 처음 불렀을 시의 언어에만 차이가 있으며, 기능상 차이가 있지는 않습니다.)

'단축어'
Luna를 처음 부를 때, 특정 단축어를 실행하기 위한 '명령'을 추가할 수 있습니다.
ex) Luna의 입력이 '애플닷컴'인 경우 'https://apple.com'을 엶
'단축어'는 함수 호출의 형식을 그대로 따르며, ExecuteCore로 명령이 직접 하달되는 구조입니다.
'단축어'의 수정 및 추가에 관한 내용은 제작자에게 문의해 주세요.

Luna의 기능들
- 다양한 기기 제어(다크/라이트 모드, 벨소리 음량...)
- 타이머 설정 및 해제
- 집중 모드 설정(주의사항 필독)
- 전화 걸기/메시지 전송
- 리마인더 추가(주의사항 필독)
- 기억
- - 사용자의 정보 저장
- - 필요한 경우 기억 불러옴
- 정보 요청
- - 며칠 동안의 날씨 정보, 현재 보고 있는 웹사이트, 사진 촬영, 스크린샷, 건강 정보 등을 통해 사용자의 요청 작업을 원활하게 수행
- 모델 및 디버그 모드 변경
- - 제미니와 ChatGPT 사이의 모델 변경
- - API 출력 결과 전문을 출력하는 디버그 모드 변경
ChatGPT(o1 및 o1 mini)을 통해 작업 수행
- - ChatGPT의 자체 단축어 동작 통해 앱에 작업을 할당한 이후 앱 실행
- - 사용자의 직접적인 요청이 필요한 경우가 많음

주의사항
- Luna의 공식 지원 언어는 한국어이며, 영어로의 사용이
가능하기는 하나 예상치 못한 행동이 실행될 수 있습니다. (Luna only supports Korean. Using English may cause unexpected behaviors.)
- 핵심 기능은 Openrouter를 통해 구동이 가능하나, 초기 실행 모델로 gpt-4o를 사용하고, 기억 저장의 경우 gpt-4o-mini 모델을 사용하므로 ChatGPT의 API 키는 초기 설정 시 필요합니다.
- Openrouter를 통한 사용의 경우 Gemini를 제외한 다른 모델을 사용할 경우, 함수 호출 기능이 있는 LLM 모델이 아니라면 에이전트 기능들이 작동하지 않습니다.
- 리마인더 추가 및 집중 모드 설정: 해당 기능을 수행하는 경우, 리마인더의 경우 리마인더 폴더가 지정되지 않았을 가능성이 높습니다. 이를 해결하려면 Luna ExecuteCore 단축어에서, 조건문 'Funcname이 addReminder인 경우'를 찾아, 리마인더를 추가하는 동작에서 원하시는 리마인더 폴더를 선택해 주세요. 집중 모드 설정의 경우 기본 집중 모드를 제외하고는 사용자화가 불가합니다.
- 모델을 gpt-4o로 사용할 시, 사용 요금이 높게 나올 수 있습니다. Luna의 사용 요금을 낮추기 위해서는 Openrouter를 통한 Gemini 모델을 사용하시거나, gpt-4o-mini 모델틀 사용해 주세요. (모델 변경은 Luna가 수행해 줍니다.)

단축어 다운로드용 iCloud 링크
1. Luna 초기 설정
https://www.icloud.com/shortcuts/72f4713fc2b94b7184145ccda4bba155

3. Luna Core - ChatGPT
https://www.icloud.com/shortcuts/ec1960913a6742b28e3577df290cf7ca

4. Luna Core - Gemini
https://www.icloud.com/shortcuts/bef2cb9974a544e19faf56f76ba38f3a

5. Luna ExecuteCore
https://www.icloud.com/shortcuts/4e20ce652ba74196a980bf0f2d1b5a71

7. Luna GetControl
https://www.icloud.com/shortcuts/28b7b124fe9440ca8a42b2dbf765ca3c

8. Luna SaveControl
https://www.icloud.com/shortcuts/3ba2fd837b3f469f868a48879f3511f2

9. Luna Fetch
https://www.icloud.com/shortcuts/8b5e13d10e624467958e8b0d690c9f44

10. Luna WeatherInfo
https://www.icloud.com/shortcuts/c4d1596f24524040abf409d5aee984bd

11. Luna ODIP
https://www.icloud.com/shortcuts/70efe684a0f34aef944718c5f602c116

12. Luna에게 보내기
https://www.icloud.com/shortcuts/96fbdee10ede4d25a54a6b1b20d1a3a4

13. 루나 데이터셋 추가
https://www.icloud.com/shortcuts/3d5e858940794ac4b8441119cc72fb3c

14. Luna setLunaSettings
https://www.icloud.com/shortcuts/7bc512f1e811402086eb902df063b025

--루나 호출 및 편의기능--
1. 루나 부르기
https://www.icloud.com/shortcuts/0ec481c3231441df8b19dcdc4949a1ec

2. 루나&Luna(Siri)
https://www.icloud.com/shortcuts/4a61ca003d6b4960856a244138712309
https://www.icloud.com/shortcuts/02cf2a36fecf40739d0215a4f1e6fa93

3. Edit functions(함수 호출 수정용)
https://www.icloud.com/shortcuts/7c9b98194a1e4aac952da3feda02f7c5

4. Luna Shortcut
https://www.icloud.com/shortcuts/e3494ef6d8b649b1b730d10de9a13f2a

5. LS Edit Add
https://www.icloud.com/shortcuts/7651065634c84cd5b06d65b4e06581c8

개발자 연락처
이메일 kyoung01122189@gmail.com
디스코드 kyoung_1229
