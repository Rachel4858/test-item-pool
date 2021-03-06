## 실습 진행 방법 및 제출 방법
* 실습은 java 언어 기반의 웹 프레임워크를 활용해 다음 문제를 해결해야 한다.
* MVC 패턴 기반으로 개발해야 한다.
* 실습 결과물은 [GitHub](https://github.com)를 통해 공유한다.

## 볼링게임 점수판
볼링 점수를 계산하는 프로그램을 구현한다.

* 볼링 게임의 점수 계산 방식 아는 사람은 바로 구현을 시작한다.
* 점수 계산 방식을 모르는 사람은 구글에서 "볼링 점수 계산법"과 같은 키워드로 검색해 볼링 게임의 점수 계산 방식을 학습한 후 구현을 시작한다.

#### 요구사항
* 1명 이상 사용자의 볼링 게임 점수를 관리할 수 있는 프로그램을 구현한다.
* 콘솔 화면에서 볼링 게임 실행 결과는 다음과 같다. **콘솔 화면의 UI를 웹 UI 기반으로 동작하도록 구현해야 한다.**
* 사용자가 잘못된 값을 입력했을 때는 에러 메시지를 사용자에게 보여줘야 한다.

```
How many people? 2
플레이어 1의 이름은?(3 english letters): PJS
플레이어 2의 이름은?(3 english letters): KYJ
| NAME |  01  |  02  |  03  |  04  |  05  |  06  |  07  |  08  |  09  |  10  |
|  PJS |      |      |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |
|  KYJ |      |      |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |

PJS's turn : 10
| NAME |  01  |  02  |  03  |  04  |  05  |  06  |  07  |  08  |  09  |  10  |
|  PJS |  X   |      |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |
|  KYJ |      |      |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |

KYJ's turn : 8
| NAME |  01  |  02  |  03  |  04  |  05  |  06  |  07  |  08  |  09  |  10  |
|  PJS |  X   |      |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |
|  KYJ |  8   |      |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |

KYJ's turn : 2
| NAME |  01  |  02  |  03  |  04  |  05  |  06  |  07  |  08  |  09  |  10  |
|  PJS |  X   |      |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |
|  KYJ |  8|/ |      |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |

PJS's turn : 8
| NAME |  01  |  02  |  03  |  04  |  05  |  06  |  07  |  08  |  09  |  10  |
|  PJS |  X   |  8   |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |
|  KYJ |  8|/ |      |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |

PJS's turn : 2
| NAME |  01  |  02  |  03  |  04  |  05  |  06  |  07  |  08  |  09  |  10  |
|  PJS |  X   |  8|/ |      |      |      |      |      |      |      |      |
|      |  20  |      |      |      |      |      |      |      |      |      |
|  KYJ |  8|/ |      |      |      |      |      |      |      |      |      |
|      |      |      |      |      |      |      |      |      |      |      |

KYJ's turn : 10
| NAME |  01  |  02  |  03  |  04  |  05  |  06  |  07  |  08  |  09  |  10  |
|  PJS |  X   |  8|/ |      |      |      |      |      |      |      |      |
|      |  20  |      |      |      |      |      |      |      |      |      |
|  KYJ |  8|/ |  X   |      |      |      |      |      |      |      |      |
|      |  20  |      |      |      |      |      |      |      |      |      |

PJS's turn : 

...
```

#### 프로그래밍 제약 사항
* 객체 지향 설계 기반 개발이 가능하도록 구현한다.
* 상속을 사용해 구현해야 한다. 예를 들어 1 ~ 9 프레임과 10 프레임의 동작 방식이 다른데 이 부분을 상속을 통해 해결해 본다.
* 배열 대신 java의 collection(List, Map 등)을 사용해 구현해야 한다.
* 모든 소스 코드는 junit 기반의 단위 테스트가 존재해야 한다.(controller 코드는 제외)
* indent(인덴트, 들여쓰기) depth를 2단계에서 1단계로 줄여라.
  * depth의 경우 if문을 사용하는 경우 1단계의 depth가 증가한다. if문 안에 while문을 사용한다면 depth가 2단계가 된다.
* else를 사용하지 마라.
* 메소드의 크기가 최대 10라인을 넘지 않도록 구현한다.
  * method가 한 가지 일만 하도록 최대한 작게 만들어라.
