# Furniture Manufacturing Optimization Example

## Problem Statement

A furniture manufacturer produces Chairs and Tables with the following constraints:
- Each Chair: 2 hours labor, 3 kg wood
- Each Table: 4 hours labor, 5 kg wood
- Daily resources: 40 hours labor, 60 kg wood
- Profit: $30 per Chair, $50 per Table

## Sequential Thinking Solution

### Step 1: Problem Definition and Setup
Identified variables and constraints:
```
Variables:
- x = number of Chairs
- y = number of Tables

Objective Function:
Maximize Profit = 30x + 50y

Constraints:
1. Labor: 2x + 4y ≤ 40 hours
2. Wood: 3x + 5y ≤ 60 kg
3. Non-negativity: x ≥ 0, y ≥ 0
```

### Step 2: Boundary Analysis
Calculated constraint boundaries:
- Labor constraint points: (0,10) and (20,0)
- Wood constraint points: (0,12) and (20,0)

### Step 3: Intersection Point
Found intersection through system of equations:
```
2x + 4y = 40
3x + 5y = 60

Solution: (20,0)
```

### Step 4: Solution Evaluation
Evaluated profit at corner points:
- (0,0): $0
- (0,10): $500
- (20,0): $600

### Step 5: Verification
Verified constraints:
- Labor: 2(20) + 4(0) = 40 ✓
- Wood: 3(20) + 5(0) = 60 ✓
- Non-negativity: x,y ≥ 0 ✓

### Step 6: Final Solution
Optimal production plan:
- 20 Chairs
- 0 Tables
- Maximum profit: $600