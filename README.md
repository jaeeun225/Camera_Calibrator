# 카메라 캘리브레이션

이 프로그램은 OpenCV를 사용하여 체스보드 영상에 대한 카메라 캘리브레이션을 수행합니다. 캘리브레이션을 통해 프로그램은 영상의 왜곡을 보정하여, 정확하고 왜곡되지 않은 영상을 취득합니다.

## 기능

- **카메라 캘리브레이션**: 선택된 이미지를 사용하여 카메라 캘리브레이션을 수행합니다. 각 이미지에서 체스보드의 코너를 검출하고, 이를 이용하여 카메라 매트릭스와 왜곡 계수를 계산합니다.
- **렌즈 왜곡 보정**: 카메라 캘리브레이션에서 얻은 카메라 매트릭스와 왜곡 계수를 사용하여 비디오 파일의 왜곡을 보정합니다.

## 사용 방법

1. 프로젝트 디렉토리에 사용할 비디오 파일을 추가합니다.
2. `camera_calibration.py` 스크립트 내에서 `video_file` 변수를 원하는 비디오 파일명으로 설정합니다.
3. 코드를 실행하면 카메라 캘리브레이션 창이 표시되며 카메라 캘리브레이션이 시작됩니다.
4. 스페이스바를 눌러 영상을 일시 정지할 수 있습니다.
5. 정지된 상태에서 엔터 키를 눌러 캘리브레이션에 사용할 이미지를 추가할 수 있습니다. 선택된 이미지의 수는 영상 상단에 표시됩니다.
6. ESC 키를 누르거나 원본 비디오가 종료될 때까지 재생하면 카메라 캘리브레이션이 종료됩니다.
7. 카메라 캘리브레이션 과정이 완료되면 터미널에 카메라 매트릭스와 왜곡 계수 등의 값이 출력됩니다. 이어서 렌즈 왜곡 보정 창이 표시되고 비디오 파일의 왜곡 보정이 시작됩니다.
8. 스페이스바를 눌러 영상을 일시 정지할 수 있습니다.
9. Tab 키를 눌러 보정 모드와 원본 모드를 토글할 수 있습니다.
10. ESC 키를 누르거나 원본 비디오가 종료될 때까지 재생하면 렌즈 왜곡 보정이 종료됩니다.

## 주의 사항

제대로 된 카메라 캘리브레이션을 위해서는 반드시 1개 이상의 이미지를 선택해야 합니다. 이를 통해 카메라 매트릭스와 왜곡 계수를 올바르게 계산하여 비디오 파일의 왜곡을 보정할 수 있습니다.
