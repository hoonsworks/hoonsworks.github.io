# gulp

- 아래 내용은 macOS 사용자 기준으로 작성되었습니다.

### NVM (Node Version Manager)

- Node.js를 설치하고 관리하기 위한 셀 스크립트로 다양한 Node.js 버전을 사용하기에 적합합니다.

### brew 설치

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### 1. 기존 노드 버전 제거

```bash
brew uninstall --ignore-dependencies node
brew uninstall --force node
```

### 2. NVM 설치

```bash
brew update
brew install nvm
```

#### 3. 홈 디렉터로에 nvm 폴더 생성

```bash
mkdir ~/.nvm
```

#### 4. 환경변수 설정

```bash
vi ~/.bash_profile

// or

vim ~/.bash_profile
```

#### 5. .bash_profile에 아래 내용 입력

```bash
export NVM_DIR=~/.nvm
source $(brew --prefix nvm)/nvm.sh
```

- 내용 입력 후 ECS -> :wq! 저장하여 종료

#### 6. 환경변수 적용

```bash
source ~/.bash_profile
```

#### 7. nvm 설치 확인

```bash
nvm ls-remote
```

- node 버전들이 표시되면 설치 완료

#### 8. node 설치

```bash
nvm install node  // LTS 버전 설치
nvm install 14
nvm install 14.21.3
```

- 원하는 Node 버전 또는 LTS 버전을 설치

#### 9. node 선택

```bash
nvm use node
nvm use 14
```
