# Borek: 2D Structural Analysis Tool in SymPy

> This report describes the development of a Python based tool for 2D structural analysis in civil engineering, using the SymPy library (Meurer A, 2017) and applying the Macaulay method (Macaulay, 1919) to enable symbolic computation for structural analysis. The tool serves as a proof of concept demonstrating the feasibility of symbolic computation in analyzing internal forces.
>
> Central to the project is the extension of existing SymPy modules, specifically the Beam module, to support 2D analysis by introducing new modules: "Column" and "Structure2D." The existing "Beam" module in SymPy, which computes vertical load effects, was used to handle shear forces and bending moments by creating a load equation for the vertical direction. To handle normal forces a "Column" module was proposed (although not implemented in this iteration), designed to compute horizontal load effects based on the material’s elasticity modulus, length, and cross-sectional area. The "Structure2D" module integrates both vertical and horizontal load computations by transforming a 2D structure into two corresponding 1D representations. This method enables separate computations for each direction, converting 2D problems into simpler 1D computations while preserving load and support behavior.
>
> The tool’s workflow involves users defining structure components (members, loads, supports) on a 2D grid. Once defined, the structure is "unwrapped" to map each member along a continuous line. Each load is split into its horizontal and vertical components and applied to the corresponding axis. Through examples, the report showcases the tool’s ability to calculate shear forces, bending moments, and reaction loads.
>
> Although the project successfully demonstrates the potential of symbolic computation for 2D structural analysis, several limitations exist. The tool currently lacks a functional Column module, restricting it to single horizontal reaction loads and limiting its ability to solve for horizontal deflections and axial forces fully. Additionally, the structure must be non-branching and linear, excluding complex configurations like truss networks. Material properties must be uniform across members, a constraint that simplifies the model but limits its real-world applicability. Addressing these limitations would involve developing a more advanced unwrapping algorithm for intersecting members and introducing a complete Column module.
>
> In summary, this prototype validates the possibility of a symbolic 2D structural analysis tool, providing civil engineering students and educators with an analytical framework that combines Macaulay’s method and modern symbolic computation. This tool lays the groundwork for future developments that could expand its functionality, to move away from proof of concept to a fully featured open-source product.

{cite:ts}`borek_2024`

## Documenten
- [TU Delft repository](https://resolver.tudelft.nl/uuid:e4961d2e-230f-419c-9a15-545ff0f049f8)
- [GitHub repository](https://github.com/BorekSaheli/sympy/tree/structure2d), example as in report shown in this [book](./borek_example.ipynb)