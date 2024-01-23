## MDS_HeatWaveMaintenanceNotification
How to subscribe MDS and HeatWave Maintenance Notification


MDS 및 HeatWave의 maintenance 시작과 종료에 대한 알람을 설정할 수 있음(email)

### 1. 노티를 위한 Topic 및 Subscription 생성 (create a topic for the notification)
- Developer Services > Application Integration > Notifications
- Notification를 위한 Topic 생성(Create Topic)
![Create Topic](image-2.png)
- 구독 생성 (Create a subscription with your email address)
     - Subscription Topic  리스트박스에 위에서 만든 Notification Topic명을 선택해주고,구독(Subscriptions) 화면에 고객분 이메일을 추가하시면 됩니다. 이 때 **해당 email 로 Confirm 메일이 발송됩니다. 해당 메일로 들어가셔서 링크를 클릭하셔서 confirm 하셔야 Ative 상태**가 됩니다.
![Create Subscription](image-3.png)

### 2. MDS/HeatWave Event Rule 생성

OCI Console에서 햄버거 메뉴 선택 후 
Observability & Management > Events Service > Rules 


Events Service 설정
- Create Rule (Rule 생성)
     - Rule 생성 시 rule 이름을 지정하고 아래의 Rule Condition의 Service name에 MySQL을 선택하면 MySQL 관련 event list가 Event Type 에 보여집니다. 원하시는 이벤트를 선택하시면 됩니다.
![Rele Conditions에 MySQL과 Event type 선택](image.png)


- Set the Actions for mysql notifications
    - Actions에 미리 만들어 둔 topic 선택을 선택하고 create 버튼을 클릭하시면 완료됩니다.
![Actions-만들어 둔 notification 선택](image-1.png)


### 참고자료
- [권기혁 님 Github ](https://github.com/khkwon01/MySQL_Q-A/blob/main/README.md)

- [Oracle Cloud 메뉴얼 ](https://docs.oracle.com/en-us/iaas/Content/Notification/Tasks/create-topic.htm?Highlight=%08topic)

