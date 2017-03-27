#
#GLComputeHelper lib
#

set(GLHelperSrc
	Context.cpp
	ComputeShader.cpp
	Util.cpp
	ShaderImage.cpp
	QuadImage.cpp
	Texture.cpp
	BufferTexture.cpp
)	

add_library(GLComputeHelper STATIC ${GLHelperSrc})

#link with gl specific libs
target_link_libraries(GLComputeHelper opengl32)
target_link_libraries(GLComputeHelper glew32s)
target_link_libraries(GLComputeHelper glfw3)

