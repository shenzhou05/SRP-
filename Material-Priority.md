HDRP uses Material rendering priority settings to sort transparent GameObjects.

The built-it Unity render pipeline sorts GameObjects according to their **Rendering Mode** and render queue. HDRP uses the render queue in a different way, in that HDRP Materials do not expose the render queue directly. Instead, Materials with a **Transparent Surface Type** have a **Sort Priority** property:

![](https://github.com/Unity-Technologies/ScriptableRenderPipeline/wiki/Pages/HDRP/Images/MaterialRenderingPriority1.png)

HDRP uses this priority to offset sorting inside a particular GameObject group (opaques, transparency). HDRP renders smaller values first.