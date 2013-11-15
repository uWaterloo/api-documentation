# Subject Listings

```
GET /courses/{subject}.{format}
```

## Description

> This method returns all the coures offered under a given subject

## Summary

<table>
  <tr>
    <td><b>Name</b></td>
    <td><b>Value</b></td>
    <td><b><b>Name</b></b></td>
    <td><b>Value</b></td>
  </tr>
  <tr>
    <td><b>Request Protocol</b></td>
    <td>GET</td>
    <td><b>Requires API Key</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Method ID</b></td>
    <td>1439</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>courses</td>
    <td><b>Service ID</b></td>
    <td>239</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Registrar</td>
    <td><b>Data Type</b></td>
    <td>Scraped</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every request (live)</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources

- http://ugradcalendar.uwaterloo.ca/
- http://gradcalendar.uwaterloo.ca/


## Parameters

```
GET /courses/{subject}.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>subject</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Valid uWaterloo subject name</td>
  </tr>
  <tr>
    <td><b>format</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>The format of the output</td>
  </tr>
  <tr>
    <td><b>key</b></td>
    <td>filter</td>
    <td><i>yes</i></td>
    <td>Valid API key</td>
  </tr>
  <tr>
    <td><b>callback</b></td>
    <td>filter</td>
    <td><i>no</i></td>
    <td>JSONP callback format</td>
  </tr>
</table>

**Output Formats**

- json
- xml


## Examples

```
GET /courses/{subject}.{format}
```

- **https://api.uwaterloo.ca/v2/courses/MATH.json**
- **https://api.uwaterloo.ca/v2/courses/MATH.xml**
- **https://api.uwaterloo.ca/v2/courses/MATH.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>course_id</b></td>
    <td>string</td>
    <td>Registrar assigned course ID</td>
  </tr>
  <tr>
    <td><b>subject</b></td>
    <td>string</td>
    <td>Requested subject acronym</td>
  </tr>
  <tr>
    <td><b>catalog_number</b></td>
    <td>string</td>
    <td>Registrar assigned class number</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Class name and title</td>
  </tr>
  <tr>
    <td><b>units</b></td>
    <td>number</td>
    <td>Credit count for the mentioned course</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Brief course description</td>
  </tr>
  <tr>
    <td><b>academic_level</b></td>
    <td>string</td>
    <td>Undergraduate or graduate course classification</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":300,
    "timestamp":1384535133,
    "status":200,
    "message":"Request successful",
    "method_id":1439,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "course_id":"010374",
      "subject":"MATH",
      "catalog_number":"51",
      "title":"Pre-University Algebra and Geometry",
      "units":0,
      "description":"Topics covered in the course include operations with vectors, scalar multiplications dot and cross products, projections, equations of lines and planes, systems of equations, Gaussian elimination, operations with matrices, determinants, binomial theorem, proof by mathematical induction, complex numbers.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"010375",
      "subject":"MATH",
      "catalog_number":"52",
      "title":"Pre-University Calculus",
      "units":0,
      "description":"The concepts included are limits, derivatives, antiderivatives and definite integrals. These concepts will be applied to solve problems of rates of change, maximum and minimum, curve sketching and areas. The classes of functions used to develop these concepts and applications are: polynomial, rational, trigonometric, exponential and logarithmic.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"010113",
      "subject":"MATH",
      "catalog_number":"97",
      "title":"Study Abroad",
      "units":2.5,
      "description":"For studies at other universities under approved exchange agreements.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006847",
      "subject":"MATH",
      "catalog_number":"103",
      "title":"Introductory Algebra for Arts and Social Science",
      "units":0.5,
      "description":"An introduction to applications of algebra to business, the behavioural sciences, and the social sciences. Topics will be chosen from set theory, permutations and combinations, binomial theorem, probability theory, systems of linear equations, vectors and matrices, mathematical induction. [Offered: F,W,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006848",
      "subject":"MATH",
      "catalog_number":"104",
      "title":"Introductory Calculus for Arts and Social Science",
      "units":0.5,
      "description":"An introduction to applications of calculus in business, the behavioural sciences, and the social sciences. The models studied will involve polynomial, rational, exponential and logarithmic functions. The major concepts introduced to solve problems are rate of change, optimization, growth and decay, and integration. [Offered: F,W]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006869",
      "subject":"MATH",
      "catalog_number":"106",
      "title":"Applied Linear Algebra 1",
      "units":0.5,
      "description":"Systems of linear equations. Matrix algebra. Determinants. Introduction to vector spaces. Applications. [Offered: F,W,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006853",
      "subject":"MATH",
      "catalog_number":"109",
      "title":"Mathematics for Accounting",
      "units":0.5,
      "description":"Review and extension of differential calculus for functions of one variable. Multivariable differential calculus. Partial derivatives, the Chain Rule, maxima and minima and Lagrange multipliers. Introduction to matrix algebra.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"011645",
      "subject":"MATH",
      "catalog_number":"114",
      "title":"Linear Algebra for Science",
      "units":0.5,
      "description":"Vectors in 2- and 3-space and their geometry. Linear equations, matrices and determinants. Introduction to vector spaces. Eigenvalues and diagonalization. Applications. Complex numbers. [Offered: F]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006862",
      "subject":"MATH",
      "catalog_number":"115",
      "title":"Linear Algebra for Engineering",
      "units":0.5,
      "description":"Linear equations, matrices and determinants. Introduction to vector spaces. Eigenvalues and diagonalization. Applications. Complex numbers. [Offered: F]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006865",
      "subject":"MATH",
      "catalog_number":"116",
      "title":"Calculus 1 for Engineering",
      "units":0.5,
      "description":"Functions: review of polynomials, exponential, logarithmic, trigonometric. Operations on functions, curve sketching. Trigonometric identities, inverse functions. Derivatives, rules of differentiation. Mean Value Theorem, Newton's Method. Indeterminate forms and L'Hopital's rule, applications. Integrals, approximations, Riemann definite integral, Fundamental Theorems. Applications of the integral. [Offered: F]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006866",
      "subject":"MATH",
      "catalog_number":"117",
      "title":"Calculus 1 for Engineering",
      "units":0.5,
      "description":"Functions of engineering importance; review of polynomial, exponential, and logarithmic functions; trigonometric functions and identities. Inverse functions (logarithmic and trigonometric). Limits and continuity. Derivatives, rules of differentiation; derivatives of elementary functions. Applications of the derivative, max-min problems, Mean Value Theorem. Antiderivatives, the Riemann definite integral, Fundamental Theorems. Methods of integration, approximation, applications, improper integrals. [Offered: F]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006867",
      "subject":"MATH",
      "catalog_number":"118",
      "title":"Calculus 2 for Engineering",
      "units":0.5,
      "description":"Methods of integration: by parts, trigonometric substitutions, partial fractions; engineering applications, approximation of integrals, improper integrals. Linear and separable first order differential equations, applications. Parametric curves and polar coordinates, arc length and area. Infinite sequences and series, convergence tests, power series and applications. Taylor polynomials and series, Taylor's Remainder Theorem, applications. [Offered: W,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006868",
      "subject":"MATH",
      "catalog_number":"119",
      "title":"Calculus 2 for Engineering",
      "units":0.5,
      "description":"Elementary approximation methods: interpolation; Taylor polynomials and remainder; Newton's method, Landau order symbol, applications. Infinite series: Taylor series and Taylor's Remainder Theorem, geometric series, convergence test, power series, applications. Functions of several variables: partial derivatives, linear approximation and differential, gradient and directional derivative, optimization and Lagrange multipliers. Vector-valued functions: parametric representation of curves, tangent and normal vectors, line integrals and applications. [Offered: W,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"012879",
      "subject":"MATH",
      "catalog_number":"124",
      "title":"Calculus and Vector Algebra for Kinesiology",
      "units":0.5,
      "description":"Review of trigonometry and basic algebra. Introduction to vectors in 2- and 3-space: sums, addition, dot products, cross products and angles between vectors. Solving linear systems in two and three variables. Functions of a real variable: powers, rational functions, trigonometric, exponential and logarithmic functions, their properties. Intuitive discussion of limits and continuity. Derivatives of elementary functions, derivative rules; applications to curve sketching, optimization. Relationships between distance, velocity and acceleration. The definite integral, antiderivatives, the Fundamental Theorem of Calculus; change of variable and integration by parts; applications to area, centre of mass. [Offered: F]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006871",
      "subject":"MATH",
      "catalog_number":"127",
      "title":"Calculus 1 for the Sciences",
      "units":0.5,
      "description":"Functions of a real variable: powers, rational functions, trigonometric, exponential and logarithmic functions, their properties and inverses. Intuitive discussion of limits and continuity. Definition and interpretation of the derivative, derivatives of elementary functions, derivative rules and applications. Riemann sums and other approximations to the definite integral. Fundamental Theorems and antiderivatives; change of variable. Applications to area, rates, average value. [Offered: F,W,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006872",
      "subject":"MATH",
      "catalog_number":"128",
      "title":"Calculus 2 for the Sciences",
      "units":0.5,
      "description":"Transforming and evaluating integrals; application to volumes and arc length; improper integrals. Separable and linear first order differential equations and applications. Introduction to sequences. Convergence of series; Taylor polynomials, Taylor's Remainder Theorem, Taylor series and applications. Parametric\/vector representation of curves; particle motion and arc length. Polar coordinates in the plane. [Offered: F,W,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006878",
      "subject":"MATH",
      "catalog_number":"135",
      "title":"Algebra for Honours Mathematics",
      "units":0.5,
      "description":"An introduction to the language of mathematics and proof techniques through a study of the basic algebraic systems of mathematics: the integers, the integers modulo n, the rational numbers, the real numbers, the complex numbers and polynomials.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006879",
      "subject":"MATH",
      "catalog_number":"136",
      "title":"Linear Algebra 1 for Honours Mathematics",
      "units":0.5,
      "description":"Systems of linear equations, matrix algebra, elementary matrices, computational issues. Real n-space, vector spaces and subspaces, basis and dimension, rank of a matrix, linear transformations and matrix representations. Determinants, eigenvalues and diagonalization, applications.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006880",
      "subject":"MATH",
      "catalog_number":"137",
      "title":"Calculus 1 for Honours Mathematics",
      "units":0.5,
      "description":"Rational, trigonometric, exponential, and power functions of a real variable; composites and inverses. Absolute values and inequalities. Limits and continuity. Derivatives and the linear approximation. Applications of the derivative, including curve sketching, optimization, related rates, and Newton's method. The Mean Value Theorem and error bounds. Introduction to the Riemann Integral and approximations. Antiderivatives and the Fundamental Theorem. Change of variable, areas and rate integrals. Suitable topics are illustrated using computer software.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006881",
      "subject":"MATH",
      "catalog_number":"138",
      "title":"Calculus 2 For Honours Mathematics",
      "units":0.5,
      "description":"Review of the Fundamental Theorem. Methods of integration. Further applications of the integral. Improper integrals. Linear and separable differential equations and applications. Vector (parametric) curves in R2. Convergence of sequences and series. Tests for convergence. Functions defined as power series. Taylor polynomials, Taylor's Theorem, and polynomial approximation. Taylor series. Suitable topics are illustrated using computer software.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006886",
      "subject":"MATH",
      "catalog_number":"145",
      "title":"Algebra (Advanced Level)",
      "units":0.5,
      "description":"MATH 145 is an advanced-level version of MATH 135. [Offered: F]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006887",
      "subject":"MATH",
      "catalog_number":"146",
      "title":"Linear Algebra 1 (Advanced level)",
      "units":0.5,
      "description":"MATH 146 is an advanced-level version of MATH 136. [Offered: W]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006888",
      "subject":"MATH",
      "catalog_number":"147",
      "title":"Calculus 1 (Advanced Level)",
      "units":0.5,
      "description":"MATH 147 is an advanced-level version of MATH 137. [Offered: F]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006889",
      "subject":"MATH",
      "catalog_number":"148",
      "title":"Calculus 2 (Advanced Level)",
      "units":0.5,
      "description":"MATH 148 is an advanced-level version of MATH 138. [Offered: W]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"013105",
      "subject":"MATH",
      "catalog_number":"207",
      "title":"Calculus 3 (Non-Specialist Level)",
      "units":0.5,
      "description":"Multivariable functions and partial derivatives. Gradients. Optimization including Lagrange multipliers. Polar coordinates. Multiple integrals. Surface integrals on spheres and cylinders. Introduction to Fourier Series. [Offered: F,W,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006891",
      "subject":"MATH",
      "catalog_number":"211",
      "title":"Advanced Calculus 1 for Electrical and Computer Engineers",
      "units":0.5,
      "description":"Fourier series. Ordinary differential equations. Laplace transform. Applications to linear electrical systems. [Offered: F,W]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"013158",
      "subject":"MATH",
      "catalog_number":"211N",
      "title":"Advanced Calculus 1 for Nanotechnology Engineering",
      "units":0.5,
      "description":"Ordinary differential equations with constant coefficients. Boundary value problems and applications to quantum mechanics. Laplace transforms, Fourier series and applications. Numerical solution of ordinary differential equations. [Offered: F]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006892",
      "subject":"MATH",
      "catalog_number":"212",
      "title":"Advanced Calculus 2 for Electrical Engineers",
      "units":0.5,
      "description":"Triple integrals, cylindrical and spherical polar coordinates. Divergence and curl, applications. Surface integrals, Green's, Gauss' and Stokes' theorems, applications. Complex functions, analytic functions, contour integrals, Cauchy's integral formula, Laurent series, residues. [Offered: F]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"013160",
      "subject":"MATH",
      "catalog_number":"212N",
      "title":"Advanced Calculus 2 for Nanotechnology Engineering",
      "units":0.5,
      "description":"Gradient, Divergence and Curl: Applications. Line and Surface Integrals. Green's, Gauss', and Stokes' Theorems: Applications to electromagnetism and fluid mechanics. Numerical solution of partial differential equations. [Offered: S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"011849",
      "subject":"MATH",
      "catalog_number":"213",
      "title":"Advanced Mathematics for Software Engineers",
      "units":0.5,
      "description":"Fourier series. Differential equations. Laplace transforms. Applications to circuit analysis. [Offered: S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"013464",
      "subject":"MATH",
      "catalog_number":"215",
      "title":"Linear Algebra for Engineering",
      "units":0.5,
      "description":"Systems of linear equations; their representation with matrices and vectors; their generalization to linear transformations on abstract vector spaces; and the description of these linear transformations through quantitative characteristics such as the determinant, the characteristic polynomial, eigenvalues and eigenvectors, the rank, and singular values. [Offered F,W]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006897",
      "subject":"MATH",
      "catalog_number":"217",
      "title":"Calculus 3 for Chemical Engineering",
      "units":0.5,
      "description":"Curves and surfaces in R3. Multivariable functions, partial derivatives, the chain rule, gradients. Optimization, Lagrange Multipliers. Double and triple integrals, change of variable. Vector fields, divergence and curl. Vector integral calculus: Green's theorem, the Divergence theorem and Stokes' theorem. Applications in engineering are emphasized. [Offered: F,W]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006898",
      "subject":"MATH",
      "catalog_number":"218",
      "title":"Differential Equations for Engineers",
      "units":0.5,
      "description":"First order equations, second order linear equations with constant coefficients, series solutions, the Laplace transform method, systems of linear differential equations. Applications in engineering are emphasized. [Offered: F,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006870",
      "subject":"MATH",
      "catalog_number":"225",
      "title":"Applied Linear Algebra 2",
      "units":0.5,
      "description":"Vector spaces. Linear transformations and matrices. Inner products. Eigenvalues and eigenvectors. Diagonalization. Applications. [Offered: F,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006907",
      "subject":"MATH",
      "catalog_number":"227",
      "title":"Calculus 3 for Honours Physics",
      "units":0.5,
      "description":"Directional derivative and the chain rule for multivariable functions. Optimization, Lagrange multipliers. Double and triple integrals on simple domains; transformations and Jacobians; change of variable in multiple integrals. Vector fields, divergence and curl. Vector integral calculus: Line and surface integrals, Green's Theorem, Stokes' Theorem, Gauss' Theorem, conservative vector fields.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006908",
      "subject":"MATH",
      "catalog_number":"228",
      "title":"Differential Equations for Physics and Chemistry",
      "units":0.5,
      "description":"First-order equations, second-order linear equations with constant coefficients, series solutions and special functions, the Laplace transform method. Applications in physics and chemistry are emphasized. [Offered: F,W]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"013104",
      "subject":"MATH",
      "catalog_number":"229",
      "title":"Introduction to Combinatorics (Non-Specialist Level)",
      "units":0.5,
      "description":"Introduction to graph theory: colourings, connectivity, Eulerian tours, planarity. Introduction to combinatorial analysis: elementary counting, generating series, binary strings. [Offered: F,W]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006913",
      "subject":"MATH",
      "catalog_number":"235",
      "title":"Linear Algebra 2 for Honours Mathematics",
      "units":0.5,
      "description":"Orthogonal and unitary matrices and transformations. Orthogonal projections, Gram-Schmidt procedure, best approximations, least-squares. Inner products, angles and orthogonality, orthogonal diagonalization, singular value decomposition, applications.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006914",
      "subject":"MATH",
      "catalog_number":"237",
      "title":"Calculus 3 for Honours Mathematics",
      "units":0.5,
      "description":"Calculus of functions of several variables. Limits, continuity, differentiability, the chain rule. The gradient vector and the directional derivative. Taylor's formula. Optimization problems. Mappings and the Jacobian. Multiple integrals in various co-ordinate systems.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006915",
      "subject":"MATH",
      "catalog_number":"239",
      "title":"Introduction to Combinatorics",
      "units":0.5,
      "description":"Introduction to graph theory: colourings, matchings, connectivity, planarity. Introduction to combinatorial analysis: generating series, recurrence relations, binary strings, plane trees.",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006920",
      "subject":"MATH",
      "catalog_number":"245",
      "title":"Linear Algebra 2 (Advanced Level)",
      "units":0.5,
      "description":"MATH 245 is an advanced-level version of MATH 235. [Offered: F,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006921",
      "subject":"MATH",
      "catalog_number":"247",
      "title":"Calculus 3 (Advanced Level)",
      "units":0.5,
      "description":"Topology of real n-dimensional space: completeness, closed and open sets, connectivity, compact sets, continuity, uniform continuity. Differential calculus on multivariable functions: partial differentiability, differentiability, chain rule, Taylor polynomials, extreme value problems. Riemann integration: Jordan content, integrability criteria, Fubini's theorem, change of variables. Local properties of continuously differentiable functions: open mapping theorem, inverse function theorem, implicit function theorem. [Offered: F,W,S]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"006922",
      "subject":"MATH",
      "catalog_number":"249",
      "title":"Introduction to Combinatorics (Advanced Level)",
      "units":0.5,
      "description":"MATH 249 is an advanced-level version of MATH 239. [Offered: F,W]",
      "academic_level":"undergraduate"
    },
    {
      "course_id":"013923",
      "subject":"MATH",
      "catalog_number":"600",
      "title":"Introduction to Mathematical Software for Teachers",
      "units":0.25,
      "description":"This course exposes students to the technical tools that professional mathematicians use.  The software presented in the course will enhance each student's communication, presentation, visualization, and problem-solving skills.  The course will also take a brief look at the history of mathematical communication and its impact on the development of the subject.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013831",
      "subject":"MATH",
      "catalog_number":"630",
      "title":"Foundations of Probability",
      "units":0.5,
      "description":"This course will explore the basic properties of probability focusing on both discrete and continuous random variables.  Topics include:  Laws of probability, discrete and continuous random variables, probability distributions, mean, variance, generating functions, Markov chains, problem solving, history of probability.",
      "academic_level":"graduate"
    },
    {
      "course_id":"014701",
      "subject":"MATH",
      "catalog_number":"631",
      "title":"Statistics for Teachers",
      "units":0.5,
      "description":"This course discusses some of the mathematical and scientific aspects of empirical, or data-based, problem solving.  Topics will include methods for the design of experiments and surveys, and the analysis of data using statistical models.  Examples will illustrate the application of these methods to data-based problems in science, health, business and industry.",
      "academic_level":"graduate"
    },
    {
      "course_id":"014212",
      "subject":"MATH",
      "catalog_number":"640",
      "title":"Number Theory for Teachers",
      "units":0.5,
      "description":"This course explores the many fascinating properties of the natural numbers. Topics include: the Euclidean algorithm, congruences and modular arithmetic, primitive roots and quadratic residues, sums of squares, multiplicative functions, continued fractions and Diophantine equations, and rational approximations to real numbers.",
      "academic_level":"graduate"
    },
    {
      "course_id":"014340",
      "subject":"MATH",
      "catalog_number":"641",
      "title":"Algorithm Design and Analysis",
      "units":0.25,
      "description":"This course explores the intersection between mathematics and computer science by examining general methods for solving problems efficiently. We will study a variety of algorithm design techniques for problems in diverse application areas and use mathematical models to compare algorithms.  Students will be introduced to \"big ideas\" from computer science, such as the generalization and reuse of previous solutions, and the notion of limits to the power of computation.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013841",
      "subject":"MATH",
      "catalog_number":"647",
      "title":"Foundations of Calculus I",
      "units":0.5,
      "description":"This course will explore the foundations of differential calculus, the role of rigor in mathematics, and the use of sophisticated mathematical software.  Topics include:  A brief primer on logic and proof, axiom of choice and other ideas from set theory, convergence of sequences and the various forms of the completeness axiom for R, detailed study of limits, continuity and the Intermediate Value Theorem, fundamentals of differentiation and the importance of linear approximation, role of the Mean Value Theorem, the nature and existence of extrema, Taylor's Theorem and polynomial approximation, MAPLE as a tool for discovery.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013840",
      "subject":"MATH",
      "catalog_number":"648",
      "title":"Foundations of Calculus II",
      "units":0.5,
      "description":"This course explores the foundations of integral calculus and the use of series in approximating the basic functions of mathematics.  Topics include:  Understanding the Riemann Integral and its flaws, the idea of Lebesque, the geometric meaning of the Riemann-Stieltjes integral, the Fundamental Theorem of Calculus, numerical integration, numerical series, uniform convergence of functions and the extraordinary nature of power series, Fourier Series.",
      "academic_level":"graduate"
    },
    {
      "course_id":"014058",
      "subject":"MATH",
      "catalog_number":"650",
      "title":"Mathematical Modeling with Differential Equations",
      "units":0.5,
      "description":"Solving and interpreting differential and difference equations motivated by a variety of systems from the physical and social sciences.  Analytical solutions of standard linear and non-linear equations of first and second order; phase portrait analysis; linearization of non-linear systems in the plane.   Numerical and graphical solutions using mathematical software.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013833",
      "subject":"MATH",
      "catalog_number":"660",
      "title":"Explorations in Geometry",
      "units":0.5,
      "description":"This course is designed to allow the student to discover fundamental facts about geometry through the interactive use of mathematical software.  Possible topics include:  An introduction to affine, projective and non-Euclidean geometry, conic sections in projective geometry, inversion in circles, the Theorems of Desargues, Pappas and Pascal.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013839",
      "subject":"MATH",
      "catalog_number":"670",
      "title":"Mathematical Connections:  Real World Problems in Mathematics I",
      "units":0.25,
      "description":"This course is intended to give the student insight to an important area of mathematics and how it connects with problems in the real world. Topics:  The course is one of four similar courses that will consist of either one six week module, or two three week modules each introducing a separate though possibly related area of mathematics.  The emphasis will be on how the mathematics is used in a real world context.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013838",
      "subject":"MATH",
      "catalog_number":"671",
      "title":"Mathematical Connections: Real World Problems in Mathematics II",
      "units":0.25,
      "description":"This course is intended to give the student insight to an important area of mathematics and how it connects with problems in the real world.  Topics: The course is one of four similar courses that will consist of either one six week module, or two three week modules each introducing a separate though possibly related area of mathematics.  The emphasis will be on how the mathematics is used in a real world context.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013837",
      "subject":"MATH",
      "catalog_number":"672",
      "title":"Mathematical Connections:  Real World Problems in Mathematics III",
      "units":0.25,
      "description":"This course is intended to give the student insight to an important area of mathematics and how it connects with problems in the real world.  Topics: The course is one of four similar courses that will consist of either one six week module, or two three week modules each introducing a separate though possibly related area of mathematics.  The emphasis will be on how the mathematics is used in a real world context.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013836",
      "subject":"MATH",
      "catalog_number":"673",
      "title":"Mathematical Connections:  Real World Problems in Mathematics IV",
      "units":0.25,
      "description":"This course is intended to give the student insight to an important area of mathematics and how it connects with problems in the real world.  Topics:  The course is one of four similar courses that will consist of either one six week module, or two three week modules each introducing a separate though possibly related area of mathematics.  The emphasis will be on how the mathematics is used in a real world context.",
      "academic_level":"graduate"
    },
    {
      "course_id":"014213",
      "subject":"MATH",
      "catalog_number":"674",
      "title":"Special Topics in Mathematical Connections",
      "units":0.25,
      "description":"This course is intended to give the student insight to an important area of mathematics and how it connects with problems in the real world.  The course will consist of either a one six week module, or two three week modules each introducing a separate though possibly related area of mathematics.  The emphasis will be on how the mathematics is used in a real world context.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013842",
      "subject":"MATH",
      "catalog_number":"680",
      "title":"History of Mathematics",
      "units":0.5,
      "description":"We explore the who, where, when and why of some of the most important ideas in mathematics.  Topics include:  William T. Tutte and Decryption, Euclid and the Delian Problem, Archimedes and his estimate of Pi, Al Khwarizmi and Islamic mathematics, Durer and the Renaissance, Descartes and Analytic Geometry, and Kepler and Planetary Motion.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013835",
      "subject":"MATH",
      "catalog_number":"681",
      "title":"Problem Solving and Mathematical Discovery",
      "units":0.5,
      "description":"This course aims to develop the student's mathematical problem solving ability.  Common heuristics such as problem modification, patterning, contradiction arguments and exploiting symmetry will be examined.  A wide range of challenging problems from various branches of mathematics will provide the medium through which these important principles and broad strategies are experienced.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013834",
      "subject":"MATH",
      "catalog_number":"690",
      "title":"Summer Conference for Teachers of Mathematics",
      "units":0.25,
      "description":"This intense 3-day workshop focuses on the integration of problem solving technology into the curriculum and enrichment activities.  The Workshop is suitable for teachers from all over the world.",
      "academic_level":"graduate"
    },
    {
      "course_id":"009357",
      "subject":"MATH",
      "catalog_number":"692",
      "title":"Reading, Writing and Discovering Proofs",
      "units":0.25,
      "description":"Objectives: To develop the vocabulary, techniques and analytical skills associated with reading and writing proofs, and to gain practice in formulating conjectures and discovering proofs.  Emphasis will be placed on understanding logical structures, recognition and command over common proof techniques, and precision in language. \r\n\r\nTopics Include: rules of formal logic, truth tables, role of definitions, implications, sets, existential and universal quantifiers, negation and counter-example, proofs by contradiction, proofs using the contrapositive, proofs of uniqueness and induction.",
      "academic_level":"graduate"
    },
    {
      "course_id":"014236",
      "subject":"MATH",
      "catalog_number":"698",
      "title":"Reading Course in Mathematics for Teachers",
      "units":0.25,
      "description":"Students will undertake a reading, research and writing project on a mathematical topic of interest to teachers.",
      "academic_level":"graduate"
    },
    {
      "course_id":"013832",
      "subject":"MATH",
      "catalog_number":"699",
      "title":"Master of Mathematics for Teachers Capstone",
      "units":0.5,
      "description":"The capstone course is designed to give students an opportunity to showcase the knowledge they have gained and to provide a forum for bringing that knowledge into their own classroom.  As part of this course students will design a mini-course on an approved subject in mathematics.",
      "academic_level":"graduate"
    },
    {
      "course_id":"014344",
      "subject":"MATH",
      "catalog_number":"700",
      "title":"Math for Teachers - OVGS Transfer Course",
      "units":1,
      "description":"",
      "academic_level":"graduate"
    }
  ]
}
```

