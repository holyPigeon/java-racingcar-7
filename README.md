# java-racingcar-precourse

<div class="Container_box__GEbZX"><div class="MissionView_mission-viewer-body__OXsxc markdown-body"><h2>목표</h2><h3>학습 목표</h3><ul><li>여러 역할을 수행하는 큰 함수를 단일 역할을 수행하는 작은 함수로 분리한다.</li><li>테스트 도구를 사용하는 방법을 배우고 프로그램이 제대로 작동하는지 테스트한다.</li><li><a href="https://docs.google.com/document/d/1MdiqBV5nhSfFB96-p5LlKrGM8uLopXslh1vEzwxR9Bo/edit?usp=sharing">1주 차 공통 피드백</a>을 최대한 반영한다.</li></ul><h3>회고</h3><p>아래 질문에 대한 중간 회고를 진행하고 소감에 구체적인 결과를 작성한다. 소감은 텍스트로 작성해야 하며 외부 링크는 허용하지 않는다.</p><ul><li>지원서에 작성한 목표를 얼마나 달성하고 있다고 생각하나요? 그 이유는 무엇인가요?</li><li>지원서에 작성한 목표를 변경해야 한다고 생각하시나요? 그렇다면 그 이유와 어떤 목표로 변경하고 싶으신가요?</li><li>프리코스를 진행하면서 눈에 띄는 변화나 깨달은 점이 있나요?</li></ul><hr><h2>프리코스 진행 방식</h2><h3>진행 방식</h3><ul><li>미션은 <strong>과제 진행 요구 사항</strong>, <strong>기능 요구 사항</strong>, <strong>프로그래밍 요구 사항</strong> 세 가지로 구성되어 있다.</li><li>세 개의 요구 사항을 만족하기 위해 노력한다. 특히 기능을 구현하기 전에 기능 목록을 만들고, 기능 단위로 커밋 하는 방식으로 진행한다.</li><li><strong>기능 요구 사항에 기재되지 않은 내용은 스스로 판단하여 구현한다.</strong></li><li>매주 진행할 미션은 화요일 오후 3시부터 확인할 수 있으며, 다음 주 월요일까지 구현을 완료하여 제출해야 한다. <strong>제출은 일요일 오후 3시부터 가능하다.</strong><ul><li><strong>정해진 시간을 지키지 않을 경우 미션을 제출하지 않은 것으로 간주한다.</strong></li><li>종료 일시 이후에는 추가 푸시를 허용하지 않는다.</li></ul></li></ul><h3>미션 제출 방법</h3><ul><li>미션 구현을 완료한 후 GitHub을 통해 제출해야 한다.<ul><li>GitHub을 활용한 제출 방법은 <a href="https://github.com/woowacourse/woowacourse-docs/tree/master/precourse">프리코스 과제 제출</a> 문서를 참고해 제출한다.</li></ul></li><li>GitHub에 미션을 제출한 후 <a href="https://apply.techcourse.co.kr">우아한테크코스 지원 플랫폼</a>에 PR 링크를 포함하여 최종 제출한다.<ul><li>자세한 안내는 <a href="https://github.com/woowacourse/woowacourse-docs/tree/master/precourse#%EC%A0%9C%EC%B6%9C-%EA%B0%80%EC%9D%B4%EB%93%9C">제출 가이드</a>를 참고한다.</li><li>과제를 수행하면서 느낀 점, 배운 점, 많은 시간을 투자한 부분 등 자유롭게 작성한다.</li></ul></li></ul><h3>과제 제출 전 체크 리스트</h3><ul><li>기능을 올바르게 구현했더라도 <strong>요구 사항에 명시된 출력 형식을 따르지 않으면 0점</strong>을 받게 된다.</li><li>기능 구현을 완료한 후 아래 가이드에 따라 모든 테스트가 성공적으로 실행되는지 확인한다.</li><li><strong>테스트가 실패하면 점수가 0점</strong>이 되므로 제출하기 전에 반드시 확인한다.</li></ul><h4>테스트 실행 가이드</h4><ul><li>터미널에서 <code>java -version</code>을 실행하여 Java 버전이 21인지 확인한다. Eclipse 또는 IntelliJ IDEA와 같은 IDE에서 Java 21로 실행되는지 확인한다.</li><li>터미널에서 Mac 또는 Linux 사용자의 경우 <code>./gradlew clean test</code> 명령을 실행하고, Windows 사용자의 경우 <code>gradlew.bat clean test</code> 또는 <code>.\gradlew.bat clean test</code> 명령을 실행할 때 모든 테스트가 아래와 같이 통과하는지 확인한다.</li></ul><pre><code data-highlighted="yes" class="hljs language-apache"><span class="hljs-attribute">BUILD</span> SUCCESSFUL in <span class="hljs-number">0</span>s
</code></pre><hr><h1>자동차 경주</h1><h2>과제 진행 요구 사항</h2><ul><li>미션은 <a href="https://github.com/woowacourse-precourse/java-racingcar-7">자동차 경주</a> 저장소를 포크하고 클론하는 것으로 시작한다.</li><li><strong>기능을 구현하기 전 <code>README.md</code>에 구현할 기능 목록을 정리</strong>해 추가한다.</li><li>Git의 커밋 단위는 앞 단계에서 <code>README.md</code>에 정리한 기능 목록 단위로 추가한다.<ul><li><a href="https://gist.github.com/stephenparish/9941e89d80e2bc58a153">AngularJS Git Commit Message Conventions</a>을 참고해 커밋 메시지를 작성한다.</li></ul></li><li>자세한 과제 진행 방법은 프리코스 진행 가이드 문서를 참고한다.</li></ul><h2>기능 요구 사항</h2><p>초간단 자동차 경주 게임을 구현한다.</p><ul><li>주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.</li><li>각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.</li><li>자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.</li><li>사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.</li><li>전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.</li><li>자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.</li><li>우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.</li><li>사용자가 잘못된 값을 입력할 경우 <code>IllegalArgumentException</code>을 발생시킨 후 애플리케이션은 종료되어야 한다.</li></ul><h3>입출력 요구 사항</h3><h4>입력</h4><ul><li>경주할 자동차 이름(이름은 쉼표(,) 기준으로 구분)</li></ul><pre><code data-highlighted="yes" class="hljs language-autohotkey"><span class="hljs-built_in">pobi,</span>woni,jun
</code></pre><ul><li>시도할 횟수</li></ul><pre><code data-highlighted="yes" class="hljs language-undefined">5
</code></pre><h4>출력</h4><ul><li>차수별 실행 결과</li></ul><pre><code data-highlighted="yes" class="hljs language-ada">pobi : --
woni : ----
jun : ---
</code></pre><ul><li>단독 우승자 안내 문구</li></ul><pre><code data-highlighted="yes" class="hljs language-ada">최종 우승자 : <span class="hljs-type">pobi</span>
</code></pre><ul><li>공동 우승자 안내 문구</li></ul><pre><code data-highlighted="yes" class="hljs language-ada">최종 우승자 : <span class="hljs-type">pobi</span>, jun
</code></pre><h4>실행 결과 예시</h4><pre><code data-highlighted="yes" class="hljs language-ada">경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
pobi,woni,jun
시도할 횟수는 몇 회인가요?
<span class="hljs-number">5</span>

실행 결과
pobi : -
woni : 
<span class="hljs-type">jun</span> : -

pobi : --
woni : -
jun : --

pobi : ---
woni : --
jun : ---

pobi : ----
woni : ---
jun : ----

pobi : -----
woni : ----
jun : -----

최종 우승자 : <span class="hljs-type">pobi</span>, jun
</code></pre><h2>프로그래밍 요구 사항 1</h2><ul><li>JDK 21 버전에서 실행 가능해야 한다.</li><li>프로그램 실행의 시작점은 <code>Application</code>의 <code>main()</code>이다.</li><li><code>build.gradle</code> 파일은 변경할 수 없으며, <strong>제공된 라이브러리 이외의 외부 라이브러리는 사용하지 않는다.</strong></li><li>프로그램 종료 시 <code>System.exit()</code>를 호출하지 않는다.</li><li>프로그래밍 요구 사항에서 달리 명시하지 않는 한 파일, 패키지 등의 이름을 바꾸거나 이동하지 않는다.</li><li>자바 코드 컨벤션을 지키면서 프로그래밍한다.<ul><li>기본적으로 <a href="https://github.com/woowacourse/woowacourse-docs/blob/main/styleguide/java">Java Style Guide</a>를 원칙으로 한다.</li></ul></li></ul><h2>프로그래밍 요구 사항 2</h2><ul><li>indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다.<ul><li>예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.</li><li>힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메서드)를 분리하면 된다.</li></ul></li><li>3항 연산자를 쓰지 않는다.</li><li>함수(또는 메서드)가 한 가지 일만 하도록 최대한 작게 만들어라.</li><li>JUnit 5와 AssertJ를 이용하여 정리한 기능 목록이 정상적으로 작동하는지 테스트 코드로 확인한다.<ul><li>테스트 도구 사용법이 익숙하지 않다면 아래 문서를 참고하여 학습한 후 테스트를 구현한다.<ul><li><a href="https://junit.org/junit5/docs/current/user-guide">JUnit 5 User Guide</a></li><li><a href="https://assertj.github.io/doc">AssertJ User Guide</a></li><li><a href="https://www.baeldung.com/assertj-exception-assertion">AssertJ Exception Assertions</a></li><li><a href="https://www.baeldung.com/parameterized-tests-junit-5">Guide to JUnit 5 Parameterized Tests</a></li></ul></li></ul></li></ul><h3>라이브러리</h3><ul><li><code>camp.nextstep.edu.missionutils</code>에서 제공하는 <code>Randoms</code> 및 <code>Console</code> API를 사용하여 구현해야 한다.<ul><li>Random 값 추출은 <code>camp.nextstep.edu.missionutils.Randoms</code>의 <code>pickNumberInRange()</code>를 활용한다.</li><li>사용자가 입력하는 값은 <code>camp.nextstep.edu.missionutils.Console</code>의 <code>readLine()</code>을 활용한다.</li></ul></li></ul><h4>사용 예시</h4><ul><li>0에서 9까지의 정수 중 한 개의 정수 반환</li></ul><pre><code class="language-java hljs" data-highlighted="yes">Randoms.pickNumberInRange(<span class="hljs-number">0</span>, <span class="hljs-number">9</span>);
</code></pre></div></div>
