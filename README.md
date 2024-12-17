# 거인 키보드 - Unihertz Titan 용 한글 키보드 패치
[ONEYEAR](https://play.google.com/store/apps/dev?id=7730787383717222740)님이 개발하신 [스트로베리 키보드](https://www.clien.net/service/board/cm_bb/12428757)에 적용할 수 있는 패치 파일입니다. 스트로베리 키보드 1.3.2 버전을 기반으로 합니다.

> [!WARNING]  
> 악의적으로 작성된 코드 및 패치는 없으나 패치를 사용함으로 인해 발생할 수 있는 불이익에 대한 모든 책임은 사용자에 있습니다. 개발자는 이에 대해 책임지지 않습니다.

# APK 패치 및 설치 방법
아래 두 방법 중 하나를 선택하시면 됩니다.

## 1. `Xdelta3` 사용 (컴퓨터 불필요)
1. 스트로베리 키보드 1.3.2 APK 파일을 다운로드 받습니다. ([예시 링크](https://apkpure.com/kr/%EC%8A%A4%ED%8A%B8%EB%A1%9C%EB%B2%A0%EB%A6%AC-%ED%82%A4%EB%B3%B4%EB%93%9C-for-%ED%82%A4%EC%9B%90/com.funanduseful.strawberry/download). 현재 구글 플레이 스토어에서는 다운로드 할 수 없습니다.)
2. 패치 파일을 다운로드 받습니다. ([Xdelta3용 패치 링크](https://github.com/naturale0/Geoin-Keyboard/releases/download/v1.0.0/patch.1.0.0.xdelta3))
3. 폰에 [Unipatcher 앱](https://play.google.com/store/apps/details?id=org.emunix.unipatcher&hl=en_US)을 설치합니다.
4. 1, 2에서 다운받은 APK와 패치파일을 폰으로 옮깁니다.
5. Unipatcher를 실행 후 아래를 차례대로 따라합니다.
   1. "Patch file"을 터치 후 2에서 다운받은 패치 파일을 선택합니다.
   2. "ROM file"을 터치 후 1에서 다운받은 원본 APK를 선택합니다.
   3. "Output file"을 터치 후 패치된 APK의 이름 및 저장할 폴더를 지정합니다.
6. 우측 하단 저장 아이콘을 클릭하면 패치된 APK가 저장됩니다.
7. 패치된 APK를 실행하여 설치합니다.
   1. Google Play Protect 경고가 뜨면 "More detail" (자세히)을 누른 뒤 "Install without scanning" (스캔하지 않고 설치)를 눌러줍니다.

## 2. `bsdiff` 사용 (컴퓨터 필요)
1. 스트로베리 키보드 1.3.2 APK 파일을 다운로드 받습니다. ([예시 링크](https://apkpure.com/kr/%EC%8A%A4%ED%8A%B8%EB%A1%9C%EB%B2%A0%EB%A6%AC-%ED%82%A4%EB%B3%B4%EB%93%9C-for-%ED%82%A4%EC%9B%90/com.funanduseful.strawberry/download))
2. 패치 파일을 다운로드 받습니다. ([bsdiff용 패치 링크](https://github.com/naturale0/Geoin-Keyboard/releases/download/v1.0.0/patch.1.0.0))
3. `bsdiff`를 사용하여 APK 파일을 패치합니다. (bsdiff 다운로드: [Windows](https://www.romhacking.net/utilities/929/), [MacOS](https://formulae.brew.sh/formula/bsdiff))
   ```
   bspatch "패치 전 앱.apk" "Geoin-kb-patched.apk" patch.1.0.0
   ```
   -> `패치 전 앱.apk`에 패치 1.0.0 버전을 적용하여 `Geoin-kb-patched.apk`를 만듭니다.
4. 패치된 `Geoin-kb-patched.apk`를 스마트폰에 설치합니다.

# 수정/추가된 기능
- 블랙베리 키원에 맞춰져있던 기호 키 배열을 유니허츠 타이탄 시리즈에 맞추어 재배열했습니다.
- `ALT+SHIFT` 를 눌렀을 때 한국어에서 자주 사용하는 기호를 바로 입력할 수 있습니다. 예시: `ALT+SHIFT+W`를 누르면 물결표(`~`)를 작성합니다.
    - `ALT+SHIFT`+`QWERTYUIOP` -> ``~[]{}-_+=`
- `SYM` 키를 커스텀 키로 사용할 수 있습니다. 설정에서 선택할 수 있습니다.
- `Fn` 키를 누르면 한/영 전환됩니다. 이를 위해서 스마트폰 설정 intelligent assistance > shortcut settings에서 `Fn`키가 `Magic key`로 설정되어있어야 합니다.
- 키를 길게 누르면 해당되는 특수문자가 입력됩니다. 예시: `W`를 길게 누르면 `1`이 입력됩니다.

# To do
- [ ] ~~글자 지울 때 자모 흩어지지 않게 하기 (현재는 모음을 지워도 자음이 다시 합쳐지지 않음. ex. `한그루` > `한그ㄹ`)~~
    - 구현 어려울 듯. 길게 누르면 특수문자 입력하도록 구현한 방법과 비슷하게 하면 가능할지도.
- [ ] 스페이스 연속으로 두 번 입력하면 자동 마침표 찍기.
