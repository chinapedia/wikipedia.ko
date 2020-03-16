> This article is converted from Wikipedia: [CMake](https://ko.wikipedia.org/wiki/CMake).


**CMake**(Cross Platform Make)는 멀티플랫폼으로 사용할 수 있는 [Make의](https://ko.wikipedia.org/wiki/make_\(소프트웨어\) "wikilink") 대용품을 만들기 위한 오픈소스 프로젝트로 [키트웨어](https://ko.wikipedia.org/wiki/키트웨어 "wikilink")와 [인사이트 콘솔티엄에서](https://ko.wikipedia.org/wiki/인사이트_콘솔티엄 "wikilink") 만들었다. 스스로 기존의 Make의 과정을 수행하지는 않고 지정한 운영 체제에 맞는 Make 파일([마이크로소프트 윈도에서는](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 솔루션 파일)의 생성만을 수행하기 때문에 Meta Make라고도 불린다. 가장 큰 이점은 [유닉스 계열](../Page/유닉스_계열.md "wikilink") OS 중심이던 기존의 Make와는 달리 한번 작성해 두면 유닉스 계열은 물론, 마이크로소프트 윈도 계열의 프로그래밍 도구도 지원한다는 것이다.

## 기능

  - 소프트웨어 빌드에 특화된 언어로 독자적 설정 스크립트를 사용한다.
  - [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [포트란](../Page/포트란.md "wikilink")에 대해서는 자체적으로 의존 관계를 분석할 수 있다.
  - [스위그](https://ko.wikipedia.org/wiki/스위그 "wikilink"), [Qt](https://ko.wikipedia.org/wiki/Qt_\(툴킷\) "wikilink") 지원에 특화되어 있다.
  - [마이크로소프트 비주얼 스튜디오를](https://ko.wikipedia.org/wiki/비주얼_스튜디오 "wikilink") 자체적으로 지원한다(6, 7, 7.1, 8.0, 9.0 등).
  - [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink")용 빌드 파일을 생성할 수 있다.
  - [타임스탬프](../Page/타임스탬프.md "wikilink")를 통해 파일 내용의 변화를 알아낼 수 있다.
  - [평행 빌드를](https://ko.wikipedia.org/wiki/평행_빌드 "wikilink") 할 수 있다.
  - [크로스 컴파일을](https://ko.wikipedia.org/wiki/크로스_컴파일 "wikilink") 할 수 있다.
  - 다양한 플랫폼을 지원한다.
      - [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제([리눅스](../Page/리눅스.md "wikilink"), [BSD계](https://ko.wikipedia.org/wiki/BSD/OS "wikilink") 운영 체제 등)
      - [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink")
      - [윈도 95](https://ko.wikipedia.org/wiki/윈도_95 "wikilink")/[98](https://ko.wikipedia.org/wiki/윈도_98 "wikilink")/[NT](https://ko.wikipedia.org/wiki/윈도_NT "wikilink")/[2000](https://ko.wikipedia.org/wiki/윈도_2000 "wikilink")/[XP](https://ko.wikipedia.org/wiki/윈도_XP "wikilink") 와 [MinGW](../Page/MinGW.md "wikilink")/MSYS
  - 내부 모듈인 CTest로 [유닛 테스트를](../Page/유닛_테스트.md "wikilink") 수행할 수 있다.
  - 내부 모듈인 CPack으로 자동 인스톨러를 만들 수 있다.

## CMake 파일 예제

``` cmake
if (${UNIX})
  set (DESKTOP $ENV{HOME})
else()
  set (DESKTOP $ENV{USERPROFILE}/Desktop)
endif()

set (PRJ ${DESKTOP}/common/svn )
set (FILELIST ${PRJ}/src/source.txt )

message(STATUS "CMAKE_GENERATOR : ${CMAKE_GENERATOR}")
message(STATUS "DESKTOP : ${DESKTOP}")
message(STATUS "PRJ : ${PRJ}")
message(STATUS "FILELIST : ${FILELIST}")
message(STATUS "SYSTEM_NAME : ${CMAKE_SYSTEM_NAME}")

project(project_name)

include_directories(
  ${PRJ}/src
  ${PRJ}/includes
)

# Load SRC Variable from file
file(READ ${FILELIST} SRC)
string(REGEX REPLACE "#.*$" "" SRC ${SRC})
string(REPLACE "\n" ";" SRC ${SRC})

add_executable(${PROJECT_NAME} ${SRC} )

foreach (f ${SRC})
  set_source_files_properties(${f} PROPERTIES LANGUAGE       CXX)
endforeach(f)

if (${WIN32})
  link_directories(
  )

  add_definitions(
    -DDEFINE1
  )

  target_link_libraries(
    ${PROJECT_NAME}
    wsock32.lib
  )
endif()
```

## CMake를 채택한 프로젝트

  - [KDE](../Page/KDE.md "wikilink")(4판부터)
  - [LMMS](../Page/LMMS.md "wikilink")
  - [MySQL](../Page/MySQL.md "wikilink")([마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [리눅스](../Page/리눅스.md "wikilink"))
  - [OpenLieroX](https://ko.wikipedia.org/wiki/OpenLieroX "wikilink")
  - [OpenSceneGraph](https://ko.wikipedia.org/wiki/OpenSceneGraph "wikilink")
  - [OpenSourceComputerVision](https://ko.wikipedia.org/wiki/OpenSourceComputerVision "wikilink")
  - [SuperTux](../Page/SuperTux.md "wikilink")
  - [VTK](https://ko.wikipedia.org/wiki/VTK "wikilink")
  - [뮤즈스코어](../Page/뮤즈스코어.md "wikilink")
  - [스크리버스](https://ko.wikipedia.org/wiki/스크리버스 "wikilink")
  - [스텔라리움](../Page/스텔라리움.md "wikilink")
  - [퀀텀 GIS](https://ko.wikipedia.org/wiki/퀀텀_GIS "wikilink")
  - [포플러](../Page/포플러_\(소프트웨어\).md "wikilink") - Autoconf와 CMake를 함께 지원
  - [헷지워즈](https://ko.wikipedia.org/wiki/헷지워즈 "wikilink")
  - [GNU Radio](https://ko.wikipedia.org/wiki/Https:/en.wikipedia.org/wiki/GNU_Radio "wikilink")

## 같이 보기

  - [Autoconf](../Page/Autoconf.md "wikilink")

## 참조

<references />

## 외부 링크

  - [CMake 공식 사이트](http://www.cmake.org/)

[분류:빌드 자동화](https://ko.wikipedia.org/wiki/분류:빌드_자동화 "wikilink") [분류:컴파일 도구](https://ko.wikipedia.org/wiki/분류:컴파일_도구 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink")