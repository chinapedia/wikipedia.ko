> This article is converted from Wikipedia: [OpenGL](https://ko.wikipedia.org/wiki/OpenGL).


**오픈 그래픽 라이브러리**( 줄여서 **OpenGL**)\[1\]\[2\]은 1992년 [실리콘 그래픽스사에서](../Page/실리콘_그래픽스.md "wikilink") 만든 2차원 및 3차원 그래픽스 표준 [API](../Page/API.md "wikilink") 규격으로, 프로그래밍 언어 간 플랫폼 간의 교차 응용 프로그래밍을 지원한다. 이 API는 약 250여개 가량의 함수 호출을 이용하여 단순한 기하도형에서부터 복잡한 삼차원 장면을 생성할 수 있다. OpenGL은 현재 [CAD](https://ko.wikipedia.org/wiki/CAD "wikilink"), [가상현실](https://ko.wikipedia.org/wiki/가상현실 "wikilink"), [정보시각화](https://ko.wikipedia.org/wiki/정보시각화 "wikilink"), 비행 시뮬레이션 등의 분야에서 활용되고 있다. 또한 컴퓨터 게임 분야에서도 널리 활용되고 있으며, [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")사의 [Direct3D와](https://ko.wikipedia.org/wiki/다이렉트3D "wikilink") 함께 컴퓨터 그래픽 세계를 양분하고 있다. Direct3D와는 달리, 표준안이 여러 관련 업체의 토론과 제안으로 이루어지기에 버전 업데이트는 느린 편이다. OpenGL을 사용하여 개발된 대표적인 게임은 [이드 소프트웨어의](https://ko.wikipedia.org/wiki/이드_소프트웨어 "wikilink") [퀘이크](https://ko.wikipedia.org/wiki/퀘이크_\(비디오_게임\) "wikilink"), [둠3](https://ko.wikipedia.org/wiki/둠3 "wikilink") 시리즈이다. 현재 비영리 기술 컨소시엄인 [크로노스 그룹에](https://ko.wikipedia.org/wiki/크로노스_그룹 "wikilink") 의하여 관리되고 있다.

## 역사

1980년대에 다양한 그래픽 하드웨어와 기능할 수 있는 소프트웨어를 개발하는 일은 큰 도전이었다. 소프트웨어 개발자들은 개별 하드웨어에 맞추어 맞춤식 인터페이스와 드라이버를 작성하였다. 이러한 일은 비용이 많이 들었고 노력이 크게 늘어나게 되었다.

1990년대 초, [실리콘 그래픽스](../Page/실리콘_그래픽스.md "wikilink")(SGI)는 워크스테이션용 3차원 그래픽스의 리더였다. [IRIS GL](https://ko.wikipedia.org/wiki/IRIS_GL "wikilink") API\[3\]는 [사실 상의](https://ko.wikipedia.org/wiki/데_팍토 "wikilink") 표준 산업이 되어 오픈 표준 기반의 [PHIGS](https://ko.wikipedia.org/wiki/PHIGS "wikilink")를 무색케 했다. IRIS GL이 사용하기 쉬운 것으로 간주되었을 뿐 아니라, [즉시 모드](https://ko.wikipedia.org/wiki/즉시_모드 "wikilink") 렌더링을 지원하였기 때문이다. 이와 대조적으로, PHIGS는 사용하기 어렵고 기능이 시대에 뒤쳐진 것으로 간주되었다.

SGI의 경쟁사들([썬 마이크로시스템즈](../Page/썬_마이크로시스템즈.md "wikilink"), [휴렛 패커드](https://ko.wikipedia.org/wiki/휴렛_패커드 "wikilink"), [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink"))은 PHIGS 표준의 확장을 지원하는 3차원 하드웨어를 마케팅할 수 있었다. 더 많은 3차원 그래픽스 제공자들이 시장에 진입하면서 SGI 시장 점유율을 약화시켰다. 시장에 영향을 주려는 노력으로 SGI는 IrisGL API를 오픈 표준으로 전환시키기로 결정하였는데, 이것이 OpenGL이다.

## 버전 역사

OpenGL의 최초 버전은 1992년 6월 30일 Mark Segal and [Kurt Akeley에](https://ko.wikipedia.org/wiki/Kurt_Akeley "wikilink") 의해 출시되었다. 그 이후로 새로운 버전의 사양을 출시함으로써 OpenGL은 확장되어왔다.

### 개요

  - OpenGL 1.1
  - OpenGL 1.2\[4\]
  - OpenGL 1.3
  - OpenGL 1.4
  - OpenGL 1.5
  - OpenGL 2.0 - [GLSL](https://ko.wikipedia.org/wiki/GLSL "wikilink") 1.1
  - OpenGL 2.1 - GLSL 1.2
  - OpenGL 3.0 - GLSL 1.3
  - OpenGL 3.1 - GLSL 1.4
  - OpenGL 3.2 - GLSL 1.5
  - OpenGL 3.3 - GLSL 3.30
  - OpenGL 4.0 - GLSL 4.00
  - OpenGL 4.1 - GLSL 4.10
  - OpenGL 4.2 - GLSL 4.20
  - OpenGL 4.3 - GLSL 4.30
  - OpenGL 4.4 - GLSL 4.40
  - OpenGL 4.5 - GLSL 4.50
  - OpenGL 4.6 - GLSL 4.60

### OpenGL 1.1

출시일: 1997년 3월 4일

<table>
<thead>
<tr class="header">
<th><p>Extension Name</p></th>
<th><p>Sort #Number</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_polygon_offset.txt">EXT_polygon_offset</a></p></td>
<td><p>Extension #3</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture.txt">EXT_texture</a></p></td>
<td><p>Extension #4</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_subtexture.txt">EXT_subtexture</a><br />
<a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_copy_texture.txt">EXT_copy_texture</a></p></td>
<td><p>Extension #9<br />
Extension #10</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_object.txt">EXT_texture_object</a></p></td>
<td><p>Extension #20</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_vertex_array.txt">EXT_vertex_array</a></p></td>
<td><p>Extension #30</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_blend_logic_op.txt">EXT_blend_logic_op</a></p></td>
<td><p>Extension #39</p></td>
</tr>
</tbody>
</table>

### OpenGL 1.2

출시일: 1998년 3월 16일

| Extension Name                                                                                                           | Sort \#Number   |
| ------------------------------------------------------------------------------------------------------------------------ | --------------- |
| [EXT_texture3D](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture3D.txt)                               | Extension \#6   |
| [EXT_packed_pixels](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_packed_pixels.txt)                      | Extension \#23  |
| [SGIS_texture_lod](https://www.khronos.org/registry/OpenGL/extensions/SGIS/SGIS_texture_lod.txt)                       | Extension \#24  |
| [EXT_rescale_normal](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_rescale_normal.txt)                    | Extension \#27  |
| [SGIS_texture_edge_clamp](https://www.khronos.org/registry/OpenGL/extensions/SGIS/SGIS_texture_edge_clamp.txt)        | Extension \#35  |
| [EXT_draw_range_elements](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_draw_range_elements.txt)         | Extension \#112 |
| [EXT_bgra](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_bgra.txt)                                         | Extension \#129 |
| [EXT_separate_specular_color](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_separate_specular_color.txt) | Extension \#144 |

#### OpenGL 1.2.1

출시일: 1998년 10월 14일

### OpenGL 1.3

출시일: 2001년 8월 14일

<table>
<thead>
<tr class="header">
<th><p>Extension Name</p></th>
<th><p>Sort #Number</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_multitexture.txt">ARB_multitexture</a></p></td>
<td><p>in OpenGL 1.2.1 integrated</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_transpose_matrix.txt">ARB_transpose_matrix</a></p></td>
<td><p>ARB Extension #3</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_multisample.txt">ARB_multisample</a></p></td>
<td><p>ARB Extension #5</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_cube_map.txt">ARB_texture_cube_map</a></p></td>
<td><p>ARB Extension #7</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_env_add.txt">ARB_texture_env_add</a><br />
<a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_env_combine.txt">ARB_texture_env_combine</a><br />
<a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_env_dot3.txt">ARB_texture_env_dot3</a></p></td>
<td><p>ARB Extension #6<br />
ARB Extension #17<br />
ARB Extension #19</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_compression.txt">ARB_texture_compression</a></p></td>
<td><p>ARB Extension #12</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_border_clamp.txt">ARB_texture_border_clamp</a></p></td>
<td><p>ARB Extension #13</p></td>
</tr>
</tbody>
</table>

### OpenGL 1.4

출시일: 2002년 7월 24일

<table>
<thead>
<tr class="header">
<th><p>Extension Name</p></th>
<th><p>Sort #Number</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/SGIS/SGIS_generate_mipmap.txt">SGIS_generate_mipmap</a></p></td>
<td><p>Extension 32</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_blend_color.txt">EXT_blend_color</a><br />
<a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_blend_subtract.txt">EXT_blend_subtract</a></p></td>
<td><p>Extension #2<br />
Extension #38</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_blend_minmax.txt">EXT_blend_minmax</a></p></td>
<td><p>OpenGL Extension #37</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_secondary_color.txt">EXT_secondary_color</a></p></td>
<td><p>Extension #145</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_multi_draw_arrays.txt">EXT_multi_draw_arrays</a></p></td>
<td><p>Extension #148</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_fog_coord.txt">EXT_fog_coord</a></p></td>
<td><p>Extension #149</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_blend_func_separate.txt">EXT_blend_func_separate</a></p></td>
<td><p>Extension #173</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_stencil_wrap.txt">EXT_stencil_wrap</a></p></td>
<td><p>Extension #176</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_lod_bias.txt">EXT_texture_lod_bias</a></p></td>
<td><p>OpenGL Extension #186</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/NV/NV_blend_square.txt">NV_blend_square</a></p></td>
<td><p>Extension 194</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_point_parameters.txt">ARB_point_parameters</a></p></td>
<td><p>ARB Extension #14</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_env_crossbar.txt">ARB_texture_env_crossbar</a></p></td>
<td><p>ARB Extension #18</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_mirrored_repeat.txt">ARB_texture_mirrored_repeat</a></p></td>
<td><p>ARB Extension #21</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_depth_texture.txt">ARB_depth_texture</a><br />
<a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shadow.txt">ARB_shadow</a></p></td>
<td><p>ARB Extension #22<br />
ARB Extension #23</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_window_pos.txt">ARB_window_pos</a></p></td>
<td><p>ARB Extension #25</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_vertex_program.txt">ARB_vertex_program</a></p></td>
<td><p>ARB Extension #26</p></td>
</tr>
</tbody>
</table>

### OpenGL 1.5

출시일: 2003년 7월 29일

| Extension Name                                                                                                     | Sort \#Number      |
| ------------------------------------------------------------------------------------------------------------------ | ------------------ |
| [ARB_vertex_buffer_object](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_vertex_buffer_object.txt) | ARB Extension \#28 |
| [ARB_occlusion_query](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_occlusion_query.txt)            | ARB Extension \#29 |
| [EXT_shadow_funcs](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_shadow_funcs.txt)                  | Extension \#267    |

### OpenGL 2.0

출시일: 2004년 9월 7일

<table>
<thead>
<tr class="header">
<th><p>Extension Name</p></th>
<th><p>Sort #Number</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_objects.txt">ARB_shader_objects</a><br />
<a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_vertex_shader.txt">ARB_vertex_shader</a><br />
<a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_fragment_shader.txt">ARB_fragment_shader</a><br />
<a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shading_language_100.txt">ARB_shading_language_100</a></p></td>
<td><p>ARB Extension #30<br />
ARB Extension #31<br />
ARB Extension #32<br />
ARB Extension #33</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_non_power_of_two.txt">ARB_texture_non_power_of_two</a></p></td>
<td><p>ARB Extension #34</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_point_sprite.txt">ARB_point_sprite</a></p></td>
<td><p>ARB Extension #35</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_draw_buffers.txt">ARB_draw_buffers</a></p></td>
<td><p>ARB Extension #37</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_stencil_two_side.txt">EXT_stencil_two_side</a><br />
<a href="https://www.khronos.org/registry/OpenGL/extensions/ATI/ATI_separate_stencil.txt">ATI_separate_stencil</a></p></td>
<td><p>Extension #268<br />
Extension #289</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_blend_equation_separate.txt">EXT_blend_equation_separate</a></p></td>
<td><p>Extension #299</p></td>
</tr>
</tbody>
</table>

### OpenGL 2.1

출시일: 2006년 7월 2일

| Extension Name                                                                                                   | Sort \#Number      |
| ---------------------------------------------------------------------------------------------------------------- | ------------------ |
| [ARB_pixel_buffer_object](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_pixel_buffer_object.txt) | ARB Extension \#42 |
| [EXT_texture_sRGB](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_sRGB.txt)                | Extension \#315    |

### OpenGL 3.0

출시일: 2008년 8월 11일

<table>
<thead>
<tr class="header">
<th><p>Extension</p></th>
<th><p>Details</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_gpu_shader4.txt">EXT_gpu_shader4</a></p></td>
<td><p>Extension #326</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_color_buffer_float.txt">ARB_color_buffer_float</a></p></td>
<td><p>ARB Extension #39</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_half_float_pixel.txt">ARB_half_float_pixel</a></p></td>
<td><p>ARB Extension #40</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_float.txt">ARB_texture_float</a></p></td>
<td><p>ARB Extension #41</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_depth_buffer_float.txt">ARB_depth_buffer_float</a></p></td>
<td><p>ARB Extension #43</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_framebuffer_object.txt">ARB_framebuffer_object</a></p></td>
<td><p>ARB Extension #45</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_half_float_vertex.txt">ARB_half_float_vertex</a></p></td>
<td><p>ARB Extension #48</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_map_buffer_range.txt">ARB_map_buffer_range</a></p></td>
<td><p>ARB Extension #50</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_rg.txt">ARB_texture_rg</a></p></td>
<td><p>ARB Extension #53</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_vertex_array_object.txt">ARB_vertex_array_object</a></p></td>
<td><p>ARB Extension #54</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/GLX_ARB_create_context.txt">GLX_ARB_create_context</a></p></td>
<td><p>ARB Extension #56 (GLX_ARB_create_context), ARB Extension #75 (GLX_ARB_create_context_profile)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_framebuffer_object.txt">ARB_framebuffer_object</a></p></td>
<td><p>ARB Extension #45</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/NV/NV_half_float.txt">NV_half_float</a></p></td>
<td><p>Extension #283</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_framebuffer_object.txt">EXT_framebuffer_object</a></p></td>
<td><p>Extension #310</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_packed_depth_stencil.txt">EXT_packed_depth_stencil</a></p></td>
<td><p>Extension #312</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_framebuffer_blit.txt">EXT_framebuffer_blit</a><br />
<a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_framebuffer_multisample.txt">EXT_framebuffer_multisample</a></p></td>
<td><p>Extension #316, #317</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_packed_float.txt">EXT_packed_float</a></p></td>
<td><p>Extension #328</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_array.txt">EXT_texture_array</a></p></td>
<td><p>Extension #329</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_compression_rgtc.txt">EXT_texture_compression_rgtc</a></p></td>
<td><p>OpenGL Extension #332</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_shared_exponent.txt">EXT_texture_shared_exponent</a></p></td>
<td><p>Extension #333</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/NV/NV_depth_buffer_float.txt">NV_depth_buffer_float</a></p></td>
<td><p>Extension #334</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_framebuffer_sRGB.txt">EXT_framebuffer_sRGB</a></p></td>
<td><p>Extension #337</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_draw_buffers2.txt">EXT_draw_buffers2</a></p></td>
<td><p>Extension #340</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_integer.txt">EXT_texture_integer</a></p></td>
<td><p>Extension #343</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/NV/NV_conditional_render.txt">NV_conditional_render</a></p></td>
<td><p>OpenGL Extension #346</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_transform_feedback.txt">EXT_transform_feedback</a></p></td>
<td><p>Extension #352</p></td>
</tr>
</tbody>
</table>

### OpenGL 3.1

출시일: 2009년 3월 24일

| Details                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------- |
| [ARB_texture_rectangle](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_rectangle.txt)          |
| [ARB_draw_instanced](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_draw_instanced.txt)                |
| [ARB_texture_buffer_object](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_buffer_object.txt) |
| [ARB_uniform_buffer_object](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_uniform_buffer_object.txt) |
| [ARB_copy_buffer](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_copy_buffer.txt)                      |
| [NV_primitive_restart](https://www.khronos.org/registry/OpenGL/extensions/NV/NV_primitive_restart.txt)             |
| [EXT_texture_snorm](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_snorm.txt)                  |

### OpenGL 3.2

출시일: 2009년 8월 3일

<table>
<thead>
<tr class="header">
<th><p>Extension</p></th>
<th><p>Details</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_geometry_shader4.txt">ARB_geometry_shader4</a><br />
(heavily modified)</p></td>
<td><p>ARB Extension #47 (NVIDIA Revision: 26)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_depth_clamp.txt">ARB_depth_clamp</a></p></td>
<td><p>ARB Extension #61</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_draw_elements_base_vertex.txt">ARB_draw_elements_base_vertex</a></p></td>
<td><p>ARB Extension #62</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_fragment_coord_conventions.txt">ARB_fragment_coord_conventions</a></p></td>
<td><p>ARB Extension #63</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_provoking_vertex.txt">ARB_provoking_vertex</a></p></td>
<td><p>ARB Extension #64</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_seamless_cube_map.txt">ARB_seamless_cube_map</a></p></td>
<td><p>ARB Extension #65</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_sync.txt">ARB_sync</a></p></td>
<td><p>ARB Extension #66</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_multisample.txt">ARB_texture_multisample</a></p></td>
<td><p>ARB Extension #67</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_vertex_array_bgra.txt">ARB_vertex_array_bgra</a></p></td>
<td><p>ARB Extension #68</p></td>
</tr>
</tbody>
</table>

### OpenGL 3.3

출시일: 2010년 3월 11일

| Extension                                                                                                                          | Details            |
| ---------------------------------------------------------------------------------------------------------------------------------- | ------------------ |
| [ARB_instanced_arrays](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_instanced_arrays.txt)                          | ARB Extension \#49 |
| [ARB_blend_func_extended](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_blend_func_extended.txt)                   | ARB Extension \#78 |
| [ARB_explicit_attrib_location](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_explicit_attrib_location.txt)         | ARB Extension \#79 |
| [ARB_occlusion_query2](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_occlusion_query2.txt)                          | ARB Extension \#80 |
| [ARB_sampler_objects](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_sampler_objects.txt)                            | ARB Extension \#81 |
| [ARB_shader_bit_encoding](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_bit_encoding.txt)                   | ARB Extension \#82 |
| [ARB_texture_rgb10_a2ui](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_rgb10_a2ui.txt)                     | ARB Extension \#83 |
| [ARB_texture_swizzle](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_swizzle.txt)                            | ARB Extension \#84 |
| [ARB_timer_query](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_timer_query.txt)                                    | ARB Extension \#85 |
| [ARB_vertex_type_2_10_10_10_rev](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_vertex_type_2_10_10_10_rev.txt) | ARB Extension \#86 |

### OpenGL 4.0

출시일: 2010년 3월 11일

| Extension                                                                                                                         | Details            |
| --------------------------------------------------------------------------------------------------------------------------------- | ------------------ |
| [ARB_draw_buffers_blend](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_draw_buffers_blend.txt)                    | ARB Extension \#69 |
| [ARB_sample_shading](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_sample_shading.txt)                             | ARB Extension \#70 |
| [ARB_texture_cube_map_array](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_cube_map_array.txt)           | ARB Extension \#71 |
| [ARB_texture_gather](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_gather.txt)                             | ARB Extension \#72 |
| [ARB_texture_query_lod](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_query_lod.txt)                      | ARB Extension \#73 |
| [ARB_draw_indirect](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_draw_indirect.txt)                               | ARB Extension \#87 |
| [ARB_gpu_shader5](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_gpu_shader5.txt)                                   | ARB Extension \#88 |
| [ARB_gpu_shader_fp64](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_gpu_shader_fp64.txt)                          | ARB Extension \#89 |
| [ARB_shader_subroutine](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_subroutine.txt)                       | ARB Extension \#90 |
| [ARB_tessellation_shader](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_tessellation_shader.txt)                   | ARB Extension \#91 |
| [ARB_texture_buffer_object_rgb32](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_buffer_object_rgb32.txt) | ARB Extension \#92 |
| [ARB_transform_feedback2](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_transform_feedback2.txt)                   | ARB Extension \#93 |
| [ARB_transform_feedback3](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_transform_feedback3.txt)                   | ARB Extension \#94 |

### OpenGL 4.1

출시일: 2010년 7월 26일

| Extension                                                                                                                | Details             |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------- |
| [ARB_ES2_compatibility](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_ES2_compatibility.txt)              | ARB Extension \#95  |
| [ARB_get_program_binary](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_get_program_binary.txt)           | ARB Extension \#96  |
| [ARB_separate_shader_objects](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_separate_shader_objects.txt) | ARB Extension \#97  |
| [ARB_shader_precision](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_precision.txt)                | ARB Extension \#98  |
| [ARB_vertex_attrib_64bit](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_vertex_attrib_64bit.txt)         | ARB Extension \#99  |
| [ARB_viewport_array](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_viewport_array.txt)                    | ARB Extension \#100 |

### OpenGL 4.2

*출시일:* 2011년 8월 8일\[5\]

| Extension                                                                                                                                   | Details             |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| [ARB_texture_compression_bptc](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_compression_bptc.txt)                  | ARB Extension \#77  |
| [ARB_compressed_texture_pixel_storage](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_compressed_texture_pixel_storage.txt) | ARB Extension \#110 |
| [ARB_shader_atomic_counters](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_atomic_counters.txt)                      | ARB Extension \#114 |
| [ARB_texture_storage](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_storage.txt)                                     | ARB Extension \#117 |
| [ARB_transform_feedback_instanced](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_transform_feedback_instanced.txt)          | ARB Extension \#109 |
| [ARB_base_instance](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_base_instance.txt)                                         | ARB Extension \#107 |
| [ARB_shader_image_load_store](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_image_load_store.txt)                   | ARB Extension \#115 |
| [ARB_conservative_depth](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_conservative_depth.txt)                               | ARB Extension \#111 |
| [ARB_shading_language_420pack](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shading_language_420pack.txt)                  | ARB Extension \#108 |
| [ARB_internalformat_query](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_internalformat_query.txt)                           | ARB Extension \#112 |
| [ARB_map_buffer_alignment](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_map_buffer_alignment.txt)                          | ARB Extension \#113 |
| [ARB_shading_language_packing](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shading_language_packing.txt)                  | ARB Extension \#116 |

### OpenGL 4.3

*출시일:* 2012년 8월 6일\[6\]

| Extension                                                                                                                             | Details             |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| [KHR_debug](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_debug.txt)                                                    | ARB Extension \#119 |
| [ARB_arrays_of_arrays](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_arrays_of_arrays.txt)                            | ARB Extension \#120 |
| [ARB_clear_buffer_object](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_clear_buffer_object.txt)                      | ARB Extension \#121 |
| [ARB_compute_shader](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_compute_shader.txt)                                 | ARB Extension \#122 |
| [ARB_copy_image](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_copy_image.txt)                                         | ARB Extension \#123 |
| [ARB_texture_view](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_view.txt)                                     | ARB Extension \#124 |
| [ARB_vertex_attrib_binding](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_vertex_attrib_binding.txt)                  | ARB Extension \#125 |
| [ARB_ES3_compatibility](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_ES3_compatibility.txt)                           | ARB Extension \#127 |
| [ARB_explicit_uniform_location](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_explicit_uniform_location.txt)          | ARB Extension \#128 |
| [ARB_fragment_layer_viewport](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_fragment_layer_viewport.txt)              | ARB Extension \#129 |
| [ARB_framebuffer_no_attachments](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_framebuffer_no_attachments.txt)        | ARB Extension \#130 |
| [ARB_internalformat_query2](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_internalformat_query2.txt)                   | ARB Extension \#131 |
| [ARB_invalidate_subdata](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_invalidate_subdata.txt)                         | ARB Extension \#132 |
| [ARB_multi_draw_indirect](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_multi_draw_indirect.txt)                      | ARB Extension \#133 |
| [ARB_program_interface_query](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_program_interface_query.txt)              | ARB Extension \#134 |
| [ARB_robust_buffer_access_behavior](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_robust_buffer_access_behavior.txt) | ARB Extension \#135 |
| [ARB_shader_image_size](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_image_size.txt)                          | ARB Extension \#136 |
| [ARB_shader_storage_buffer_object](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_storage_buffer_object.txt)   | ARB Extension \#137 |
| [ARB_stencil_texturing](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_stencil_texturing.txt)                           | ARB Extension \#138 |
| [ARB_texture_buffer_range](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_buffer_range.txt)                    | ARB Extension \#139 |
| [ARB_texture_query_levels](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_query_levels.txt)                    | ARB Extension \#140 |
| [ARB_texture_storage_multisample](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_storage_multisample.txt)      | ARB Extension \#141 |

### OpenGL 4.4

*출시일:* 2013년 7월 22일\[7\]

| Extension                                                                                                                            | Details             |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------- |
| [ARB_buffer_storage](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_buffer_storage.txt)                                | ARB Extension \#144 |
| [ARB_clear_texture](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_clear_texture.txt)                                  | ARB Extension \#145 |
| [ARB_enhanced_layouts](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_enhanced_layouts.txt)                            | ARB Extension \#146 |
| [ARB_multi_bind](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_multi_bind.txt)                                        | ARB Extension \#147 |
| [ARB_query_buffer_object](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_query_buffer_object.txt)                     | ARB Extension \#148 |
| [ARB_texture_mirror_clamp_to_edge](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_mirror_clamp_to_edge.txt) | ARB Extension \#149 |
| [ARB_texture_stencil8](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_stencil8.txt)                            | ARB Extension \#150 |
| [ARB_vertex_type_10f_11f_11f_rev](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_vertex_type_10f_11f_11f_rev.txt)  | ARB Extension \#151 |



### OpenGL 4.5

*출시일:* 2014년 8월 11일\[8\]\[9\]

| Extension                                                                                                                           | Details                |
| ----------------------------------------------------------------------------------------------------------------------------------- | ---------------------- |
| [ARB_ES3_1_compatibility](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_ES3_1_compatibility.txt)                    | ARB Extension \#159    |
| [ARB_clip_control](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_clip_control.txt)                                   | ARB Extension \#160,   |
| [ARB_conditional_render_inverted](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_conditional_render_inverted.txt)    | ARB Extension \#161    |
| [ARB_cull_distance](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_cull_distance.txt)                                 | ARB Extension \#162    |
| [ARB_derivative_control](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_derivative_control.txt)                       | ARB Extension \#163    |
| [ARB_direct_state_access](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_direct_state_access.txt)                    | ARB Extension \#164    |
| [ARB_get_texture_sub_image](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_get_texture_sub_image.txt)               | ARB Extension \#165    |
| [ARB_shader_texture_image_samples](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_texture_image_samples.txt) | ARB Extension \#166    |
| [ARB_texture_barrier](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_barrier.txt)                             | ARB Extension \#167    |
| [KHR_context_flush_control](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_context_flush_control.txt)                | ARB Extension \#168    |
| [KHR_robustness](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_robustness.txt)                                        | ARB Extension \#170    |
| [EXT_shader_integer_mix](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_shader_integer_mix.txt)                      | OpenGL Extension \#437 |



### OpenGL 4.6

*출시일:* 2017년 7월 31일\[10\]\[11\]\[12\]

| Extension                                                                                                                                     | Details              |
| --------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| [ARB_indirect_parameters](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_indirect_parameters.txt)                               | ARB Extension \#154, |
| [ARB_shader_draw_parameters](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_draw_parameters.txt)                        | ARB Extension \#156, |
| [ARB_shader_group_vote](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_group_vote.txt)                                  | ARB Extension \#157  |
| [ARB_pipeline_statistics_query](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_pipeline_statistics_query.txt)                  | ARB Extension \#171  |
| [ARB_transform_feedback_overflow_query](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_transform_feedback_overflow_query.txt) | ARB Extension \#173  |
| [KHR_no_error](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_no_error.txt)                                                     | ARB Extension \#175  |
| [ARB_shader_atomic_counter_ops](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_atomic_counter_ops.txt)                 | ARB Extension \#182  |
| [ARB_gl_spirv](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_gl_spirv.txt)                                                     | ARB Extension \#190  |
| [ARB_polygon_offset_clamp](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_polygon_offset_clamp.txt)                            | ARB Extension \#193  |
| [ARB_spirv_extensions](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_spirv_extensions.txt)                                     | ARB Extension \#194  |
| [ARB_texture_filter_anisotropic](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_filter_anisotropic.txt)                | ARB Extension \#195  |

## 설계

[섬네일](https://ko.wikipedia.org/wiki/파일:Pipeline_OpenGL.svg "wikilink") OpenGL은 두 가지의 주된 용도를 제공한다:

  - 프로그래머에게 단일한 API를 제공함으로써 서로 다른 [3차원 가속기](https://ko.wikipedia.org/wiki/3차원_가속기 "wikilink") 사이의 복잡한 상호 정보교환 방식을 간단하게 한다.
  - (필요하다면 소프트웨어적인 에뮬레이션을 이용하더라도) 모든 구현이 완전한 OpenGL 기능 집합을 지원하도록 강제함으로써 각각의 하드웨어 플랫폼마다 다른 능력 차이를 감추는 역할을 한다.

OpenGL의 동작은 점, 선, 다각형과 같은 기본 도형을 그리고, 이를 [픽셀](https://ko.wikipedia.org/wiki/픽셀 "wikilink") 형식으로 변환하는 것을 허용하고 있다. 이러한 일은 OpenGL 상태 머신(OpenGL State Machine)이라는 [그래픽스 파이프라인을](https://ko.wikipedia.org/wiki/그래픽스_파이프라인 "wikilink") 통하여 이루어진다.

## 예제

``` c
glClear( GL_COLOR_BUFFER_BIT );
```

  -
    이 문장은 색상 버퍼를 소거하여 화면을 빈화면으로 만든다.

<!-- end list -->

``` c
glMatrixMode( GL_PROJECTION ); /* 뒤이어 나타나는 행렬 명령이 투영행렬에 영향을 줌 */
glLoadIdentity(); /* 투영행렬을 단위 행렬로 초기화 함 */
glFrustum( -1, 1, -1, 1, 1, 1000 ); /* 투시투영행렬을 적용시킴 */
```

  -
    위 문장은 투영행렬을 초기화한 후, 가시 영역을 표현하는 행렬로 삼차원 [절두체](https://ko.wikipedia.org/wiki/절두체 "wikilink") 행렬을 사용한다는 명령이다. 이 행렬은 카메라에 상대적인 공간에서 표현되는 객체를 OpenGL의 투영 공간으로 변환시키는 일을 한다.

<!-- end list -->

``` c
glMatrixMode( GL_MODELVIEW ); /* 뒤이어 나타나는 행렬 명령이 모델뷰행렬에 영향을 줌 */
glLoadIdentity(); /* 모델뷰행렬을 단위행렬로 초기화 함 */
glTranslatef( 0, 0, -3 ); /* z 축으로 3 단위만큼 모델뷰를 평행이동시킴 */
```

  -
    위 문장은 모델뷰 행렬을 단위행렬로 초기화시킨다. 이 행렬은 모델에 상대적인 좌표로부터 카메라 공간으로의 변환을 정의하는 행렬이다.

<!-- end list -->

``` glsl
glBegin( GL_POLYGON ); /* 다각형을 만든다 */
  glColor3f( 0, 1, 0 );               /* 현재 색상을 녹색으로 설정한다 */
  glVertex3f( -1, -1, 0 );            /* 다각형에 필요한 정점을 만든다 */
  glVertex3f( -1, 1, 0 );             /* 다각형에 필요한 정점을 만든다 */
  glVertex3f( 1, 1, 0 );              /* 다각형에 필요한 정점을 만든다 */
  glVertex3f( 1, -1, 0 );             /* 다각형에 필요한 정점을 만든다 */
glEnd(); /* 다각형 만드는 일을 종료시킨다 */
```

  -
    위의 명령은 XY 평면 위에 녹색의 다각형을 그리는 일을 한다.

## 같이 보기

  - [GLSL](https://ko.wikipedia.org/wiki/GLSL "wikilink") - OpenGL의 상위 레벨 셰이딩 언어.
  - [글라이드](../Page/글라이드.md "wikilink") - 부두 그래픽 가속 카드를 위한 3D 그래픽스 API.
  - [OpenGL ES](../Page/OpenGL_ES.md "wikilink") - 임베디드 단말을 위한 OpenGL.

### OpenGL 지원 라이브러리

  - [GLUT](https://ko.wikipedia.org/wiki/OpenGL_유틸리티_툴킷 "wikilink") – OpenGL 유틸리티 툴킷으로 윈도 시스템에 독립적인 OpenGL 프로그램을 작성하도록 도와주는 도구.
  - [SDL](../Page/심플_다이렉트미디어_레이어.md "wikilink") – Simple DirectMedia Layer.
  - [GLU](https://ko.wikipedia.org/wiki/OpenGL_Utility_Library "wikilink") – OpenGL 프로그램을 위한 추가적인 함수를 제공.
  - [GLee](https://ko.wikipedia.org/wiki/OpenGL_Easy_Extension_library "wikilink") - OpenGL 프로그램을 위한 단순한 추가 라이브러리 제공.
  - [GLEW](https://ko.wikipedia.org/wiki/OpenGL_Extension_Wrangler_Library "wikilink") – OpenGL 확장 Wrangler 라이브러리 제공.
  - [GLUI](https://ko.wikipedia.org/wiki/OpenGL_사용자_인터페이스_라이브러리 "wikilink") - GLUT로 만들어진 [GUI](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") 툴킷으로 버튼, 체크박스 등의 GUI 기능을 제공.
  - [GLFW](https://ko.wikipedia.org/wiki/OpenGL_FrameWork "wikilink") - OpenGL 응용 프로그램 개발을 위한 이식 가능한 프레임워크.
  - [GLM](https://ko.wikipedia.org/wiki/OpenGL_Mathematics "wikilink") - GLSL 규격에 기반한 OpenGL을 위한 C++ 수학 툴킷.
  - [SFML](https://ko.wikipedia.org/wiki/Simple_and_Fast_Multimedia_Library "wikilink") - 간단하고 빠른 멀티미디어 라이브러리.
  - [Glux](https://ko.wikipedia.org/wiki/OpenGL_Utility_&_Auxiliary_Toolkit "wikilink") - OpenGL 유틸리티 및 보조 라이브러리.

### 기타 3D 그래픽스 API

  - [Mesa 3D](https://ko.wikipedia.org/wiki/Mesa_3D "wikilink") - OpenGL의 공개소스 판.
  - [VirtualGL](https://ko.wikipedia.org/wiki/VirtualGL "wikilink") - 원격지 X 서버로 렌더링된 이미지를 보내주는 OpenGL 3D 모델 서버.
  - [Direct3D](../Page/Direct3D.md "wikilink") - [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")사에서 개발한 OpenGL의 대항 API.
  - [RISpec](https://ko.wikipedia.org/wiki/RenderMan_Interface_Specification "wikilink") - [픽사](https://ko.wikipedia.org/wiki/픽사 "wikilink")에서 개발한 실사 오프라인 렌더링을 위한 공개 API.

### 기타 2D 그래픽스 API

  - [카이로](https://ko.wikipedia.org/wiki/카이로_\(그래픽스\) "wikilink") - 여러 운영체제에서 사용할 수 있는 벡터 그래픽 툴킷.
  - [GTK+](https://ko.wikipedia.org/wiki/GTK+ "wikilink") - 여러 운영체제에서 사용할 수 있는 그래픽 위젯 툴킷.
  - [Qt](https://ko.wikipedia.org/wiki/Qt_\(프레임워크\) "wikilink") - 여러 운영체제에서 사용할 수 있는 그래픽 위젯 툴킷.
  - [wxWidgets](https://ko.wikipedia.org/wiki/wxWidgets "wikilink") - 여러 운영체제에서 사용할 수 있는 그래픽 위젯 툴킷.

## 벌컨

과거 이름이 "Next Generation OpenGL Initiative"(glNext)이었던 벌칸(Vulkan)은\[13\]\[14\] OpenGL과 OpenGL ES를 기존 OpenGL 버전들과 하위 호환되지 않는 하나의 공통된 API로 통합하려는 재설계적 일환이다.\[15\]\[16\]\[17\]

벌컨 API의 최초 버전은 2016년 2월 16일에 출시되었다.

## 각주

## 외부 링크

  - [공식 사이트](http://www.opengl.org/)

  - [Neon Helium](https://web.archive.org/web/20071126072642/http://nehe.gamedev.net/) - OpenGL 설명서, 약칭 NeHe.

  - [CodeSampler.com](https://web.archive.org/web/20060116010741/http://www.codesampler.com/oglsrc.htm) - OpenGL 게임 프로그래밍 코드 예제 및 설명서.

  - [OpenGL 디렉터리](https://web.archive.org/web/20060409135741/http://www.pzeta.org/opengl/) - OpenGL를 위한 자원과 링크의 비교

  - [표준 OpenGL 광원의 해석](http://www.sjbaker.org/steve/omniv/opengl_lighting.html)

  - [Blender](http://blender3d.org/) - OpenGL을 이용한 오픈소스 3D 모델링 소프트웨어.

  -
[OpenGL](https://ko.wikipedia.org/wiki/분류:OpenGL "wikilink") [분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink") [분류:3차원 컴퓨터 그래픽스](https://ko.wikipedia.org/wiki/분류:3차원_컴퓨터_그래픽스 "wikilink") [분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:1992년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1992년_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12. <https://www.khronos.org/registry/OpenGL/specs/gl/GLSLangSpec.4.60.pdf>
13.
14.
15.
16.
17.