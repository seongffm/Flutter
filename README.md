# 📱 Dart & Flutter 학습 내용 정리


![dart 언어 로드맵](https://github.com/user-attachments/assets/83248914-fa9d-4e46-89e1-e555d872a978)

이 레포지토리는 Dart 언어와 Flutter 프레임워크를 활용한 모바일 애플리케이션 개발 학습 내용을 정리한 것입니다. 기초부터 고급 개념까지 다양한 주제를 다루어, 효과적인 앱 개발을 위한 핵심 기술을 익혔습니다.

## 📘 주요 학습 내용

### 1. 📚 Dart 언어 기초
- Dart 언어의 기본 문법과 구조를 학습했습니다.
- 데이터 타입, 변수, 조건문, 반복문 등의 기초 개념을 익혔습니다.
```dart
void main() {
  var name = 'Dart';
  print('Hello, $name!');
}
```
### 2. 🛠️ Dart 고급 기능
- 함수, 클래스 및 비동기 프로그래밍을 포함한 고급 개념을 배웠습니다.
- 비동기 처리 방법을 익혔습니다.
```dart
Future<void> fetchData() async {
  await Future.delayed(Duration(seconds: 2));
  print('Data fetched!');
}
```
### 3. 📱 Flutter 소개
- Flutter 프레임워크의 개념과 장점을 학습했습니다.
- Flutter의 위젯 시스템과 기본 구조를 이해했습니다.

### 4. 🎨 Flutter UI 구성
- Flutter를 사용하여 다양한 UI 구성 요소를 만드는 방법을 익혔습니다.
- **StatelessWidget**과 **StatefulWidget**의 차이를 학습했습니다.
```dart
class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text('My Home Page')),
      body: Center(child: Text('Hello, Flutter!')),
    );
  }
}
```
### 5. 🌐 Flutter 네비게이션
- Flutter에서 페이지 간의 네비게이션 구현 방법을 학습했습니다.
- **Navigator**와 **Routes**를 활용한 페이지 전환을 익혔습니다.
```dart
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => SecondPage()),
);
```
### 6. 📡 API 통신
- Flutter에서 HTTP 패키지를 사용하여 RESTful API와 통신하는 방법을 배웠습니다.
```dart
import 'package:http/http.dart' as http;

Future<void> fetchData() async {
  final response = await http.get(Uri.parse('https://api.example.com/data'));
  if (response.statusCode == 200) {
    print('Data: ${response.body}');
  } else {
    print('Request failed with status: ${response.statusCode}.');
  }
}
```
### 7. 🔍 상태 관리
- Flutter에서 상태 관리를 위한 다양한 방법(Provider, Riverpod 등)을 학습했습니다.

### 8. 🎉 Flutter 패키지 활용
- Flutter에서 유용한 외부 패키지를 찾아보고 적용하는 방법을 배웠습니다.

### 9. 📦 로컬 환경 배포
- Flutter 애플리케이션을 로컬 환경에서 실제 스마트폰에 설치하여 테스트하는 방법을 익혔습니다. 이 과정에서는 다음 단계를 따릅니다:
  1. **USB 디버깅 활성화**: 스마트폰의 개발자 옵션에서 USB 디버깅을 활성화합니다.
  2. **장치 연결**: USB 케이블을 사용하여 스마트폰을 컴퓨터에 연결합니다.
  3. **Flutter 프로젝트 실행**:
     - 터미널에서 해당 Flutter 프로젝트 디렉토리로 이동합니다.
     - 다음 명령어를 사용하여 앱을 스마트폰에 설치하고 실행합니다:
       ```bash
       flutter run
       ```
- 이 명령어를 통해 앱이 빌드되고 연결된 스마트폰에 설치되어 실행됩니다.
