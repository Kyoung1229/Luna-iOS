# Luna-iOS
Luna는 여러 개의 단축어로 이루어진 AI 에이전트입니다. iOS의 단축어의 기능들을 사용하여, 다른 스마트폰에 탑재된 AI와 비슷한 기능들을 구현합니다.

Luna는 클라우드 AI를 사용하여 작업을 수행하며, 이를 위해 OpenAI의 API 키, 혹은 Google의 AI Studio API 키가 필요합니다. 따라서 Luna를 사용할 땐 특수한 경우를 제외하고는 사용량에 따른 비용이 발생합니다.


Luna 디스코드
- https://discord.gg/AavxXarZ

----------------

설치

1. OpenAI API 키 혹은 Google AI Studio API 키를 준비해 주세요.
2. 'Luna 설정'(https://www.icloud.com/shortcuts/3e1c3ebbce1a4eef937c2460d042b168) 단축어를 다운로드 합니다.
3. 다운로드한 단축어를 총 3번 실행, 1~3번 메뉴를 각각 한 번씩 눌러 설치를 완료해 주세요. (OpenAI / Google AI Studio 중 하나의 API 키만 저장하여도 정상작동 합니다.



Luna를 부르는 방법

시리로 실행된 경우와 아닌 경우를 구분하기 위해 Luna는 세 가지의 실행 단축어를 제공합니다.
Siri로 실행하지 않는 경우, '루나 부르기' 단축어를 통해 실행합니다.
Siri로 실행하는 경우, Siri의 입력란에 '루나' 혹은 'Luna'를 입력하여 실행합니다. (Siri로 실행되는 두 단축어는 호출 시의 언어에만 차이가 있으며, 기능상 차이가 있지는 않습니다.)
+ Luna를 처음 실행하거나 혹은 업데이트 이후의 경우 단축어가 실행됨에 따라 권한을 묻는 메시지가 여러 번 출력됩니다. 모든 메시지에 대해 허용을 눌러 주세요.

'공유 시트' 설정법
- Luna는 기사, 사진 등의 경우 공유 버튼을 눌러 Luna에게 보내는 기능을 제공합니다. 사진, 웹사이트 등의 공유 버튼을 눌러, '공유 시트'를 맨 밑까지 스크롤하여 '동작 편집' 버튼을 누른 후, 'Luna에게 보내기' 단축어를 공유 시트의 상단에 고정해 주세요.
기사를 읽거나, 사진 등을 볼 때 공유 버튼을 누른 뒤 Luna에게 보내 기사를 요약하거나, 사진에 대한 분석을 요청할 수 있습니다.

'단축어'

Luna를 부를 때, 특정 단축어를 실행하기 위한 '명령'을 추가할 수 있습니다.
ex) Luna의 입력이 '구글'인 경우 https://google.com 을 엶
'단축어'는 함수 호출의 형식을 그대로 따르며, ExecuteCore로 명령이 직접 하달되는 구조입니다.
'단축어'의 수정 및 추가에 관한 내용은 제작자에게 문의해 주세요.

Luna의 기능들

- 기기 제어(다크/라이트 모드, 벨소리 음량...)
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
- - Gemini와 ChatGPT 사이의 모델 변경
- - API 출력 결과 전문을 출력하는 디버그 모드 변경
- ChatGPT(o1 및 o1 mini)을 통해 작업 수행
- - ChatGPT의 자체 단축어 동작 통해 앱에 작업을 할당한 이후 앱 실행
- - 사용자의 직접적인 요청이 필요한 경우가 많음

주의사항

- Luna의 공식 지원 언어는 한국어이며, 영어로의 사용이
가능하기는 하나 예상치 못한 행동이 실행될 수 있습니다. (Luna only supports Korean. Using English may cause unexpected behaviors.)
- 리마인더 추가 및 집중 모드 설정: 해당 기능을 수행하는 경우, 리마인더의 경우 리마인더 폴더가 지정되지 않았을 가능성이 높습니다. 이를 해결하려면 Luna ExecuteCore 단축어에서, 조건문 'Funcname이 addReminder인 경우'를 찾아, 리마인더를 추가하는 동작에서 원하는 리마인더 폴더를 선택해 주세요. 집중 모드 설정의 경우 기본 집중 모드를 제외하고는 사용자화가 불가합니다.
- 모델을 gpt-4o로 사용할 시, 높은 사용 요금이 발생할 수 있습니다. Luna의 사용 요금을 낮추기 위해서는 Openrouter를 통한 Gemini 모델 혹은 gpt-4o-mini 모델을 사용해 주세요. (모델 변경은 Luna가 수행해 줍니다.)
- Luna는 사용자의 개인 정보를 수집하지 않으나, API 호출의 과정에서 OpenAI 혹은 Google의 서버로 개인 정보가 전송될 수 있습니다. Luna가 원활한 사용을 위해 요청 없이 가져오는 개인 정보는 건강 정보(심박수, 걸음, 수면), 현재 보고 있는 콘텐츠(웹사이트, 사진, 스크린샷), 위치 정보입니다. 이러한 개인 정보의 전송은 사용자의 요청을 수행하는 것에 필요하다고 생각되는 경우에만 이루어집니다. 

개발자 연락처

- 이메일 kyoung01122189@gmail.com
- 디스코드 kyoung_1229
