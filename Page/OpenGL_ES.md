> This article is converted from Wikipedia: [OpenGL ES](https://ko.wikipedia.org/wiki/OpenGL_ES).


**OpenGL ES** (임베디드 시스템을 위한 OpenGL)는 [크로노스 그룹이](https://ko.wikipedia.org/wiki/크로노스_그룹 "wikilink") 정의한 3차원 컴퓨터 그래픽스 API인 OpenGL의 서브셋으로, 휴대전화, PDA 등과 같은 임베디드 시스템을 위한 API이다.

## 이용

OpenGL ES 1.0 은 [심비안 OSs](https://ko.wikipedia.org/wiki/심비안_OS "wikilink")60v5와 [안드로이드 플랫폼의](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink") 공식 3D 그래픽 [API](../Page/API.md "wikilink")로 채택되었다.

OpenGL ES 1.0 그리고 2.0의 일부 기능과 [Cg는](https://ko.wikipedia.org/wiki/CG "wikilink") [플레이스테이션 3의](https://ko.wikipedia.org/wiki/플레이스테이션_3 "wikilink") 공식 그래픽 API 중 하나로 지원된다.

OpenGL ES 1.1 은 [아이폰](../Page/아이폰.md "wikilink") SDK의 3D 라이브러리 중 하나이다.

OpenGL ES 1.0 과 1.1 은 블랙베리 5.0 운영체제에서 지원된다. 현재 BlackBerry Storm 2와 BlackBerry Curve 8530만이 OpenGL ES 1.x을 하드웨어적으로 지원

OpenGL ES 2.0은 [WebGL](https://ko.wikipedia.org/wiki/WebGL "wikilink") (OpenGL for browser) 에서 사용된다. 2007년 3월에 공개 되었다.\[1\] OpenGL ES 2.0은 OpenGL ES 1.1과 [하위 호환성이](../Page/하위_호환성.md "wikilink") 제공 되지 않는다.

노키아 [심비안OS](https://ko.wikipedia.org/wiki/심비안OS "wikilink")^3 과 마에모 기반의 노키아N900에도 지원된다.

[미고](https://ko.wikipedia.org/wiki/미고 "wikilink")os의 공식 API로 채택되었다.

[블랙베리 OS](https://ko.wikipedia.org/wiki/블랙베리_OS "wikilink")7, 블랙베리10 및 블랙베리 플레이북

[아이폰](../Page/아이폰.md "wikilink") SDK(아이폰 3GS와 아이팟 터치3세대 및 그 이후모델을 지원한다)의 3D 라이브러리 중 하나이다

판도라 콘솔의 3D 라이브러리로 사용되고있다.

iOS 7.0 부터 OpenGL ES 3.0 를 지원한다.

[안드로이드 플랫폼의](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink") 경우

1.0 버전부터 OpenGL ES 1.0 와 1.1를 지원하며,

2.2 버전(froyo) 부터 OpenGL ES 2.0 를 지원하고,

4.3 버전(jellybean mr2) 부터 OpenGL ES 3.0 를 지원한다.

파이어폭스에 사용되는 [게코 (레이아웃 엔진)](https://ko.wikipedia.org/wiki/게코_\(레이아웃_엔진\) "wikilink") 1.9.3a1 부터 [WebGL](https://ko.wikipedia.org/wiki/WebGL "wikilink")을 통해서 지원되고 있다.\[2\]

## 버전

### OpenGL ES 1.0

| 확장 이름                                                                                                                               | 정렬 \#번호                  | 상세 내용                             |
| ----------------------------------------------------------------------------------------------------------------------------------- | ------------------------ | --------------------------------- |
| [OES_byte_coordinates](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_byte_coordinates.txt)                           | OpenGL ES Extension \#4  | (formerly OpenGL Extension \#291) |
| [OES_compressed_paletted_texture](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_compressed_paletted_texture.txt)    | OpenGL ES Extension \#6  | (formerly OpenGL Extension \#294) |
| [OES_fixed_point](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_fixed_point.txt)                                     | OpenGL ES Extension \#9  | (formerly OpenGL Extension \#292) |
| [OES_query_matrix](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_query_matrix.txt)                                   | OpenGL ES Extension \#16 | (formerly OpenGL Extension \#296) |
| [OES_read_format](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_read_format.txt)                                     | OpenGL ES Extension \#17 | (formerly OpenGL Extension \#295) |
| [OES_single_precision](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_single_precision.txt)                           | OpenGL ES Extension \#18 | (formerly OpenGL Extension \#293) |
|                                                                                                                                     | optional                 | Mesa (all drivers)                |
| [OES_compressed_ETC1_RGB8_texture](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_compressed_ETC1_RGB8_texture.txt) | OpenGL ES Extension \#5  |                                   |

### OpenGL ES 1.1

| 확장 이름                                                                                                                   | Sort \#Number              |
| ----------------------------------------------------------------------------------------------------------------------- | -------------------------- |
| [OES_draw_texture](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_draw_texture.txt)                       | OpenGL ES Extension \#7    |
| [OES_matrix_get](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_matrix_get.txt)                           | OpenGL ES Extension \#11   |
| [OES_point_size_array](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_point_size_array.txt)              | OpenGL ES Extension \#14   |
| [OES_point_sprite](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_point_sprite.txt)                       | OpenGL ES Extension \#15   |
| optional                                                                                                                | Mesa (all drivers)         |
| [OES_EGL_image](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_EGL_image.txt)                             | OpenGL ES Extension \#23   |
| [OES_EGL_image_external](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_EGL_image_external.txt)          | OpenGL ES Extension \#87   |
| [OES_required_internalformat](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_required_internalformat.txt) | OpenGL ES Extension \# TBD |

### OpenGL ES 2.0

| 확장 이름                                                                                                                                        | Sort \#Number                                |
| -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- |
| [OES_texture_cube_map](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_texture_cube_map.txt)                                   | OpenGL ES Extension \#20                     |
| [OES_texture_npot](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_texture_npot.txt)                                            | OpenGL ES Extension \#37                     |
| [OES_depth24](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_depth24.txt)                                                       | OpenGL ES Extension \#24                     |
| [OES_depth_texture](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_depth_texture.txt)                                          | OpenGL ES Extension \#44                     |
| [OES_element_index_uint](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_element_index_uint.txt)                               | OpenGL ES Extension \#26                     |
| [OES_fbo_render_mipmap](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_fbo_render_mipmap.txt)                                 | OpenGL ES Extension \#27                     |
| [OES_get_program_binary](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_get_program_binary.txt)                               | OpenGL ES Extension \#47                     |
| [OES_mapbuffer](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_mapbuffer.txt)                                                   | OpenGL ES Extension \#29                     |
| [OES_packed_depth_stencil](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_packed_depth_stencil.txt)                           | OpenGL ES Extension \#43                     |
| [OES_rgb8_rgba8](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_rgb8_rgba8.txt)                                                | OpenGL ES Extension \#30                     |
| [OES_stencil8](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_stencil8.txt)                                                     | OpenGL ES Extension \#33                     |
| [OES_vertex_half_float](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_vertex_half_float.txt)                                 | OpenGL ES Extension \#38                     |
| additional                                                                                                                                   | in MESA (all drivers)                        |
| [OES_EGL_image](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_EGL_image.txt)                                                  | OpenGL ES Extension \#23 (different for 1.1) |
| [OES_EGL_image_external](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_EGL_image_external.txt)                               | OpenGL ES Extension \#87 (different for 1.1) |
| [OES_texture_float](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_texture_float.txt)                                          | OpenGL ES Extension \#36                     |
| [OES_standard_derivatives](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_standard_derivatives.txt)                            | OpenGL ES Extension \#45                     |
| [OES_surfaceless_context](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_surfaceless_context.txt)                              | OpenGL ES Extension \#116                    |
| [OES_depth_texture_cube_map](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_depth_texture_cube_map.txt)                      | OpenGL ES Extension \#136                    |
| [EXT_texture_filter_anisotropic](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_filter_anisotropic.txt)               | OpenGL ES Extension \#41                     |
| [EXT_texture_type_2_10_10_10_REV](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_type_2_10_10_10_REV.txt)         | OpenGL ES Extension \#42                     |
| [EXT_texture_compression_dxt1](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_compression_dxt1.txt)                   | OpenGL ES Extension \#49                     |
| [EXT_texture_format_BGRA8888](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_format_BGRA8888.txt)                     | OpenGL ES Extension \#51                     |
| [EXT_discard_framebuffer](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_discard_framebuffer.txt)                              | OpenGL ES Extension \#64                     |
| [EXT_blend_minmax](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_blend_minmax.txt)                                            | OpenGL ES Extension \#65                     |
| [EXT_read_format_bgra](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_read_format_bgra.txt)                                   | OpenGL ES Extension \#66                     |
| [EXT_multi_draw_arrays](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_multi_draw_arrays.txt)                                 | OpenGL ES Extension \#69                     |
| [EXT_frag_depth](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_frag_depth.txt)                                                | OpenGL ES Extension \#86                     |
| [EXT_unpack_subimage](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_unpack_subimage.txt)                                      | OpenGL ES Extension \#90                     |
| [EXT_texture_rg](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_rg.txt)                                                | OpenGL ES Extension \#103                    |
| [EXT_draw_buffers](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_draw_buffers.txt)                                            | OpenGL ES Extension \#151                    |
| [EXT_compressed_ETC1_RGB8_sub_texture](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_compressed_ETC1_RGB8_sub_texture.txt) | OpenGL ES Extension \#188                    |
| [NV_draw_buffers](https://www.khronos.org/registry/OpenGL/extensions/NV/NV_draw_buffers.txt)                                               | OpenGL ES Extension \#91                     |
| [NV_fbo_color_attachments](https://www.khronos.org/registry/OpenGL/extensions/NV/NV_fbo_color_attachments.txt)                            | OpenGL ES Extension \#92                     |
| [NV_read_buffer](https://www.khronos.org/registry/OpenGL/extensions/NV/NV_read_buffer.txt)                                                 | OpenGL ES Extension \#93                     |
| [NV_read_depth_stencil](https://www.khronos.org/registry/OpenGL/extensions/NV/NV_read_depth_stencil.txt)                                  | OpenGL ES Extension \#94                     |
| [ANGLE_texture_compression_dxt](https://www.khronos.org/registry/OpenGL/extensions/ANGLE/ANGLE_texture_compression_dxt.txt)               | OpenGL ES Extension \#111                    |

### OpenGL ES 3.0

| 확장 이름                                                                                                                         | 정렬 \#번호                   | 상세 내용                                       |
| ----------------------------------------------------------------------------------------------------------------------------- | ------------------------- | ------------------------------------------- |
| [OES_vertex_array_object](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_vertex_array_object.txt)              | OpenGL ES Extension \#71  |                                             |
| [KHR_context_flush_control](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_context_flush_control.txt)          | OpenGL ES Extension \#191 | (for GL_KHR_context_flush_control only) |
| additional                                                                                                                    | in MESA (all drivers)     |                                             |
| [EXT_texture_sRGB_decode](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_sRGB_decode.txt)              | OpenGL ES Extension \#152 | OpenGL Extension \#402                      |
| [EXT_texture_border_clamp](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_texture_border_clamp.txt)            | OpenGL ES Extension \#182 |                                             |
| [EXT_draw_elements_base_vertex](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_draw_elements_base_vertex.txt) | OpenGL ES Extension \#204 |                                             |
| [MESA_shader_integer_functions](https://www.khronos.org/registry/OpenGL/extensions/MESA/MESA_shader_integer_functions.txt) | OpenGL ES Extension \#495 |                                             |

### OpenGL ES 3.1

| 확장 이름                                                                                                                               | Sort \#Number                     |
| ----------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| [ARB_arrays_of_arrays](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_arrays_of_arrays.txt)                          | ARB Extension \#120               |
| [ARB_compute_shader](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_compute_shader.txt)                               | ARB Extension \#122               |
| [ARB_explicit_uniform_location](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_explicit_uniform_location.txt)        | ARB Extension \#128               |
| [ARB_framebuffer_no_attachments](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_framebuffer_no_attachments.txt)      | ARB Extension \#130               |
| [ARB_program_interface_query](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_program_interface_query.txt)            | ARB Extension \#134               |
| [ARB_shader_atomic_counters](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_atomic_counters.txt)              | ARB Extension \#114               |
| [ARB_shader_image_load_store](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_image_load_store.txt)           | ARB Extension \#115               |
| [ARB_shader_storage_buffer_object](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_storage_buffer_object.txt) | ARB Extension \#137               |
| [ARB_separate_shader_objects](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_separate_shader_objects.txt)            | ARB Extension \#97                |
| [ARB_stencil_texturing](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_stencil_texturing.txt)                         | ARB Extension \#138               |
| [ARB_vertex_attrib_binding](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_vertex_attrib_binding.txt)                | ARB Extension \#125               |
| [ARB_draw_indirect](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_draw_indirect.txt)                                 | ARB Extension \#87                |
| [ARB_shading_language_packing](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shading_language_packing.txt)          | ARB Extension \#116               |
| [ARB_shader_image_size](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_shader_image_size.txt)                        | ARB Extension \#136               |
| [ARB_texture_storage_multisample](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_storage_multisample.txt)    | ARB Extension \#141               |
| [ARB_texture_multisample](https://www.khronos.org/registry/OpenGL/extensions/ARB/ARB_texture_multisample.txt)                     | ARB Extension \#67                |
| [EXT_shader_integer_mix](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_shader_integer_mix.txt)                      | OpenGL ES Extension \#161         |
| optional                                                                                                                            | Mesa (all drivers OpenGL ES 3.1+) |
| [OES_texture_view](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_texture_view.txt)                                   | OpenGL ES Extension \#218         |
| [NV_image_formats](https://www.khronos.org/registry/OpenGL/extensions/NV/NV_image_formats.txt)                                    | OpenGL ES Extension \#200         |

### OpenGL ES 3.2

| 확장 이름                                                                                                                                                | 정렬 \#번호                                         |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| [KHR_blend_equation_advanced](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_blend_equation_advanced.txt)                             | OpenGL ES Extension \#168                       |
| [EXT_color_buffer_float](https://www.khronos.org/registry/OpenGL/extensions/EXT/EXT_color_buffer_float.txt)                                       | OpenGL ES Extension \#137                       |
| [KHR_debug](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_debug.txt)                                                                   | OpenGL ES Extension \#118                       |
| [KHR_robustness](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_robustness.txt)                                                         | OpenGL ES Extension \#190                       |
| [OES_copy_image](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_copy_image.txt)                                                        | OpenGL ES Extension \#208                       |
| [OES_draw_buffers_indexed](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_draw_buffers_indexed.txt)                                   | OpenGL ES Extension \#209                       |
| [OES_draw_elements_base_vertex](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_draw_elements_base_vertex.txt)                        | OpenGL ES Extension \#219                       |
| [OES_geometry_shader](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_geometry_shader.txt)                                              | OpenGL ES Extension \#210                       |
| [OES_gpu_shader5](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_gpu_shader5.txt)                                                      | OpenGL ES Extension \#211                       |
| [OES_sample_shading](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_sample_shading.txt)                                                | OpenGL ES Extension \#169                       |
| [OES_sample_variables](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_sample_variables.txt)                                            | OpenGL ES Extension \#170                       |
| [OES_shader_image_atomic](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_shader_image_atomic.txt)                                     | OpenGL ES Extension \#171                       |
| [OES_shader_io_blocks](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_shader_io_blocks.txt)                                           | OpenGL ES Extension \#213                       |
| [OES_shader_multisample_interpolation](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_shader_multisample_interpolation.txt)           | OpenGL ES Extension \#172                       |
| [OES_tessellation_shader](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_tessellation_shader.txt)                                      | OpenGL ES Extension \#214                       |
| [OES_texture_border_clamp](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_texture_border_clamp.txt)                                   | OpenGL ES Extension \#215                       |
| [OES_texture_buffer](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_texture_buffer.txt)                                                | OpenGL ES Extension \#216                       |
| [OES_texture_cube_map_array](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_texture_cube_map_array.txt)                              | OpenGL ES Extension \#217                       |
| [OES_texture_stencil8](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_texture_stencil8.txt)                                            | OpenGL ES Extension \#173                       |
| [OES_texture_storage_multisample_2d_array](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_texture_storage_multisample_2d_array.txt) | OpenGL ES Extension \#174                       |
| [KHR_texture_compression_astc_ldr](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_texture_compression_astc_hdr.txt)                  | OpenGL ES Extension \#117 (LDR only)            |
| [OES_primitive_bounding_box](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_primitive_bounding_box.txt)                               | OpenGL ES Extension \#212                       |
| optional                                                                                                                                             | Mesa (all drivers OpenGL ES 3.2+)               |
|                                                                                                                                                      |                                                 |
| [KHR_texture_compression_astc_hdr](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_texture_compression_astc_hdr.txt)                  | OpenGL ES Extension \#117 (LDR included)        |
| [KHR_blend_equation_advanced_coherent](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_blend_equation_advanced.txt)                   | OpenGL ES Extension \#168                       |
| [KHR_texture_compression_astc_sliced_3d](https://www.khronos.org/registry/OpenGL/extensions/KHR/KHR_texture_compression_astc_sliced_3d.txt)     | OpenGL ES Extension \#249 (ARB Extension \#189) |
| [OES_viewport_array](https://www.khronos.org/registry/OpenGL/extensions/OES/OES_viewport_array.txt)                                                | OpenGL ES Extension \#267                       |

## 같이 보기

  - [OpenGL](https://ko.wikipedia.org/wiki/OpenGL "wikilink")

## 각주

## 외부 링크

  - [공식 사이트](http://www.khronos.org/opengles/)

[분류:OpenGL](https://ko.wikipedia.org/wiki/분류:OpenGL "wikilink") [분류:3차원 컴퓨터 그래픽스](https://ko.wikipedia.org/wiki/분류:3차원_컴퓨터_그래픽스 "wikilink")

1.
2.  [WebGL - MDC](https://developer.mozilla.org/en/WebGL)