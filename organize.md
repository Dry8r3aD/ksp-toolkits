# 행사 주최자용 도움말

## 행사 준비
행사 참가자들이 사전에 충분이 준비할 수 있도록, 시간을 충분히 두고 행사를 공지하는 것이 좋습니다.
GPG Key 가 이미 있는사람이면 상관 없지만, 없는 사람이면 새로 만들어야 하며, 생성 방법과 공개키 제출 방법에 따라 시간이 많이 필요할 수 있습니다.

### 준비
행사 일시, 장소, 참가자가 준비할 사항 등을 정하고 공지합니다.

- 공개키 수집 방식
    - 키사이닝 파티에 필요한 참가자들의 공개키를 어떤 방식으로 수집할 지 정합니다.
    - 보통 이메일을 통해 제출하도록 하는 방법을 많이 사용합니다.
    - Google Form 등을 통해 수집 할 수도 있습니다.

- 제출 도움말 배포
    - 행사 공지시, 제출 방법에 대한 도움말을 같이 안내합니다.
        - 키 생성법, 생성시 주의사항, 키 생성시 준수해야 할 사항, 공개키 파일 생성 및 서명 방법, 제출 마감일시 등
        - 본 저장소에 포함된 도구를 사용해도 좋습니다.
    - 키사이닝 파티는 Web of Trust 를 확보하기 위한 행사입니다.
        - 서로 신뢰 가능한 키로 서명을 해야 하므로, 제출할 키 조건을 같이 안내하는 것도 좋습니다.
        - 2018년 기준, 아래와 같은 기준을 권장합니다. 최근 나오는 gpg 도구는 아래 기준을 거의 다 만족하는 키를 생성해 줍니다.
            - 키 길이는 3072 이상(3072 또는 4096)
            - 키 유형은 RSA and RSA 유형
            - 해싱 알고리즘은 SHA 256 이상(SHA 256 또는 SHA 512) - SHA1 은 보안 취약점이 있으므로 사용하지 않습니다.
            - 약 2년 안에 만료
            - PGP v4 버전 이상
            - Comment 필드 사용 자제
            - 이름과 이메일은 본인의 실명과 실제 많이 쓰는 이메일 주소로

- 도구 준비
    - 아래와 같은 작업을 수행하는 도구를 준비하세요.
        - 제출된 서명된 공개키를 일괄적으로 불러와 서명을 검증하는 도구
        - 서명이 검증된 공개키를 Keyring 에 저장하는 도구
        - Keyring 에서 공개키 정보 목록을 뽑아내는 도구

- 제출기간 마감 후
    - 참가자들의 이름과 공개키 정보(핑거프린트와 신원 정보(uid)) 목록이 담긴 텍스트 파일이나 PDF 파일을 생성합니다.
    - 목록 파일과 목록 파일을 검증하는 체크섬 파일을 생성하고, 이 둘을 주최자의 gpg 키로 서명하여 서명 파일도 준비합니다.
    - 준비된 파일을 배포하고, 참가자들이 다운로드 받아 아래와 같은 과정을 수행하도록 안내합니다.
        - 공개키 목록에 대해 체크섬 계산. 제공된 체크섬 파일로 공개키 목록 검증.
        - 체크섬 파일과 공개키 목록 파일의 서명 검증
        - 공개키 목록 파일 인쇄. 인쇄 후, 페이지의 체크섬 란에 본인이 계산한 체크섬 기입.
        - 행사 당일, 인쇄한 목록, 펜, 신분증 지참 안내.

## 행사 중
- 행사를 시작하기 앞서, 공개키 목록 파일의 체크섬을 프로젝터나 큰 모니터 화면 또는 큰 소리로 읽어서 안내합니다.
- 참가자들이 아래와 같은 작업을 하도록 안내합니다.
    - 서로 만나서 기입한 체크섬 일치 여부 확인
    - GPG 핑거프린트 확인
    - 공개키 신원정보와 신분증의 신원정보 확인
    - 확인 완료 후 해당 항목 체크 표시

## 행사 후
- 참가자들이 서명한 공개키를 키서버에 업로드 하거나 공개키의 주인에게 공유하도록 안내합니다.
- 키서버에 업로드된 서명 수로 통계를 내어 안내합니다.(선택사항)
