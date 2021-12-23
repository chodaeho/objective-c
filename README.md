# 1. objective-c
### Header(.h) 파일
 #### 1) 메서드나 변수
    - header파일에서 메서드나 변수(상수)를 선언
    - 변수 초기화 불가능. nil 혹은 0으로 자동 초기화 됨
 #### 2) #import
    - C언어에서 #include에 해당, swift에서 import에 해당
    - 외부 라이브러리, 프레임워크, 프로젝트 내에 선언된 클래스를 불러올 때 import 사용
 #### 3) @interface, @end
    - 외부에서 사용 할 메서드 이름, 인스턴스 변수, property 선언
    - @interface 클래스 선언의 시작, 어떤 클래스를 상속받는지, 어떤 변수와 메서드를 사용 할 건지 선언
    - @end 클래스 선언의 끝 맺음. @interface 에서 @end 까지가 interface field 선언부 해당
    - @interface 대괄호 안에 선언되는 변수는 인스턴스 변수(instance variable)
    - 변수는 “NSString *name;” 으로 선언
    - 인스턴스 변수(instance variable) 접근 지시자는 @property
    - @property는 자동으로 getter, setter를 생성해주기 때문에 별도의 작업없이 외부에서 접근 가능
    - 메서드는 “- (void)메서드명;” 으로 선언
### Implementation(.m) 파일
 #### 1) #import
    - .h 파일이 있다면 자신의 header파일을 import 해야함.
    - .h 파일에서 import 되어 있는것을 ,m에서 다시 import 안해도 됨.
 #### 2) @interface, @end
    - 프로퍼티나 인스턴스 변수를 private로 선언하고 싶을 때 @interface ~ @end 안에 선언
 #### 3) @implementation, @end
    - 메서드 구현 ex) “- (void) viewDidLoad { [super viewDidLoad]; }”
    - @implementation 에서 @end 까지가 implementation field 구현부에 해당
 #### 4) @synthesize
    - 선언부에 선언된 이름 그대로 접근 가능하도록 처리

# 2. keyword 설명
    - alloc : allocate, 객체르 메모리에 할당
    - init() : 초기화
    - typedef : 데이터 형에 다르 이름을 부여하느 기능 ex) typedef int Counter; Counter형을 변수로 선언하여 사용 가능
