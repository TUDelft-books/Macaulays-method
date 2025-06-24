# Lucas: Axial Force Analysis in SymPy

> In this report, the development and implementation of the new column module in SymPy is described.  
> This module models and solves for axial force problems in one-dimensional structural elements. This  
> implementation is based on Macaulay’s method, which uses singularity functions to express the Euler-  
> Bernoulli differential equations as a single piecewise expression. These functions are well-suited to  
> symbolic manipulation and integration within SymPy, a Python library for symbolic mathematics and  
> physics.  
>  
> The column module addresses a limitation in the existing Structure2D module, which is also part of  
> SymPy’s continuum mechanics framework. Structure2D enables modeling of two-dimensional structures  
> with members in both the x and y directions. Internally, these structures are ”unwrapped” into a  
> one-dimensional system. While a ’beam’ module is already used to solve for shear forces and bending  
> moments, axial force support in Structure2D is currently limited. Only one horizontal reaction force can  
> be solved, making use of a simple sum of horizontal loads. The column module provides the foundation  
> for extending this functionality to include symbolic treatment of multiple axial loads and reactions,  
> similar to how the beam module supports transversal loads.  
>  
> The column module can be used by initializing a column object with its length, elastic modulus and crosssectional  
> areas. Users can apply supports and loads, including distributed loads, as well as define  
> telescope hinges which allow discontinuities in displacement. The singularity functions of the supports,  
> loads and hinges are added to a continuous load equation. The unknowns in the load equation are  
> solved with force and deflection boundary conditions. At the supports, the deflection is zero and at the  
> hinges the axial force is zero. Due to the load expression needing to be integrated twice to solve for  
> displacements, two integration constants also have to be solved. The remaining equations are provided  
> by boundary conditions for absence of axial forces just outside of the element.  
>  
> The system of equations is solved symbolically using a linear solving function. The unknown forces  
> and displacements are automatically replaced into the load equation. From this solved load equation,  
> the singularity expressions for the axial force and deflection along the column can be set up and plotted.  
> The column module has been tested for multiple different use cases with different load types and  
> telescope hinges. The results have been compared with those from Matrixframe, showing that the they  
> are correct.  
>  
> While the current implementation offers core functionality for analyzing axially loaded elements, further  
> improvements can be made by developers in the future. These include enhancements such as  
> improved visualization, more flexible boundary conditions and inclusion of variable cross-sectional properties.  
> While the column module is a standalone feature, it should also be adjusted to comply with future  
> integration into the Structure2D module.

{cite:ts}`lucas_2025`

## Documenten
- [Report](./Bachelor's_Thesis_Lucas_Verlaan_5876001.pdf)
- [GitHub repository](https://github.com/lfverlaan/BEP-Use-Cases), examples also shown in this book.