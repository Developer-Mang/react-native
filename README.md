# Study React-native

## Window 환경에서 React-native 개발 환경 설정하기
**1. 프로그램 실행에 필요한 패키지 툴과 프로그램 설치하기**
- Chocolatey 
- Node
- Python
- React-Native-CLI
- JDK (JAVA DEVELOPE KIT)
- Android studio

```bash
  # Chocolatey
  @"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"$ npm run android

  # Node
  choco install -y nodejs.install

  # Python
  choco install -y python2

  # React-Native-CLI
  npm install -g react-native-cli

  # JDK
  choco install -y jdk8
```

*Android studio 다운로드 링크 : [https://developer.android.com/studio](https://developer.android.com/studio)*

**2. Android Studio 설정하기**
1. 우측 하단에 Configure 클릭
2. SDK Manger 클릭 
3. 우측하단에 show package Details 체크
4. 아래 리스트를 찾아 체크 후 다운로드
    - Android SDK Platform 28
    - Intel x86 Atom System Image
    - Google APIs Intel x86 Atom System Image
    - Google APIs Intel x86 Atom_64 System Image

**3. OS에 환경 변수 설정하기**
1. 내 PC 우측 클릭 > 속성 클릭
2. 고급 시스템 설정 클릭
3. 환경 변수 버튼 클릭
4. 상단에 있는 사용자 변수에 있는 '새로만들기' 버튼 클릭
5. ANDROID_HOME 이란 이름으로 변수 생성하고 값을 Android Studio 에서 설치했던 SDK 폴더 위치로 설정
    *위치를 찾기 힘들면, 위 Android Studio 설정하기에 SDK Manger 항목에 위치가 있음*
6. 사용자 변수 목록 중에 'Path'를 찾아 선택 후 변경 버튼 클릭
7. Android Studio 에서 설치했던 SDK 폴더 위치에 있는 platform-tools 경로를 찾아 그 경로로 설정

**4. react-native 프로젝트 생성 후 실행**

```bash
  # 오류를 막기 위한 버전 고정
  $ npm config set save-exact=true
  # 프로젝트 생성
  $ react-native init ProjectName

  $ cd ProjectName
  # 프로젝트 실행
  $ npm run android
```

## Mac 환경에서 React-native 개발 환경 설정하기
**1. 프로그램 실행에 필요한 패키지 툴과 프로그램 설치하기**
- Homebrew 
- node
- Watchman
- Xcode
- Cocoapods
- React-Native-CLI
- JDK (JAVA DEVELOPE KIT)
- Android studio

```bash
  # Homebrew 
  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

  # Node
  brew install node

  # Watchman
  brew install watchman

  # React-Native-CLI
  npm install -g react-native-cli

  # Cocoapods
  sudo gem install cocoapods

  # JDK
  brew tap AdoptOpenJDK/openjdk
  brew cask install adoptopenjdk8
```
*Xcode 다운로드 링크 : [https://apps.apple.com/us/app/xcode/id497799835?mt=12](https://apps.apple.com/us/app/xcode/id497799835?mt=12)*

*Android studio 다운로드 링크 : [https://developer.android.com/studio](https://developer.android.com/studio)*

**2. Android Studio 설정하기**
1. 우측 하단에 Configure 클릭
2. SDK Manger 클릭 
3. 우측하단에 show package Details 체크
4. 아래 리스트를 찾아 체크 후 다운로드
    - Android SDK Platform 28
    - Intel x86 Atom System Image
    - Google APIs Intel x86 Atom System Image
    - Google APIs Intel x86 Atom_64 System Image

**3. Android studio 환경 변수 설정하기**
1. 에디터에서 **~/.bash_profile** 또는 **~/.zshrc** 파일을 연다.
2. 아래 코드를 추가한다.

```
  # export ANDROID_HOME=$HOME/Library/Android/sdk
  export ANDROID_HOME=자신의 안드로이드SDK 위치/Android/sdk
  export PATH=$PATH:$ANDROID_HOME/emulator
  export PATH=$PATH:$ANDROID_HOME/tools
  export PATH=$PATH:$ANDROID_HOME/tools/bin
  export PATH=$PATH:$ANDROID_HOME/platform-tools
```

**4. react-native 프로젝트 생성 후 실행**

```bash
  # 오류를 막기 위한 버전 고정
  $ npm config set save-exact=true
  # 프로젝트 생성
  $ react-native init ProjectName

  $ cd ProjectName
  # 프로젝트 실행
  $ npm run android
```

## How to start React-native for window
**1. Install some tools and programs**
- Chocolatey 
- Node
- Python
- React-Native-CLI
- JDK (JAVA DEVELOPE KIT)
- Android studio

```bash
  # Chocolatey
  @"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"$ npm run android

  # Node
  choco install -y nodejs.install

  # Python
  choco install -y python2

  # React-Native-CLI
  npm install -g react-native-cli

  # JDK
  choco install -y jdk8
```

*Android studio DownLoad Link : [https://developer.android.com/studio](https://developer.android.com/studio)*

**2. Setting android studio**
1. Go Configure 
2. Click SDK Manger 
3. Check show package Details 
4. Find Lists below and Check them
    - Android SDK Platform 28
    - Intel x86 Atom System Image
    - Google APIs Intel x86 Atom System Image
    - Google APIs Intel x86 Atom_64 System Image

**3. Setting Environment Variable**
1. Go Advanced System setting 
2. Open Advanced Tap 
3. Click 'Environment Variable' button 
4. Click 'New' button below User Variables
5. Make Variable name 'ANDROID_HOME' to set value android sdk loaction
    *if you can't find location, you can find using android studio SDK manger belong Configure*
6. Edit Path in User variables > Create platform-tools location below sdk location

**4. Conect Cell phone using USB or run amulator**

```bash
  $ npm run android
```

## How to start React-native for Mac
**1. Install some tools and programs**
- Homebrew 
- node
- Watchman
- Xcode
- Cocoapods
- React-Native-CLI
- JDK (JAVA DEVELOPE KIT)
- Android studio

```bash
  # Homebrew 
  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

  # Node
  brew install node

  # Watchman
  brew install watchman

  # React-Native-CLI
  npm install -g react-native-cli

  # Cocoapods
  sudo gem install cocoapods

  # JDK
  brew tap AdoptOpenJDK/openjdk
  brew cask install adoptopenjdk8
```
*Xcode DownLoad Link : [https://apps.apple.com/us/app/xcode/id497799835?mt=12](https://apps.apple.com/us/app/xcode/id497799835?mt=12)*

*Android studio DownLoad Link : [https://developer.android.com/studio](https://developer.android.com/studio)*

**2. Setting android studio**
1. Go Configure 
2. Click SDK Manger 
3. Check show package Details 
4. Find Lists below and Check them
    - Android SDK Platform 28
    - Intel x86 Atom System Image
    - Google APIs Intel x86 Atom System Image
    - Google APIs Intel x86 Atom_64 System Image

**3. Setting Environment Variable to android studio**
1. Find and Open **~/.bash_profile** or **~/.zshrc** file
2. Add this code

```
  # export ANDROID_HOME=$HOME/Library/Android/sdk
  export ANDROID_HOME=자신의 안드로이드SDK 위치/Android/sdk
  export PATH=$PATH:$ANDROID_HOME/emulator
  export PATH=$PATH:$ANDROID_HOME/tools
  export PATH=$PATH:$ANDROID_HOME/tools/bin
  export PATH=$PATH:$ANDROID_HOME/platform-tools
```

**4. Conect Cell phone using USB or run amulator**
```bash
  $ npm run android
```
