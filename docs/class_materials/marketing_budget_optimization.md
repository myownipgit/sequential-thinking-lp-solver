# Marketing Budget Optimization Using Sequential Thinking
## A Non-Linear Programming Example

### Problem Statement
A company needs to allocate its marketing budget of $100,000 across three channels:
- Digital Advertising
- Social Media
- Content Marketing

The unique challenge is that marketing returns follow diminishing returns (logarithmic curves).

### Given Parameters
1. Total Budget: $100,000
2. Channel Effectiveness:
   - Digital Ads: 1.5x
   - Social Media: 1.2x
   - Content Marketing: 1.3x

3. Return Functions (x in thousands):
   - Digital Ads: R1(x) = 1.5 * 10000 * ln(1 + x/10)
   - Social Media: R2(x) = 1.2 * 8000 * ln(1 + x/8)
   - Content Marketing: R3(x) = 1.3 * 9000 * ln(1 + x/9)

4. Constraints:
   - Minimum spend per channel: $10,000
   - Maximum spend per channel: $70,000

### Solution Steps Using Excel

#### Step 1: Setup Excel Worksheet
1. Create columns for:
   - Channel Name (A)
   - Allocation Amount (B)
   - Returns (C)
   - Marginal Returns (D)

2. Enter formulas for returns:
   ```excel
   Digital Ads: =15000*LN(1 + B2/10)
   Social Media: =9600*LN(1 + B3/8)
   Content Marketing: =11700*LN(1 + B4/9)
   ```

#### Step 2: Initial Allocation
1. Start with equal distribution:
   - Digital Ads: $33,333
   - Social Media: $33,333
   - Content Marketing: $33,334

2. Calculate initial returns:
   ```excel
   Total Returns: =SUM(C2:C4)
   ```

#### Step 3: Calculate Marginal Returns
1. Add formulas for marginal returns:
   ```excel
   Digital Ads: =15000/(10 + B2)
   Social Media: =9600/(8 + B3)
   Content Marketing: =11700/(9 + B4)
   ```

2. Compare marginal returns to identify:
   - Highest return channel (increase allocation)
   - Lowest return channel (decrease allocation)

#### Step 4: Iterative Optimization
1. Adjust allocations based on marginal returns:
   - Increase high marginal return channels
   - Decrease low marginal return channels
   - Maintain total budget constraint

2. Monitor constraints:
   ```excel
   Budget Check: =SUM(B2:B4)
   Min Check: =MIN(B2:B4)>=10
   Max Check: =MAX(B2:B4)<=70
   ```

#### Step 5: Final Solution
After iterations, optimal allocation:
1. Digital Advertising: $45,000
   - Highest effectiveness (1.5x)
   - Largest allocation

2. Content Marketing: $30,000
   - Medium effectiveness (1.3x)
   - Medium allocation

3. Social Media: $25,000
   - Lowest effectiveness (1.2x)
   - Smallest allocation

Total Returns: $56,331

### Excel Tips
1. Use Data Tables for sensitivity analysis
2. Create a chart showing returns vs. allocation
3. Use Goal Seek to find specific return targets
4. Add conditional formatting for constraints

### Verification Steps
1. Sum of allocations equals $100,000
2. All channels ≥ $10,000
3. All channels ≤ $70,000
4. Marginal returns are approximately equal

### Learning Points
1. Diminishing returns impact optimal allocation
2. Higher effectiveness doesn't mean proportionally higher allocation
3. Balance between channels is important
4. Constraints affect optimal solution

### Exercise Questions
1. How would the allocation change if:
   - Total budget increased to $150,000?
   - Minimum spend increased to $20,000?
   - Digital Ads effectiveness increased to 1.8x?

2. Why doesn't the highest effectiveness channel get all the budget?

3. How would you modify the solution for:
   - Four channels?
   - Different return functions?
   - Additional constraints?