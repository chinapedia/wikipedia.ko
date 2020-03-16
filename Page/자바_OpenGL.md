> This article is converted from Wikipedia: [ OpenGL](https://ko.wikipedia.org/wiki/_OpenGL).


**자바 OpenGL**(Java OpenGL, **JOGL**)은 [OpenGL](../Page/OpenGL.md "wikilink")을[자바 프로그래밍 언어에](../Page/자바_\(프로그래밍_언어\).md "wikilink") 사용될 수 있도록 하는 래퍼 [라이브러리이다](../Page/라이브러리_\(컴퓨팅\).md "wikilink").\[1\]\[2\] Kenneth Bradley Russell과 Christopher John Kline에 의해 처음 개발되었다가 이후 [썬 마이크로시스템즈](../Page/썬_마이크로시스템즈.md "wikilink") 게임 테크놀로지 그룹에 의해 추가 개발되었다. 2010년 이후로 [BSD 허가서](../Page/BSD_허가서.md "wikilink") 하의 독립 [오픈 소스](../Page/오픈_소스_소프트웨어.md "wikilink") 프로젝트로 유지되고 있다. [Java Bindings for OpenGL](https://ko.wikipedia.org/wiki/Java_Bindings_for_OpenGL "wikilink")(JSR-231)의 참조 구현체이다.

JOGL은 [자바 네이티브 인터페이스](../Page/자바_네이티브_인터페이스.md "wikilink")(JNI)를 사용함으로써 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 언어 프로그램들에서 이용 가능한 대부분의 OpenGL 기능들에 접근할 수 있다.

## 코드 예제

``` java
    @Override
    public void display(GLAutoDrawable drawable) {

        GL4 gl4 = drawable.getGL().getGL4();

        gl4.glClearBufferfv(GL2ES3.GL_COLOR, 0, clearColor);
        gl4.glClearBufferfv(GL2ES3.GL_DEPTH, 0, clearDepth);

        {
            FloatUtil.makeLookAt(view, 0, eye, 0, at, 0, up, 0, tmp);
            FloatUtil.makePerspective(projection, 0, reset, 45f, aspect, near, far);

            FloatUtil.multMatrix(projection, view); // projection *= view

            transformPointer.asFloatBuffer().put(projection);
        }

        gl4.glUseProgram(programName);
        gl4.glBindVertexArray(vertexArrayName.get(0));
        gl4.glBindBufferBase(GL2ES3.GL_UNIFORM_BUFFER /*target*/, 1 /*TRANSFORM0, index*/, bufferName.get(2) /*TRANSFORM, buffer*/);

        gl4.glBindTextureUnit(0 /*diffuse*/, textureName.get(0));
        gl4.glBindSampler(0 /*diffuse*/, samplerName.get(0));

        gl4.glDrawElements(GL.GL_TRIANGLES, elementCount, GL.GL_UNSIGNED_SHORT, 0);
    }
```

## 같이 보기

  - [Java Bindings for OpenGL](https://ko.wikipedia.org/wiki/Java_Bindings_for_OpenGL "wikilink")
  - [Ardor3D](https://ko.wikipedia.org/wiki/Ardor3D "wikilink")
  - [Elflight Engine](https://ko.wikipedia.org/wiki/Elflight_Engine "wikilink")
  - [JMonkey Engine](https://ko.wikipedia.org/wiki/JMonkey_Engine "wikilink")
  - [Poxnora](https://ko.wikipedia.org/wiki/Poxnora "wikilink")
  - [룬스케이프](../Page/룬스케이프.md "wikilink")
  - [Jake2](https://ko.wikipedia.org/wiki/Jake2 "wikilink")
  - [Scilab](https://ko.wikipedia.org/wiki/Scilab "wikilink")
  - [Jreality](https://ko.wikipedia.org/wiki/Jreality "wikilink")
  - [ClearVolume](https://ko.wikipedia.org/wiki/ClearVolume "wikilink")
  - [LWJGL](../Page/LWJGL.md "wikilink")
  - [자바 OpenAL](https://ko.wikipedia.org/wiki/자바_OpenAL "wikilink")
  - [자바 OpenCL](https://ko.wikipedia.org/wiki/자바_OpenCL "wikilink")

## 각주

## 외부 링크

  -
  - [JOGL 2.3.x Specification](http://jogamp.org/deployment/jogamp-current/javadoc/jogl/javadoc/)

  - [JSR-231 Java Bindings for OpenGL](http://www.jcp.org/en/jsr/detail?id=231) website

  - [tool kiet](http://ak.kiet.le.googlepages.com/theredbookinjava.html), The OpenGL Programming Guide examples using JOGL

  - [NeHe's tutorials and sample code](https://web.archive.org/web/20071126072642/http://nehe.gamedev.net/)

  - [Setting up a JogAmp JOGL project in your favorite IDE](http://jogamp.org/wiki/index.php/Setting_up_a_JogAmp_project_in_your_favorite_IDE)

  - [Viewer3D](http://demo.dzzd.net/Viewer3D/), an applet to display interactive 3D content with JOGL

  - [Eclipse OpenGL Pack](http://sourceforge.net/projects/eclipse-opengl/) OpenGL plugin for the [Eclipse](../Page/이클립스_\(소프트웨어\).md "wikilink") IDE

[분류:3차원 그래픽 소프트웨어](https://ko.wikipedia.org/wiki/분류:3차원_그래픽_소프트웨어 "wikilink") [분류:자바 라이브러리](https://ko.wikipedia.org/wiki/분류:자바_라이브러리 "wikilink") [분류:자바 API](https://ko.wikipedia.org/wiki/분류:자바_API "wikilink") [분류:OpenGL](https://ko.wikipedia.org/wiki/분류:OpenGL "wikilink")

1.
2.