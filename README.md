CG-textureRenderer
==================

Load a specific ppm-format texture file ("texture") that is applied to every triangle of the 3D model and perform perspective correction.

* A data set ppot.asc contains a teapot sitting on a plane.

* Texture parameter that is passed to the renderer is a pointer to a function.  

* tex_fun.skel is used to build our own texture functions (adding bilinear interpolation and bounds checking) for image textures. 

* Renderer performs the perspective correction for u,v parameter interpolation.

* Supports texturing with Phong shading and Gouraud shading.  

* Gouraud shading : 

1. Texture color is treated as Ka, Kd, and Ks. 
2. That allows you to simply interpolate the light and geometry-dependent coefficients of the shading equation

* Phong shading : 

1. Texture color is treated as Ka and Kd.  
2. Ks - the specular parameter is allowed to remain as defined by the renderer state.  

* Method "ptex_fun()" : Procedural texture function.  