# Building Mass Optimization — Research Papers

Last updated: 2026-03-13

## 1. Core: EvoMass (Likai Wang et al.)

### 1a. EvoMass — Typology-Oriented Building Massing Optimization
- **Title**: Optimization-based design exploration of building massing typologies — EvoMass and a typology-oriented computational design optimization method for early-stage performance-based building massing design
- **Authors**: Likai Wang, Patrick Janssen, Guohua Ji
- **Journal**: Frontiers of Architectural Research, Vol. 13, Issue 6, p.1400, 2024
- **URL**: https://www.sciencedirect.com/science/article/pii/S2095263524000797
- **Key contributions**:
  - **Additive/Subtractive massing paradigm**: generates diverse building typologies (slab, tower, courtyard, L-shape, U-shape) from parametric rules
  - **SSIEA (Steady-State Island EA)**: hybrid evolutionary algorithm combining island model + steady-state replacement → better typological diversity than NSGA-II
  - **Island model**: separate sub-populations evolve independently, periodic migration maintains diversity — prevents premature convergence to single typology
  - **Grasshopper/Rhino platform**: EvoMass implemented as Grasshopper components
- **Relevance to our project**: Our GA uses Categorical gene for mass_shape (rect/L/U/courtyard) — similar concept but simpler. SSIEA's island model could improve diversity if needed.

### 1b. EvoMass + GH_Wind — Wind-Driven Massing
- **Title**: EvoMass + GH_Wind — An agile wind-driven building massing design optimization framework
- **Authors**: Likai Wang et al.
- **URL**: https://www.researchgate.net/publication/353906430
- **Key**: Couples wind simulation (CFD surrogate) with massing optimization. Multi-objective: daylight + wind comfort.

### 1c. Reverse Passive Strategy Exploration
- **Title**: Reverse passive strategy exploration for building massing design — An optimization-aided approach
- **Authors**: Likai Wang, Ting Luo, Tong Shao, Guohua Ji
- **Journal**: International Journal of Architectural Computing, 2023
- **URL**: https://journals.sagepub.com/doi/10.1177/14780771231177514
- **Key**: Inverts the typical workflow — starts from performance targets and discovers massing forms that achieve them.

### 1d. SSIEA Algorithm Paper
- **Title**: SSIEA: a hybrid evolutionary algorithm for supporting conceptual architectural design
- **Journal**: AI EDAM (Cambridge Core)
- **URL**: https://www.cambridge.org/core/journals/ai-edam/article/abs/ssiea-a-hybrid-evolutionary-algorithm-for-supporting-conceptual-architectural-design/F62E663EECA36C82100A8012A6D258AE
- **Key**: Original SSIEA algorithm paper. Island model with migration, steady-state replacement. Produces more diverse design alternatives than centralized-population EA.

### 1e. Massing + Facade Synergy
- **Title**: Exploring the synergy of building massing and facade design through evolutionary optimization
- **Authors**: Likai Wang et al.
- **URL**: https://www.researchgate.net/publication/359222814
- **Key**: Joint optimization of mass shape AND facade design (window ratios, shading) — shows coupling effects between form and envelope.

---

## 2. Multi-Objective Building Optimization

### 2a. NSGA-II Urban Block Morphology (Wuhan)
- **Title**: Parametric Multi-Objective Optimization of Urban Block Morphology Using NSGA-II: A Case Study in Wuhan, China
- **Journal**: Sustainability, 2025, 17(21), 9724
- **URL**: https://www.mdpi.com/2071-1050/17/21/9724
- **Key**: 3-objective NSGA-II (sunshine hours, energy use intensity, thermal comfort) for urban block morphology. EnergyPlus + Honeybee simulation. Directly relevant to our daylight objective.

### 2b. Daylighting + Solar Radiation Hybrid EA
- **Title**: Multi-objective optimization of daylighting performance and solar radiation for building geometry using a hybrid evolutionary algorithm
- **Journal**: Scientific Reports, 2025
- **URL**: https://www.nature.com/articles/s41598-025-12165-6
- **Key**: Hybrid EA for building geometry optimization with dual daylight/solar objectives. Recent (2025).

### 2c. GA-Based Multi-Objective Building Retrofitting (Survey)
- **Title**: Genetic algorithm-based multi-objective optimisation for energy-efficient building retrofitting: A systematic review
- **Journal**: ScienceDirect, 2024
- **URL**: https://www.sciencedirect.com/science/article/pii/S037877882401332X
- **Key**: Comprehensive survey of GA in building domain. NSGA-II most applied algorithm. Useful for methodology justification.

### 2d. Double-Layer Shell Structure Optimization
- **Title**: A graph-based multi-objective genetic algorithm for optimizing the structural performance in double-layer shell structures
- **Journal**: ScienceDirect, 2025
- **URL**: https://www.sciencedirect.com/science/article/pii/S2352710225014354
- **Key**: Graph-based representation for structural optimization. Novel encoding relevant to our shape representation.

---

## 3. Floor Plan Generation (GAN / RL / Hybrid)

### 3a. ArchiGAN — 3-Step Generation Stack
- **Title**: ArchiGAN: Artificial Intelligence x Architecture
- **Authors**: Stanislas Chaillou (Harvard GSD)
- **URL**: https://developer.nvidia.com/blog/archigan-generative-stack-apartment-building-design/
- **Paper**: https://papers.cumincad.org/data/works/att/artificial_intellicence2019_117.pdf
- **Key contributions**:
  - 3-step Pix2Pix GAN pipeline: (1) footprint massing from parcel, (2) program repartition, (3) furniture layout
  - GIS data (Boston) for parcel shapes training
  - Demonstrates chained generation from site → mass → plan → furnishing
- **Relevance**: Our system stops at massing — ArchiGAN shows potential downstream extension to floor plans.

### 3b. Graph-Constrained GAN for Architectural Layout
- **Title**: Architectural layout generation using a graph-constrained conditional Generative Adversarial Network (GAN)
- **Journal**: Automation in Construction, 2023
- **URL**: https://www.sciencedirect.com/science/article/abs/pii/S0926580523003138
- **Key**: Graph constraints ensure room adjacency requirements are satisfied. Better than pure pixel-based GANs.

### 3c. Deep RL for Space Layout Design
- **Title**: Reimagining space layout design through deep reinforcement learning
- **Journal**: Journal of Computational Design and Engineering (Oxford), 2024
- **URL**: https://academic.oup.com/jcde/article/11/3/43/7636504
- **Key**: RL agent places rooms sequentially, learns spatial relationships. More controllable than GAN approaches.

### 3d. Community Layout with Deep RL
- **Title**: Deep reinforcement learning for community architectural layout generation
- **Journal**: Knowledge and Information Systems (Springer), 2024
- **URL**: https://link.springer.com/article/10.1007/s10115-024-02291-4
- **Key**: Scales RL layout generation to community-level planning.

### 3e. Floor Plan Generation Survey
- **Title**: Floor plan generation: The interplay among data, machine, and designer
- **Authors**: Fatemeh Mostafavi, Casper van Engelenburg, Seyran Khademi, Georg Vrachliotis
- **Journal**: International Journal of Architectural Computing, 2025
- **URL**: https://journals.sagepub.com/doi/10.1177/14780771241290649
- **Key**: Comprehensive 2025 survey of floor plan generation methods. Human-AI interplay emphasis.

### 3f. FloorplanGAN — Vector Output
- **Title**: FloorplanGAN: Vector residential floorplan adversarial generation
- **URL**: https://www.researchgate.net/publication/362385040
- **Key**: Produces vector (not raster) floor plans — closer to CAD-ready output.

---

## 4. Generative AI in Architecture (Surveys / Reviews)

### 4a. Performance-Driven Generative Design (Survey)
- **Title**: Performance-Driven Generative Design in Buildings: A Systematic Review
- **Journal**: Buildings (MDPI), 2025
- **URL**: https://www.mdpi.com/2075-5309/15/24/4556
- **Key**: Reviews facade, envelope, and massing optimization. Energy + daylight + thermal most common objectives. Parametric platforms + simulation + multi-objective optimization dominant approach.

### 4b. Gen-AI Applications in Building Research
- **Title**: Exploring Gen-AI applications in building research and industry: A review
- **Journal**: Building Simulation (Springer), 2025
- **URL**: https://link.springer.com/article/10.1007/s12273-025-1279-x
- **Key**: Broad survey of GenAI (LLM, diffusion, GAN) in building domain.

### 4c. Generative AI in Architectural Design Workflow
- **Title**: Shaping Architecture with Generative Artificial Intelligence: Deep Learning Models in Architectural Design Workflow
- **Journal**: MDPI, 2024
- **URL**: https://www.mdpi.com/2673-8945/5/4/94
- **Key**: How deep learning models integrate into architectural workflows.

### 4d. Generative Design for Spatial Layouts (Review)
- **Title**: Generative design for architectural spatial layouts: a review of technical approaches
- **Journal**: Taylor & Francis, 2025
- **URL**: https://www.tandfonline.com/doi/full/10.1080/13467581.2025.2512235
- **Key**: Technical review of layout generation methods.

### 4e. Generative AI Models for Architecture Steps (Review)
- **Title**: Generative AI models for different steps in architectural design: A literature review
- **Journal**: Frontiers of Architectural Research, 2024
- **URL**: https://www.sciencedirect.com/science/article/pii/S209526352400147X
- **Key**: Maps GenAI to each architectural design phase (concept → massing → plan → detail).

---

## 5. Setback / Zoning Envelope

### 5a. NYC 1916 Zoning — Origin of Step-Back Massing
- **URL**: https://99percentinvisible.org/article/progressive-setbacks-the-century-old-nyc-mandate-that-shaped-modern-skylines/
- **Key**: Historical context. 1916 Zoning Resolution created "wedding cake" massing. Sky exposure plane concept.

### 5b. Arcol — Parametric Sloped Setbacks
- **URL**: https://www.arcol.io/product-updates/sloped-setbacks
- **Key**: Modern parametric tool that auto-generates building envelope from setback angles. Similar to our step-back GA gene concept.

---

## 6. CAADRIA 2024 Conference Papers

### 6a. Formal Variation for Performance-Based Massing
- **Title**: Formal Variation Exploration for Performance-Based Building Massing Design Optimization
- **URL**: https://caadria2024.org/wp-content/uploads/2024/04/288-FORMAL-VARIATION-EXPLORATION-FOR-PERFORMANCE-BASED-BUILDING-MASSING-DESIGN-OPTIMIZATION.pdf
- **Key**: Directly relevant — explores formal variation in massing optimization.

### 6b. AI-Enhanced Performative Building Design
- **Title**: AI-Enhanced Performative Building Design Optimization and Exploration
- **URL**: https://caadria2024.org/wp-content/uploads/2024/04/15-AI-ENHANCED-PERFORMATIVE-BUILDING-DESIGN-OPTIMIZATION-AND-EXPLORATION.pdf
- **Key**: AI surrogate models accelerate performance evaluation in optimization loops.

### 6c. Mobius Evolver — Competitive Urban Massing
- **Title**: Möbius evolver: Competitive exploration of urban massing strategies
- **URL**: https://www.researchgate.net/publication/360760869
- **Key**: Competition-based (game-theoretic) approach to urban massing exploration.

---

## Summary: What We Can Learn

| Paper/Tool | Our Equivalent | Gap / Opportunity |
|-----------|---------------|-------------------|
| EvoMass SSIEA island model | Single-pop NSGA-II | Island model could improve typological diversity |
| EvoMass additive/subtractive | Categorical gene (4 shapes) | Could add more shape grammar rules |
| ArchiGAN 3-step stack | Massing only | Downstream: plan → furniture possible |
| RL layout generation | Not implemented | Future: room layout within our mass |
| Graph-constrained GAN | Not implemented | Adjacency-aware layout generation |
| Daylighting hybrid EA | Simplified daylight score | Could integrate Radiance/Honeybee |
| Parametric setbacks | upper_scale + step_fraction genes | Works well for Korean 일조권 setback |
| Facade-massing synergy | Not implemented | Joint mass+facade optimization |

## Our Technical Position

Our system (`ARR/backend/design/`) implements:
- **NSGA-II** with 10-gene genome (x, y, w, d, ratio, floors, rotation, mass_shape, upper_scale, step_fraction)
- **4 mass typologies** via Categorical gene: rectangle, L, U, courtyard
- **Step-back/podium-tower** via upper_scale + step_fraction (2-tier massing)
- **Regulation-coupled constraints** from `land/analyze/` (건폐율/용적률/높이 자동 반영)
- **Cesium 3D visualization** with shape-specific colors + setback overlay
- **SSE real-time streaming** of optimization progress

Unique advantage vs. EvoMass: **Direct regulation integration** — Korean building law (건축법/국토계획법) from Neo4j graph DB auto-injects zoning constraints into GA. EvoMass requires manual constraint input.
