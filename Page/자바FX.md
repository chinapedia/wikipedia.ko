> This article is converted from Wikipedia: [자바FX](https://ko.wikipedia.org/wiki/자바FX).


**자바FX**(JavaFX)는 [데스크톱 애플리케이션과](../Page/응용_소프트웨어.md "wikilink") [리치 인터넷 애플리케이션](../Page/리치_인터넷_애플리케이션.md "wikilink")(RIA)을 개발하고 배포하는 [소프트웨어 플랫폼으로](https://ko.wikipedia.org/wiki/소프트웨어_플랫폼 "wikilink"), 다양한 장치에서 실행 가능하다. 자바FX는 [자바 SE를](https://ko.wikipedia.org/wiki/자바_SE "wikilink") 위한 표준 [GUI](../Page/그래픽_사용자_인터페이스.md "wikilink") 라이브러리로서 [스윙을](../Page/스윙_\(자바\).md "wikilink") 대체하기 위해 고안되었다.\[1\] 자바FX는 [마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink")의 [데스크톱 컴퓨터와](../Page/데스크톱_컴퓨터.md "wikilink") [웹 브라우저를](../Page/웹_브라우저.md "wikilink") 지원한다.

## 자바FX 애플리케이션 예제

### 예제 코드

다음은 단순한 자바FX 기반 프로그램을 나타낸 것이다. 버튼이 포함된 창(stage)을 표시한다. [섬네일](https://ko.wikipedia.org/wiki/파일:Hello_world_in_javafx.png "wikilink")

``` java
package javafxtuts;

import javafx.application.Application;
import javafx.event.ActionEvent;
import javafx.event.EventHandler;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.layout.StackPane;
import javafx.stage.Stage;

public class Javafxtuts extends Application {

    @Override
    public void start(Stage primaryStage) {
        // Creating the java button
        Button btn = new Button();
        // Setting text to button
        btn.setText("Hello World");
        //registering a handler for button
        btn.setOnAction((ActionEvent event) -> {
            // printing Hello World! to the console
            System.out.println("Hello World!");
        });
        // Initializing the StackPane class
        StackPane root = new StackPane();
        // Adding all the nodes to the FlowPane
        root.getChildren().add(btn);
        //Creating a scene object
        Scene scene = new Scene(root, 300, 250);
        //Adding the title to the window (primaryStage)
        primaryStage.setTitle("Hello World!");
        primaryStage.setScene(scene);
        // show the window(primaryStage)
        primaryStage.show();
    }

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        launch(args);
    }

}
```

## 각주

## 외부 링크

  -
  - [OpenJFX website](http://openjdk.java.net/projects/openjfx/)

[분류:자바 (프로그래밍 언어)](https://ko.wikipedia.org/wiki/분류:자바_\(프로그래밍_언어\) "wikilink") [분류:오라클 소프트웨어](https://ko.wikipedia.org/wiki/분류:오라클_소프트웨어 "wikilink")

1.