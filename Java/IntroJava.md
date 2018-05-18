##  Java

고급언어, 객체지향 언어의 대명사 인 것 같다.
프로그램이라는 것이 원래 사람이 읽기 쉽도록 만들어진 언어 인지라 
컴퓨터가 알 수 있도록 기계어로 변환을 해주어야 하는데, 이 변환 과정을 컴파일 이라고 한다.
자바의 소스 파일은 *.java 라는 확장자를 가지고 
컴파일이 된 소스 파일은 *.class 라는 확장자를 갖는다.

특히 CPU와 운영체제의 영향을 받지 않고 자바 가상 기계(JVM)만 있으면
어떤 컴퓨터에서든 실행이 가능한 독립성을 갖는다.

흔히 말하는 JDK는 자바 컴파일러, 자바 응용프로그램을 개발하는데 필요한 도구 이며,
자바 응용이 실행 될 때 필요한 자바 가상 기계(JVM)와 표준 클래스 파일을 포함하는 JRE로 구성된다.


-----

1. 프로그래밍 기초


	```
	# 1. 클래스 이름과 자바의 소스 파일 이름이 일치 해야 한다.
	# 2. 자바 소스 파일 확장자는 *.java이며, 파일 명의 대소문자를 구분한다.
	# 3. 소스 파일 작성 후 컴파일러(javac)는 컴파일 된 바이트 코드를 *.class 파일에 저장한다.
	# 4. 자바 프로그램의 실행은 Consol환경에서 확장자를 뺀 이름으로 실행 한다.
	     ex) $ javac HelloJB.java -> $ java HelloJB
	```

-----

2. 기본 구조


	```
	public class HelloJB {

		public static int sum(int a, int b){
			return a+b;
		}
    	public static void main(String[] args) {
    		int n = 20;
    		int hap; 

    		hap = sum(n, 30);

        	System.out.println("Hello JB!!");
        	System.out.println(hap);
    	}
	}
	```

-----