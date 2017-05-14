#
#GLComputeHelper lib
#

set(GLHelperSrc
	GLComputeHelper/Context.cpp
	GLComputeHelper/ComputeShader.cpp
	GLComputeHelper/Util.cpp
	GLComputeHelper/ShaderImage.cpp
	GLComputeHelper/QuadImage.cpp
	GLComputeHelper/Texture.cpp
	GLComputeHelper/BufferTexture.cpp
)	

add_library(GLComputeHelper STATIC ${GLHelperSrc})

#link with gl specific libs
target_link_libraries(GLComputeHelper opengl32)
target_link_libraries(GLComputeHelper glew32s)
target_link_libraries(GLComputeHelper glfw3)

