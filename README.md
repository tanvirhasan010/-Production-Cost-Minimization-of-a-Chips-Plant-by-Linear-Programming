# 🥔 Production Cost Minimization of a Chips Plant using Linear Programming

## 📊 Project Overview

This repository contains an optimization project that applies **Linear Programming (LP)** to minimize production costs for a potato chips manufacturing plant. The project addresses the complex challenge of optimizing raw material usage, production processes, and resource allocation while satisfying nutritional requirements, production constraints, and quality standards. This demonstrates the practical application of operations research techniques in the food processing industry.

## 🎯 Business Problem

The chips manufacturing plant faces several optimization challenges:
- **Cost Management**: Rising costs of raw materials (potatoes, oil, seasonings)
- **Resource Constraints**: Limited production capacity, storage space, and machine availability
- **Quality Standards**: Maintaining consistent product quality and nutritional values
- **Demand Fluctuations**: Meeting variable customer demand while minimizing costs
- **Production Efficiency**: Optimizing the use of ingredients and production processes

## 🎯 Project Objectives

- **Cost Minimization**: Develop an optimal production plan that minimizes total production costs
- **Resource Optimization**: Efficient allocation of raw materials and production resources
- **Constraint Satisfaction**: Meet all nutritional, quality, and production constraints
- **Sensitivity Analysis**: Understand how changes in costs and constraints affect the optimal solution
- **Decision Support**: Provide management with data-driven insights for production planning

## 🧮 Mathematical Modeling

### Decision Variables:
- \( x_1, x_2, ..., x_n \): Amount of each raw material used (potatoes, oil, seasonings, additives)
- \( y_1, y_2, ..., y_m \): Production time allocated to different products or processes

### Objective Function:
\[
\text{Minimize } Z = \sum_{i=1}^{n} c_i x_i + \sum_{j=1}^{m} p_j y_j
\]
Where:
- \( c_i \): Cost per unit of raw material \( i \)
- \( p_j \): Cost per unit of production time \( j \)

### Constraints:
1. **Nutritional Constraints**:
   \[
   \sum_{i=1}^{n} n_{ki} x_i \geq N_k^{\text{min}} \quad \text{and} \quad \sum_{i=1}^{n} n_{ki} x_i \leq N_k^{\text{max}} \quad \forall k
   \]
   (For fat, sodium, carbohydrates, etc.)

2. **Production Capacity**:
   \[
   \sum_{j=1}^{m} a_{ij} y_j \leq C_i \quad \forall i
   \]
   (Machine hours, labor constraints)

3. **Quality Requirements**:
   \[
   Q_k^{\text{min}} \leq \sum_{i=1}^{n} q_{ki} x_i \leq Q_k^{\text{max}} \quad \forall k
   \]
   (Texture, taste, appearance standards)

4. **Demand Constraints**:
   \[
   D_k^{\text{min}} \leq \sum_{j=1}^{m} d_{kj} y_j \leq D_k^{\text{max}} \quad \forall k
   \]

5. **Non-negativity**:
   \[
   x_i \geq 0, \quad y_j \geq 0 \quad \forall i,j
   \]

## 🛠️ Implementation Details

### Optimization Approach:
- **Linear Programming**: For continuous decision variables and linear constraints
- **Solver Selection**: Using specialized LP solvers (PuLP, SciPy, or commercial solvers)
- **Sensitivity Analysis**: Examining shadow prices and reduced costs

### Technical Stack:
- **Programming Language**: Python
- **Optimization Libraries**: PuLP, SciPy, CVXPY, or Pyomo
- **Data Analysis**: Pandas, NumPy for data manipulation
- **Visualization**: Matplotlib, Seaborn for results presentation
- **Interface**: Jupyter Notebooks for interactive analysis

### Key Features Modeled:
- **Raw Material Costs**: Potato varieties, oil types, seasoning blends
- **Production Costs**: Energy consumption, labor costs, machine maintenance
- **Nutritional Requirements**: Fat content, sodium levels, calorie counts
- **Quality Parameters**: Crispness, color, flavor intensity
- **Operational Constraints**: Storage capacity, shelf life, production line speeds

## 📊 Expected Outcomes

### Quantitative Benefits:
- **Cost Reduction**: X% reduction in total production costs
- **Waste Reduction**: X% decrease in raw material waste
- **Efficiency Improvement**: X% better resource utilization
- **Production Increase**: X% higher output with same resources

### Strategic Insights:
- **Optimal Recipes**: Cost-effective ingredient combinations
- **Production Scheduling**: Efficient allocation of production time
- **Procurement Strategy**: Optimal raw material purchasing plans
- **Pricing Guidance**: Data-driven input for product pricing decisions

## 📁 Repository Structure

```
├── data/
│   ├── raw/                    # Original cost and constraint data
│   ├── processed/              # Cleaned and formatted data
│   └── parameters/             # Nutritional and quality parameters
├── src/
│   ├── model_formulation.py    # LP model formulation
│   ├── solver_interface.py     # Solver configuration and execution
│   ├── sensitivity_analysis.py # Post-optimality analysis
│   ├── visualization.py        # Results visualization
│   └── utils/                  # Utility functions
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_model_development.ipynb
│   ├── 03_sensitivity_analysis.ipynb
│   └── 04_results_visualization.ipynb
├── docs/
│   ├── problem_statement.md    # Detailed problem description
│   ├── mathematical_model.md   # Complete mathematical formulation
│   └── results/                # Analysis reports and findings
├── tests/                      # Unit tests for model components
├── requirements.txt            # Python dependencies
└── README.md                   # This file
```

## 🚀 How to Use This Project

### Prerequisites
- Python 3.8+
- Linear programming solver (CBC, GLPK, or commercial solver)
- Basic understanding of optimization concepts

### Installation & Setup
1. **Clone the repository**:
   ```bash
   git clone https://github.com/tanvirhasan010/-Production-Cost-Minimization-of-a-Chips-Plant-by-Linear-Programming.git
   cd -Production-Cost-Minimization-of-a-Chips-Plant-by-Linear-Programming
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Install optimization solver**:
   ```bash
   # For CBC solver (open source)
   sudo apt-get install coinor-cbc
   ```

5. **Run the analysis**:
   ```bash
   jupyter notebook notebooks/01_data_exploration.ipynb
   ```

### Usage Examples:
- Modify cost parameters in configuration files
- Adjust nutritional and quality constraints
- Test different production scenarios
- Perform what-if analysis for strategic planning

## 📈 Results Interpretation

The optimization provides:
- **Optimal Solution**: Minimum cost production plan
- **Shadow Prices**: Value of relaxing constraints
- **Reduced Costs**: Cost sensitivity for non-basic variables
- **Feasibility Analysis**: Constraint satisfaction verification
- **Scenario Comparisons**: Different operational scenarios

## 🤝 Contributing

This project welcomes contributions and feedback. To contribute:
1. Fork the repository
2. Create a feature branch
3. Make your changes with proper documentation
4. Submit a pull request with detailed description

## 📄 License

This project is developed for academic and research purposes. Please contact for commercial applications.

## 👨‍💻 Author

**Md Tanvir Hasan**
- GitHub: [@tanvirhasan010](https://github.com/tanvirhasan010)


## 🙏 Acknowledgments

- Operations research community for foundational linear programming techniques
- Food processing industry references for practical constraints
- Open-source optimization tools and libraries
- Academic resources that informed the methodology

