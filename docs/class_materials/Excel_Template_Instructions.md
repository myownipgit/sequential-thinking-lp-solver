# Excel Template Setup Instructions

## Worksheet Structure

### 1. Input Parameters Sheet
- Cell A1: "Marketing Budget Optimization"
- Cells A3-A5: Channel names
- Cells B3-B5: Effectiveness multipliers
- Cells C3-C5: Current allocation
- Cell B7: Total budget
- Cells B8-B9: Min/Max constraints

### 2. Calculations Sheet

#### Returns Calculation
```excel
Row Headers (A2-A4):
- Digital Advertising
- Social Media
- Content Marketing

Column Headers (B1-E1):
- Allocation
- Returns
- Marginal Returns
- % of Budget

Formulas:
B2: =Parameters!C3
C2: =15000*LN(1 + B2/10)
D2: =15000/(10 + B2)
E2: =B2/Parameters!B7

B3: =Parameters!C4
C3: =9600*LN(1 + B3/8)
D3: =9600/(8 + B3)
E3: =B3/Parameters!B7

B4: =Parameters!C5
C4: =11700*LN(1 + B4/9)
D4: =11700/(9 + B4)
E4: =B4/Parameters!B7
```

#### Constraint Checks
```excel
G2: "Constraint Checks"
G3: "Total Budget"
H3: =SUM(B2:B4)
I3: =H3=Parameters!B7

G4: "Min Check"
H4: =MIN(B2:B4)
I4: =H4>=Parameters!B8

G5: "Max Check"
H5: =MAX(B2:B4)
I5: =H5<=Parameters!B9
```

### 3. Analysis Sheet

#### Sensitivity Analysis Table
```excel
Create a data table varying allocations:
- Row input: Digital Advertising (10k to 70k, step 10k)
- Column input: Social Media (10k to 70k, step 10k)
- Calculate Content Marketing as remainder
- Show total returns for each combination
```

#### Charts
1. Returns by Channel:
   - X-axis: Allocation amount
   - Y-axis: Returns
   - Three lines for each channel

2. Current Allocation Pie Chart:
   - Show percentage distribution
   - Use different colors for each channel

### 4. Optimization Tips

#### Using Goal Seek
1. Select total returns cell
2. Data → What-If Analysis → Goal Seek
3. Set to desired return value
4. By changing allocation cells

#### Using Solver
1. Target cell: Total returns
2. To: Maximize
3. By changing: Allocation cells
4. Subject to constraints:
   - Sum = Total budget
   - Each allocation ≥ Minimum
   - Each allocation ≤ Maximum

### 5. Data Validation

Add these validation rules to allocation cells:
```excel
Minimum value: =Parameters!B8
Maximum value: =Parameters!B9
Error message: "Allocation must be between minimum and maximum constraints"
```

## Using the Template

1. Start with equal allocations
2. Calculate initial returns
3. Use marginal returns to guide adjustments
4. Verify constraints after each change
5. Use sensitivity analysis to understand impact
6. Document optimization steps
7. Verify final solution

## Common Issues

1. Circular References
   - Check formulas for self-references
   - Use previous values for iterative calculations

2. Constraint Violations
   - Use conditional formatting to highlight violations
   - Always check constraint cells after changes

3. Returns Calculation
   - Verify logarithm base (natural log)
   - Check units (thousands vs. actual values)

4. Optimization
   - Start with feasible solution
   - Make small adjustments
   - Document each step