

图形渲染管线接受一组3D坐标，然后把它们转变为你屏幕上的有色2D像素输出。

图形渲染管线可以被划分为几个阶段，每个阶段将会把前一个阶段的输出作为输入。

所有这些阶段都是高度专门化的（它们都有一个特定的函数），并且很容易并行执行。

正是由于它们具有并行执行的特性，当今大多数显卡都有成千上万的小处理核心，它们在GPU上为每一个（渲染管线）阶段运行各自的小程序，从而在图形渲染管线中快速处理你的数据。

这些小程序叫做着色器(Shader)。


分为三种着色器：
- 顶点着色器
- 片元着色器
- 几何着色器




对于大多数场合，我们只需要配置顶点和片段着色器就行了。几何着色器是可选的，通常使用它默认的着色器就行了。


在现代OpenGL中，我们必须定义至少一个顶点着色器和一个片段着色器（因为GPU中没有默认的顶点/片段着色器）

