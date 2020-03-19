<p align="center">
  <img src="picture/_.jpg">
</p>
Surface Remesher remeshes a surface mesh using the centroidal Voronoi tessellation. The input is a triangulated surface mesh. We first cut the surface into a topological disk, then parameterize it in a planar space. We compute the centroidal Voronoi tessellation (CVT) in the parameter space with respect to a density distribution, and construct the constrained Delaunay triangulation (CDT) from the resulted CVT. The final optimized surface mesh is then obtained from the CDT.

---

We use the following packages:

1. [CGAL 5.0.2](https://www.cgal.org) to store the mesh structure, and
2. with [Eigen 3.3.7](http://eigen.tuxfamily.org) to parameterize the surface mesh;
3. [gCVT](https://www.comp.nus.edu.sg/~tants/cvt.html) to compute the centroidal Voronoi tessellation on the GPU;
4. [gDel2D](https://www.comp.nus.edu.sg/~tants/gdel3d.html) to compute the constrained Delaunay triangulation on the GPU;
5. [OpenGL](https://www.opengl.org/) and [OpenCV](https://opencv.org/) to visualize the results.

Please preinstall CGAL and Eigen, and compile it as a CUDA project if you want to use.

---

1. [Jiaqi Zheng and Tiow-Seng Tan. 2020. Computing Centroidal Voronoi Tessellation Using the GPU. In Symposium on Interactive 3D Graphics and Games (I3D ’20), May 5–7, 2020, San Francisco, CA, USA.](https://doi.org/10.1145/3384382.3384520)
2. [Pierre Alliez, Éric Colin de Verdière, Olivier Devillers, and Martin Isenburg. 2005. Centroidal Voronoi Diagrams for Isotropic Surface Remeshing. Graphical Models, Elsevier, 2005, 67 (3), pp.204-231.](https://hal.inria.fr/hal-00787166)
3. [Meng Qi, Thanh-Tung Cao, and Tiow-Seng Tan. 2012. Computing 2D Constrained Delaunay Triangulation Using the GPU. In Proceedings of the ACM SIGGRAPH Symposium on Interactive 3D Graphics and Games (I3D ’12).](https://doi.org/10.1145/2159616.2159623)
4. [Qingnan Zhou and Alec Jacobson. 2016. Thingi10K: A Dataset of 10,000 3D-Printing Models. arXiv:1605.04797.](https://ten-thousand-models.appspot.com/)
