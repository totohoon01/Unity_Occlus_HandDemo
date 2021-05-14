# 유니티-오큘러스 Hand_Tutorials

## Before Started
- 안드로이드로 스위칭


## Setup
- https://assetstore.unity.com/packages/tools/integration/oculus-integration-82022 패키지 다운로드
    - Occulus, Resource 폴더가 생성
    - VR폴더에 개발에 필요한 에셋들이 포함
    - VR / Prefabs
        - OVRCameraRig : 카메라, VR하드웨어에 접근가능
        - OVRPlayerController : 플레이어 움직임(컨트롤러)
        - OVRHandPrefab : hand 입력 관련
    - 빌드
        - XR Plugin Management에 Occulus 추가
        - Vulkan ㅂㅂㅇ
        - 오큘러스 앱 개발자모드 온
        - 사이드퀘스트 설치(컴퓨터)




## Hand Tracking
- https://developer.oculus.com/documentation/unity/unity-handtracking/
- How Does it work?
    - Hand Pose와 Key Points를 트래킹한다.
    - point, pinch, unpinch, scroll, and palm pinch의 여러 제스쳐 가능
    - 컨트롤러가 필요할 정도의 정확도있는 작업을 대체할 목적은 아님(핸드 트래킹은 옵션으로 개발해라)

- Get Started with Hands Setup
    - Setup Camera
        1. 프로젝트 생성
        2. <b>OVRCameraRig</b> 추가
        3. open the <b>OVR Manager settings</b>(스크립트)
        4. Under <b>Tracking</b>, from the <b>Tracking Origin Type</b> list, select <b>Floor Level</b> 설정
    
    - Select Hands as Input
        1. Quest Features -> Hand Tracking Support -> Controllers and Hands -> Hands Only(입력장치 설정, 앱 출시할때는 컨트롤러+핸드, 해당옵션 못찾음. 없어졌거나 다른곳인듯, 필수아님)
    
    - Add Hand Prefab
        1. OVRCameraRig > TrackingSpace > L/R HandAnchor
        2. OVRHandPrefab를 HandAnchor밑에 추가
        3. RightHand의 OVR Hand, OVR Skeleton, and OVR Mesh에 hand type을 오른손으로 변경
        4. 양쪽 손 프리팹에 OVR Mesh Renderer 체크
    
    여기까지만 빌드는 되는데 손 안나옴