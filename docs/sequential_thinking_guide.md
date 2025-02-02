# Sequential Thinking Guide

## Introduction to Sequential Thinking

Sequential Thinking is a structured approach to problem-solving that breaks down complex problems into manageable steps while maintaining the flexibility to revise and adapt throughout the solution process. When combined with the Model Context Protocol (MCP), it becomes a powerful tool for solving Linear Programming problems.

## Getting Started

### 1. Problem Setup
Before using the Sequential Thinking tool:
- Clearly define the problem
- Identify all variables
- List all constraints
- State the objective function

### 2. Tool Initialization
Basic usage pattern:
```javascript
<function_calls>
<invoke name="sequentialthinking">
<parameter name="thought">Initial problem analysis</parameter>
<parameter name="thoughtNumber">1</parameter>
<parameter name="totalThoughts">5</parameter>
<parameter name="nextThoughtNeeded">true</parameter>
</invoke>
</function_calls>
```

## Core Concepts

### 1. Thought Structure
Each thought should contain:
- Clear statement of current step
- Mathematical calculations when needed
- Logical reasoning
- Progress towards solution

### 2. Revision Capability
When revising previous thoughts:
```javascript
<function_calls>
<invoke name="sequentialthinking">
<parameter name="thought">Revised analysis based on new insight</parameter>
<parameter name="thoughtNumber">3</parameter>
<parameter name="totalThoughts">5</parameter>
<parameter name="isRevision">true</parameter>
<parameter name="revisesThought">2</parameter>
<parameter name="nextThoughtNeeded">true</parameter>
</invoke>
</function_calls>
```

### 3. Branching Logic
For exploring alternative solutions:
```javascript
<function_calls>
<invoke name="sequentialthinking">
<parameter name="thought">Alternative approach analysis</parameter>
<parameter name="thoughtNumber">4</parameter>
<parameter name="totalThoughts">6</parameter>
<parameter name="branchFromThought">3</parameter>
<parameter name="branchId">alt-1</parameter>
<parameter name="nextThoughtNeeded">true</parameter>
</invoke>
</function_calls>
```

## Best Practices

### 1. Problem Analysis
- Start with clear problem definition
- Break down complex constraints
- Identify key relationships
- Plan solution approach

### 2. Solution Development
- Progress systematically
- Show all calculations
- Document assumptions
- Verify each step

### 3. Verification
- Check all constraints
- Validate calculations
- Consider edge cases
- Test alternative solutions

## Working with Linear Programming

### 1. Problem Formulation
- Define variables clearly
- State objective function
- List all constraints
- Note assumptions

### 2. Solution Process
1. Initial setup
2. Constraint analysis
3. Solution development
4. Optimization
5. Verification

### 3. Common Patterns
- Resource allocation
- Optimization problems
- Constraint satisfaction
- Multi-variable optimization

## Advanced Features

### 1. Integration with Other MCP Servers
```javascript
// Using REPL for calculations
<function_calls>
<invoke name="repl">
<parameter name="code">
// Verification calculations
const result = verify(solution);
console.log(result);
</parameter>
</invoke>
</function_calls>
```

### 2. Complex Problem Handling
- Multiple variable management
- Constraint prioritization
- Solution optimization
- Result verification

## Troubleshooting

### 1. Common Issues
- Unclear problem definition
- Missing constraints
- Calculation errors
- Logic gaps

### 2. Solutions
- Verify inputs
- Check calculations
- Test constraints
- Review logic

## Examples

### 1. Basic Problem
```javascript
// Simple maximization problem
<function_calls>
<invoke name="sequentialthinking">
<parameter name="thought">Maximize profit given constraints</parameter>
<parameter name="thoughtNumber">1</parameter>
<parameter name="totalThoughts">4</parameter>
<parameter name="nextThoughtNeeded">true</parameter>
</invoke>
</function_calls>
```

### 2. Complex Problem
```javascript
// Multi-variable optimization
<function_calls>
<invoke name="sequentialthinking">
<parameter name="thought">Multi-resource allocation analysis</parameter>
<parameter name="thoughtNumber">1</parameter>
<parameter name="totalThoughts">7</parameter>
<parameter name="nextThoughtNeeded">true</parameter>
</invoke>
</function_calls>
```

## Tips for Success

### 1. Problem Setup
- Define clearly
- List assumptions
- Note limitations
- Plan approach

### 2. Solution Process
- Work systematically
- Document steps
- Verify results
- Consider alternatives

### 3. Result Presentation
- Clear conclusions
- Supporting data
- Verification proof
- Alternative considerations