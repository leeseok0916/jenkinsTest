node {
  def hello = 'hello jenkins'
	// 스테이지 선언
  stage ('clone') {
		// git clone
		git 'https://github.com/leeseok0916/jenkinsTest.git'
  }

	// clone 받은 프로젝트 안의 src 디렉토리에서 stage 실행
	dir ('src') {
		stage ('src/index.js execute') {
		    echo "index 파일  실행"
		}
	}

	stage ('print') {
		print(hello) // 함수 + 변수 사용
	}
}

// 함수 선언 - 반환 타입이 없기때문에 void로 선언, def로 선언하면 됨???
void print(message) {
	echo "${message}"
}