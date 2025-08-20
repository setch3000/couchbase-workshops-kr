# Couchbase Server Administration

### 실습 목표

본 실습에서는 Couchbase Server를 소개하며, 단일 노드 설치 및 웹 UI를 중심으로 진행합니다. 향후 실습에서는 Couchbase의 관리 및 구성 요소를 보다 심층적으로 다룰 예정이므로, 본 실습의 내용은 Couchbase에 대한 첫 단계의 이해를 위한 것으로 보시면 됩니다.

본 실습의 주요 목적은 운영 환경 수준의 클러스터 구축이 아니라, 다양한 개념과 기능을 설명하고 시연할 수 있는 프로토타입 실습 환경을 마련하는 데 있습니다.

예를 들어, 본 실습에서는 Linux 방화벽을 단순히 비활성화하며, Couchbase 데이터 파일과 인덱스 파일을 별도의 장치/볼륨에 분리 저장하는 모범 사례를 따르지 않습니다. 또한 본 실습에 사용되는 Amazon VM은 t2.large 인스턴스로, 2코어와 8GB 메모리만 제공합니다.

이러한 VM은 Couchbase 클러스터에서 기대할 수 있는 실제 성능을 반영하지 않습니다. 즉, 소형 VM에서 초당 약 15,000 IOPS 성능이 관찰될 수 있으나, 더 큰 Amazon VM 환경에서는 초당 100,000 IOPS, 물리적 데이터 센터 환경에서는 초당 200,000 IOPS 이상의 성능을 확인할 수 있습니다.

본 실습 또는 향후 실습과 관련된 의견이나 수정 사항은 Couchbase Learning Services (cls@couchbase.com) 으로 보내주시기 바랍니다.

예상 소요 시간: 약 1시간



### Couchbase 서버 설치 소개

아래는 Couchbase Server의 설치 및 관리에 대해 더 배우고 싶을 때, 여유 시간에 직접 살펴볼 수 있는 링크들입니다.\
이 가이드들의 핵심적이고 중요한 부분은 이번 수업에서 진행할 축약된 실습으로 정리되어 있습니다.\
그러나 Couchbase 관리에 대해 심도 있게 학습하려면 반드시 이 문서들을 읽고 시간을 투자해야 합니다.

• Couchbase 공식 문서 전체 (HTML 형식):\
https://docs.couchbase.com/home/index.html

• Couchbase Server 7.X 공식 관리자 가이드\
(좌측 상단의 파란색 드롭다운에서 “Couchbase Server”를 선택해 다양한 주제를 탐색할 수 있습니다):\
https://docs.couchbase.com/server/current/getting-started/start-here.html\
\
• Couchbase YouTube 채널 – 최근 컨퍼런스와 웨비나 영상 다수:\
https://www.youtube.com/c/CouchbaseServer/\
\
• Couchbase 자료 아카이브에서 최신 NoSQL 리소스 얻기:\
https://www.couchbase.com/resources\
\
• 다양한 무료 온라인 교육:\
http://training.couchbase.com\
\
• Couchbase 커뮤니티에서 공유된 프레젠테이션 및 슬라이드:\
https://connectondemand.couchbase.com\
\
• Couchbase 최신 기술 동향을 다루는 공식 블로그:\
http://blog.couchbase.com\
\
• Couchbase 커뮤니티 웹사이트 (기술 질문 게시 가능):\
http://www.couchbase.com/open-source
