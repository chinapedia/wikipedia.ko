> This article is converted from Wikipedia: [Three.js](https://ko.wikipedia.org/wiki/Three.js).


**Three.js**는 [웹 브라우저에서](../Page/웹_브라우저.md "wikilink") 애니메이션 [3차원 컴퓨터 그래픽스를](../Page/3차원_컴퓨터_그래픽스.md "wikilink") 만들고 표시하기 위해 사용되는 [크로스 브라우저](https://ko.wikipedia.org/wiki/크로스_브라우저 "wikilink") [자바스크립트 라이브러리이자](../Page/자바스크립트_라이브러리.md "wikilink") [API](../Page/API.md "wikilink")이다. 소스 코드는 [깃허브](../Page/깃허브.md "wikilink")의 한 저장소에서 호스팅된다.

## 개요

Three.js는 사유 [브라우저 플러그인에](../Page/브라우저_확장.md "wikilink") 의존하지 않고 [자바스크립트](../Page/자바스크립트.md "wikilink") 언어를 사용하여 [웹사이트](../Page/웹사이트.md "wikilink")의 한 부분으로서 [그래픽 처리 장치](../Page/그래픽_처리_장치.md "wikilink")(GPU) 가속 3차원 애니메이션을 만들 수 있게 한다.\[1\]\[2\] 이는 [WebGL](../Page/WebGL.md "wikilink")의 출현으로 인하여 가능하게 되었다.\[3\]

Three.js, [GLGE](https://ko.wikipedia.org/wiki/GLGE "wikilink"), SceneJS, PhiloGL, 그리고 수많은 기타 라이브러리 등 고급 라이브러리들은 전통적인 독립형 애플리케이션이나 플러그인에 필요했던 노력을 들이지 않고 개발자가 브라우저에 복잡한 3D 컴퓨터 애니메이션을 표시할 수 있게 되었다.\[4\]

## 역사

Three.js는 2010년 4월 Ricardo Cabello가 깃허브에 처음 출시하였다.\[5\] 이 라이브러리의 기원은 개발자 자신이 2000년대 초 [데모씬](https://ko.wikipedia.org/wiki/데모씬 "wikilink")에 참여한 시기로 거슬러 올라간다. 이 코드는 [액션스크립트](../Page/액션스크립트.md "wikilink")로 처음 개발되었다가 2009년 [자바스크립트](../Page/자바스크립트.md "wikilink")로 이식되었다.

## 사용법

Three.js 라이브러리는 하나의 자바스크립트 파일이다. 로컬이나 원격 사본에 연결함으로써 웹 페이지 안에 포함시킬 수 있다.

``` javascript
<script src="js/three.min.js"></script>
```

다음의 코드는 씬을 하나 만들고 카메라 하나와 큐브 하나를 해당 씬에 추가하고 WebGL 렌더러를 만들고 document.body 요소에 뷰포트를 추가한다. 로드되면 큐브는 X축과 Y축 주변을 회전한다.

``` javascript
<script>

    var camera, scene, renderer,
    geometry, material, mesh;

    init();
    animate();

    function init() {
        scene = new THREE.Scene();

        camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 1, 10000 );
        camera.position.z = 1000;

        geometry = new THREE.BoxGeometry( 200, 200, 200 );
        material = new THREE.MeshBasicMaterial( { color: 0xff0000, wireframe: true } );

        mesh = new THREE.Mesh( geometry, material );
        scene.add( mesh );

        renderer = new THREE.WebGLRenderer();
        renderer.setSize( window.innerWidth, window.innerHeight );

        document.body.appendChild( renderer.domElement );
    }

    function animate() {
        requestAnimationFrame( animate );
        render();
    }

    function render() {
        mesh.rotation.x += 0.01;
        mesh.rotation.y += 0.02;

        renderer.render( scene, camera );
    }

</script>
```

## 각주

## 참고 자료

  -
  -
  - \- "Three.js can make game development easier by taking care of low-level details"

  -
  -
<!-- end list -->

  -
## 외부 링크

  -
[분류:2010년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2010년_소프트웨어 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink") [분류:자바스크립트 라이브러리](https://ko.wikipedia.org/wiki/분류:자바스크립트_라이브러리 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:WebGL](https://ko.wikipedia.org/wiki/분류:WebGL "wikilink")

1.  [O3D](../Page/O3D.md "wikilink")
2.  [유니티 (게임 엔진)](../Page/유니티_\(게임_엔진\).md "wikilink")
3.
4.
5.