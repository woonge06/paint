# paint
윈도우 환경에서의 프로그래밍은 사용자가 발생시키는 이벤트에 의한 메시지를 처리하는 방식으로 실행된다.

이러한 윈도우 환경에서의 프로그래밍을 메시지 기반 또는 이벤트 기반 프로그래밍이라고 한다.

윈도우 시스템의 모든 애플리케이션은 메시지 또는 이벤트를 기반으로 구동된다.

메시지 기반 프로그래밍은 만약 왼쪽 마우스를 눌렀을 경우 왼쪽 마우스 버튼을 눌렀다는 이벤트에 대해 윈도우 시스템은 해당 애플리케이션에 "WM_LBUTTONDOWN"이라는 메시지를 보낸다.

메시지를 받은 애플리케이션에서는 이런 특정 메시지에 대해 어떠한 일을 수행할 것인가에 대한 처리 루틴을 만들어 주어야 한다.

윈도우 프로그래밍은 애플리케이션에서 사용자가 발생시키는 메시지에 대한 처리 루틴을 만들어 주는 것이다.

애플리케이션 내의 어떤 함수를 윈도우 시스템이 호출한다는 것이며, 이 함수의 인자는 특정 메시지를 의미하는 것으로 각자의 애플리케이션에 있는 이 함수는 윈도우 프로시저라 한다.

윈도우 프로그램은 크게 초기화하는 부분과 메시지를 처리하는 부분으로 나눌 수 있다.

초기화 부분은 WinMain() 함수에서 담당하고 메시지를 처리하는 부분은 WndProc()함수에서 담당한다.

클래스는 윈도우의 종류를 나타내는 것으로 단지 윈도우의 특징 등을 정의하고 등록한 후 윈도우를 생성한다.

WINAPI 형은 윈도우 애플리케이션이라는 의미이고, hInstance는 애플리케이션 프로그램의 ID이다.

IpszCmdLine는 프로그램을 구동할 때 같이 들어오는 매개변수로 실행 파일의 경로 등을 나타내는 문자열 포인터이다.

nCmdShow는 윈도우가 처음 화면에 표시될 때 최대화, 최소화 또는 정상 상태로 보여줄 것인지를 결정해주는 매개변수이다.

WndProc() 함수는 윈도우 시스템에서 들어온 메시지를 switch 문을 이용하여 처리하는 루틴이다.

LRESULT는 결과값을 저장하는 32bit 자료형이다.

CALLBACK 함수는 뒤에서 어떤 메시지에 의해 감추어진 형태로 구동되는 함수라는 의미로 역으로 호출받는 함수이다.

hwnd는 윈도우의 핸들이고, message는 WinMain() 함수에서 보내주는 메시지이다.

wParam와 IParam은 메시지와 함께 필요한 정보가 들어오는 매개변수이다.

도큐먼트란 데이터를 관리하는 기능을 구현한 클래스로, 데이터를 저장하거나 읽어 들입니다, 데이터의 변경 사항이 생기면 뷰의 화면을 갱신합니다.

SDI는 뷰가 1개로, 하나의 문서만 작업이 가능합니다.

MDI는 뷰가 여러개로, 여러개의 문서를 작업이 가능합니다.

메시지 핸들러 함수는 윈도우로부터 애플리케이션에 메시지가 전달될때 해당 메시지를 처리하는 멤버 함수이다.

WM_DRAWITEM(OnDraw)는 그리기 컨트롤이나 메뉴가 변경되었음을 나타냅니다.

WM_ERASEBKGND는 창 배경을 지워야 함을 나타냅니다.

WM_PAINT는 창 프레임을 그려야 함을 나타냅니다. 뷰에는 사용해선 안됩니다.

public은 어디서든 접근이 가능하단 특징이 있습니다.

protected는 상속관계일 때 접근이 가능하다는 특징이 있습니다.

private는 해당 클래스에서만 접근이 가능하단 특징이 있습니다.

afx_msg는 mfc에서 이벤트 핸들러를 오버라이딩(함수 재정의) 할 떄 자동적으로 적히게 되는 것으로, afx_msg 자체는 아무 의미가 없습니다.

afx_msg는 보통 virtual의 의미를 담고 사용하는데, virtual이란 가상함수로, 부모를 상속받은 자식 클래스에서 재정의 할것으로 기대하고 정해놓은 함수를 뜻합니다.

CPaintDC 클래스는 그리기를 위한 클래스이고, CClientDC 클래스는 창의 클라이언트 영역과 연결된 표시 컨텍스트를 관리하는 클래스입니다.

CClinetDC는 윈도우의 클라이언트 영역에 그릴 떄 주로 사용되지만 CPaintDC는 윈도우 프로시저에서 사용된다는 특징이 있습니다.

nullptr이란, 포인터를 표현하는 값 중에서 null을 표현한 값이라고 할 수 있습니다.

포인터 변수를 사용하기 위해서는 0을 사용해도 되지만, nullptr을 사용하는 것이 안전하고, 코드의 가독성을 높여준다는 특징이 있습니다.

사용자는 MFC 프로그램에서 일련의 활동을 하는데 이러한 활동을 이벤트라고 합니다. 즉 이벤트를 통해 사용자는 MFC 프로그램과 상호작용 할 수 있습니다.

이벤트가 발생하면, MFC 프로그램은 이를 메시지로 변환합니다. 예시로 마우스를 움직이면 MFC 프로그램에서는 이벤트가 발생하고, 이 이벤트에 반응하는 WM_MOUSEMOVE라는 메시지가 발생되게 됩니다.

그러한 메시지를 가지고 동작을 하기 위해서 핸들러 함수를 통해 메시지를 처리할 수 있게 됩니다.

메시지 큐란 큐를 채택해서 메세지를 전달하는 시스템입니다.

메시지 큐가 메시지 혹은 이벤트가 송신되고 수신되는 하나의 통신 통로라고 한다면

브로커는 메시지 큐에 메시지 혹은 이벤트를 넣어주고 중개하는 역할을 하는 주체입니다.

프로세스는 실행 중인 프로그램을 의미하며, 독립된 메모리 공간을 가집니다.

스레드는 프로세스 내에서 실행되는 실행 단위로, 프로세스의 자원을 공유하면서 동작합니다.

프로세스는 독립된 메모리 공간에서 실행되지만, 스레드는 프로세스 내에서 메모리를 공유하며 실행된다는 차이가 있습니다.
