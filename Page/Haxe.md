> This article is converted from Wikipedia: [Haxe](https://ko.wikipedia.org/wiki/Haxe).


**Haxe**는 각기 다른 수많은 [컴퓨팅 플랫폼을](../Page/컴퓨팅_플랫폼.md "wikilink") 대상으로 하나의 코드 기반으로 애플리케이션과 소스 코드를 생성할 수 있는, 고급 [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink") [멀티 패러다임](https://ko.wikipedia.org/wiki/멀티_패러다임 "wikilink") [프로그래밍 언어이자](../Page/프로그래밍_언어.md "wikilink") [컴파일러](../Page/컴파일러.md "wikilink")이다.\[1\]\[2\]\[3\]\[4\] [GNU GPL](https://ko.wikipedia.org/wiki/GNU_GPL "wikilink") 버전 2로 배포되는 [자유-오픈 소스 소프트웨어이며](../Page/자유-오픈_소스_소프트웨어.md "wikilink") 표준 라이브러리의 경우 [MIT 라이선스를](https://ko.wikipedia.org/wiki/MIT_라이선스 "wikilink") 따른다.

## 언어

Haxe는 [객체 지향 프로그래밍](../Page/객체_지향_프로그래밍.md "wikilink"), [제네릭 프로그래밍](https://ko.wikipedia.org/wiki/제네릭_프로그래밍 "wikilink"), 다양한 [함수형 프로그래밍](../Page/함수형_프로그래밍.md "wikilink") 구조체를 지원하는 범용 목적의 언어이다. 반복, 예외 처리, 코드 반영 등의 기능들 또한 이 언어와 라이브러리의 내장 기능들이다.\[5\]

### 클래스

``` haxe
interface ICreature {
    public var birth:Date;
    public var name:String;

    public function age():Int;
}

class Fly implements ICreature {
    public var birth:Date;
    public var name:String;

    public function age():Int return Date.now().getFullYear() - birth.getFullYear();
}
```

### 열거형

``` haxe
enum Color {
    red;
    green;
    blue;
    rgb( r : Int, g : Int, b : Int );
}

class Colors {
    static function toInt ( c : Color ) : Int {
        return switch ( c ) {
            case red: 0xFF0000;
            case green: 0x00FF00;
            case blue: 0x0000FF;
            case rgb(r, g, b): (r << 16) | (g << 8) | b;
        }
    }
    static function validCalls() {
        var redint = toInt(Color.red);
        var rgbint = toInt(Color.rgb(100, 100, 100));
    }
}
```

### 익명(무명) 형식

``` haxe
typedef AliasForAnon = { a:Int, b:String, c:Float->Void };
```

### 함수형

``` haxe
typedef F = Int->String->Float;

typedef F2 = Int->String->F;
typedef F3 = Int->String->(Int->String->Float);
```

### 추상형

``` haxe
abstract Kilometer(Float) {
    public function new(v:Float) this = v;
}

abstract Mile(Float) {
    public function new(v:Float) this = v;
    @:to public inline function toKilometer():Kilometer return (new Kilometer(this / 0.62137));
}

class Test {
  static var km:Kilometer;
  static function main(){
    var one100Miles = new Mile(100);
    km = one100Miles;

    trace(km); // 160.935
  }
}
```

### 구조적 타이핑

``` haxe

class FooBar {

   public var foo:Int;
   public var bar:String;

   public function new(){ foo=1; bar="2";}

   function anyFooBar(v:{foo:Int,bar:String}) trace(v.foo);

   static function test(){
        var fb = new FooBar();
        fb.anyFooBar(fb);
        fb.anyFooBar({foo:123,bar:"456"});
   }
}
```

## 각주

## 외부 링크

  -
[분류:프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:프로그래밍_언어 "wikilink") [분류:함수형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:함수형_프로그래밍_언어 "wikilink") [분류:다중 패러다임 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:다중_패러다임_프로그래밍_언어 "wikilink") [분류:GPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GPL_라이선스_소프트웨어 "wikilink")

1.
2.
3.
4.
5.