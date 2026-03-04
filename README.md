# CAD — Parametric Curve Theory & Implementation

Interactive Jupyter notebooks exploring parametric curve fundamentals used in Computer-Aided Design, implemented from scratch with **PyTorch** and **Matplotlib**.

## Notebooks

### [Bézier Curves](Bezier.ipynb)
A deep-dive into Bézier curves covering three equivalent formulations:

| Section | Description |
|---|---|
| **Bernstein Polynomial Form** | Constructs curves via weighted sums of Bernstein basis polynomials using binomial coefficients. Explains the relationship between control point count and curve degree. |
| **De Casteljau's Algorithm** | Builds the same curve through recursive linear interpolation (lerp). Numerically stable and widely used in shaders and animation engines. |
| **Matrix Bézier Form** | Expresses the curve as `P(t) = T · M · G` using the Bézier basis matrix. Discusses basis equivalence with Hermite curves, linear mapping of constraints, and geometric continuity. |

### [Hermite Curves](Hermite.ipynb)
Implementation of cubic Hermite curves using the matrix form `P(t) = T · M · G`, where:
- **G** — Geometry matrix: two endpoints (`P0`, `P1`) and two tangent vectors (`T0`, `T1`)
- **M** — Hermite basis matrix (4×4)
- **T** — Parameter power vector `[t³, t², t, 1]`

Includes derivation of the basis matrix and visualization of the resulting curve with control points.

### [B-Spline](B-Spline.ipynb)
*(Work in progress)*

## Tech Stack
- **Python 3.12**
- **PyTorch** — tensor operations and linear algebra
- **Matplotlib** — curve and control point visualization

## Getting Started

```bash
# Clone the repo
git clone https://github.com/prakharprasun/CAD.git
cd CAD

# Install dependencies
pip install torch matplotlib

# Launch notebooks
jupyter notebook
```

## License

[MIT](LICENSE) © 2026 Prakhar Prasun