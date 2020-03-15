> This article is converted from Wikipedia: [Gson](https://ko.wikipedia.org/wiki/Gson).


**Gson**(구글 Gson, Google Gson)은 [JSON](https://ko.wikipedia.org/wiki/JSON "wikilink")의 자바 오브젝트의 [직렬화](../Page/직렬화.md "wikilink"), 역직렬화를 해주는 [오픈 소스](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink") [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink") 라이브러리이다.

## 역사

Gson 라이브러리는 원래 [구글](https://ko.wikipedia.org/wiki/구글 "wikilink")의 내부 목적을 위해 개발되었으며 버전 1.0이 [아파치 라이선스 2.0의](https://ko.wikipedia.org/wiki/아파치_라이선스_2.0 "wikilink") 조항 하에 2008년 5월 22일 출시되었다. 최신 버전 2.8.5는 2018년 5월 21일에 출시되었다.

## 버전 역사

  - 2018년 5월 21일: 버전 2.8.5
  - 2018년 5월 01일: 버전 2.8.4
  - 2018년 4월 27일: 버전 2.8.3
  - 2017년 9월 19일: 버전 2.8.2
  - 2017년 5월 30일: 버전 2.8.1
  - 2016년 10월 27일: 버전 2.8.0
  - 2016년 6월 14일: 버전 2.7
  - 2016년 2월 26일: 버전 2.6.2
  - 2016년 2월 11일: 버전 2.6.1
  - 2016년 2월 11일: 버전 2.6
  - 2015년 11월 24일: 버전 2.5
  - 2015년 10월 4일: 버전 2.4
  - 2014년 11월 20일: 버전 2.3.1
  - 2014년 8월 11일: 버전 2.3
  - 2013년 5월 13일: 버전 2.2.4
  - 2013년 4월 12일: 버전 2.2.3
  - 2012년 7월 2일: 버전 2.2.2
  - 2012년 5월 5일: 버전 2.2.1
  - 2012년 5월 5일: 버전 2.2
  - 2011년 12월 31일: 버전 2.1
  - 2011년 11월 13일: 버전 2.0
  - 2011년 4월 13일: 버전 1.7.1
  - 2011년 4월 12일: 버전 1.7
  - 2010년 11월 24일: 버전 1.6
  - 2010년 8월 19일: 버전 1.5
  - 2009년 10월 9일: 버전 1.4
  - 2009년 4월 1일: 버전 1.3
  - 2009년 1월 12일: 버전 1.3 베타
  - 2008년 8월 29일: 버전 1.2
  - 2008년 7월 18일: 버전 1.1.1
  - 2008년 7월 1일: 버전 1.1
  - 2008년 6월 17일: 버전 1.0.1
  - 2008년 5월 22일: 버전 1.0

## 사용법

Gson은 [반영을](https://ko.wikipedia.org/wiki/반영_\(컴퓨터_과학\) "wikilink") 사용하므로 (역)직렬화된 오브젝트의 클래스에 대한 추가적인 수정이 필요하지 않다. 사실 클래스가 no-args 기본 생성자만 있으면 된다. (무조건 그런 것은 아님. [기능](https://ko.wikipedia.org/wiki/#기능 "wikilink") 문단 참고)

다음의 예는 샘플 오브젝트를 직렬화할 때 가장 기초적인 Gson 사용법을 표현한 것이다:

``` java
module GsonExample {
    requires gson;
    requires java.sql; // Required by gson
    exports Person;
    exports Car;
}
```

``` java
package Car;

public class Car {
    public String manufacturer;
    public String model;
    public double capacity;
    public boolean accident;

    public Car() {
    }

    public Car(String manufacturer, String model, Double capacity, boolean accident) {
        this.manufacturer = manufacturer;
        this.model = model;
        this.capacity = capacity;
        this.accident = accident;
    }

    @Override
    public String toString() {
        return ("Manufacturer: " + manufacturer + ", " + "Model: " + model + ", " + "Capacity: " + capacity + ", " + "Accident: " + accident);
    }
}
```

``` java
package Person;

import Car.Car;

public class Person {
    public String name;
    public String surname;
    public Car[] cars;
    public int phone;
    public transient int age;

    public Person() {
    }

    public Person(String name, String surname, int phone, int age, Car[] cars) {
        this.name = name;
        this.surname = surname;
        this.cars = cars;
        this.phone = phone;
        this.age = age;
    }

    @Override
    public String toString() {
        StringBuilder sb = new StringBuilder();
        sb.append("Name: ").append(name).append(" ").append(surname).append("\n");
        sb.append("Phone: ").append(phone).append("\n");
        sb.append("Age: ").append(age).append("\n");
        int i = 0;
        for (Car item : cars) {
            i++;
            sb.append("Car ").append(i).append(": ").append(item).append("\n");
        }
        return sb.toString();
    }
}
```

호출 후

``` java
package Main;

import Car.Car;
import Person.Person;
import com.google.gson.Gson;

public class Main {
    public static void main(String[] args) {
        Gson gson = new Gson();
        Car audi = new Car("Audi", "A4", 1.8, false);
        Car skoda = new Car("Škoda", "Octavia", 2.0, true);
        Car[] cars = {audi, skoda};
        Person johnDoe = new Person("John", "Doe", 2025550191, 35, cars);
        System.out.println(gson.toJson(johnDoe));
    }
}
```

다음의 출력을 받게 된다:

``` json
{
   "name":"John",
   "surname":"Doe",
   "cars":[
      {
         "manufacturer":"Audi",
         "model":"A4",
         "capacity":1.8,
         "accident":false
      },
      {
         "manufacturer":"Škoda",
         "model":"Octavia",
         "capacity":2.0,
         "accident":true
      }
   ],
   "phone":2025550191
}
```

Person 필드 "age"가 transient로 표시되므로 출력에 포함되지 않는다.

마지막 예제에서 만든 출력을 역직렬화하려면 다음의 코드를 실행할 수 있다:

``` java
package Main;

import Person.Person;
import com.google.gson.Gson;

public class Main {
    public static void main(String[] args) {
        Gson gson = new Gson();
        String json = "{\"name\":\"John\",\"surname\":\"Doe\",\"cars\":[{\"manufacturer\":\"Audi\",\"model\":\"A4\"," +
                "\"capacity\":1.8,\"accident\":false},{\"manufacturer\":\"Škoda\",\"model\":\"Octavia\",\"capacity\"" +
                ":2.0,\"accident\":true}],\"phone\":2025550191}";
        Person johnDoe = gson.fromJson(json, Person.class);
        System.out.println(johnDoe.toString());
    }
}
```

다음의 출력이 만들어진다:

``` text
Name: John Doe
Phone: 2025550191
Age: 0
Car 1: Manufacturer: Audi, Model: A4, Capacity: 1.8, Accident: false
Car 2: Manufacturer: Škoda, Model: Octavia, Capacity: 2.0, Accident: true
```

## 기능

  - Gson은 컬렉션, 제네릭 타입, 네스티드 클래스를 관리할 수 있다 (inner class 포함. 기본값으로는 수행이 불가능하지만)
  - 직렬화를 할 때 Gson은 역직렬화되는 오브젝트의 타입 트리를 탐색한다. 이렇게 하면 JSON 입력에 보이는 추가 필드를 무시하게 된다.
  - 사용자는 프로세스 전반을 통제하고 소스 코드 접근이 불가능한 클래스의 인스턴스의 (역)직렬화도 할 수 있도록 사용자 지정 직렬화기/역직렬화기를 작성할 수 있다.
  - 사용자는 no-args 생성자 없이 클래스의 인스턴스를 역직렬화할 수 있는 InstanceCreator를 작성할 수 있다.
  - Gson은 상당한 커스터마이즈가 가능하며 다음을 지정할 수 있다:

:\* 콤팩트/프리티 출력

:\* 널 오브젝트 필드의 관리 방법 - 기본적으로 출력에 표시되지 않음

:\* 어느 필드가 (역)직렬화에서 제외되어야 하는지의 규칙

:\* 자바 필드 이름 변환 방법

## 외부 링크

  - [Gson API](https://web.archive.org/web/20180407202242/http://google.github.io/gson/apidocs/)
  - [Gson User Guide](https://github.com/google/gson/blob/master/UserGuide.md)
  - [Project Homepage](https://github.com/google/gson)
  - [Java GSON Tutorials](https://web.archive.org/web/20150128133939/http://memorynotfound.com/category/java/json/gson/)
  - [GSON Tutorial With Examples](http://tutorialtous.com/gson)

[분류:자바 라이브러리](https://ko.wikipedia.org/wiki/분류:자바_라이브러리 "wikilink") [분류:JSON](https://ko.wikipedia.org/wiki/분류:JSON "wikilink") [분류:구글의 소프트웨어](https://ko.wikipedia.org/wiki/분류:구글의_소프트웨어 "wikilink")