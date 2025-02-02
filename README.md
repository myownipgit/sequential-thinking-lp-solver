# Sequential Thinking LP Solver

This repository demonstrates how to solve Linear Programming (LP) problems using the Sequential Thinking Model Context Protocol (MCP). The approach breaks down complex optimization problems into systematic, verifiable steps while maintaining flexibility for revisions and alternative paths.

## Prerequisites

This solution uses the Claude Desktop App, which provides access to Anthropic's Claude AI assistant and the Sequential Thinking MCP server. You can access Claude through:
- [Claude Desktop App](https://anthropic.com/claude)
- [Claude Web Interface](https://claude.ai)
- [Anthropic API](https://docs.anthropic.com/claude/docs)

## Model Context Protocol (MCP)

The Model Context Protocol (MCP) is an open standard that enables secure, two-way connections between AI models and various tools and data sources. Think of it like USB-C for AI - it provides a standardized way to connect AI models to different data sources and tools.

### MCP Architecture
The MCP follows a client-server architecture where:
- **Hosts** are LLM applications (like Claude Desktop) that initiate connections
- **Clients** maintain 1:1 connections with servers inside the host application
- **Servers** provide context, tools, and prompts to clients

For detailed architecture diagrams and documentation, visit the [Model Context Protocol Documentation](https://modelcontextprotocol.io/docs).

In our case, we're using the Sequential Thinking MCP Server through Claude Desktop App, which provides structured problem-solving capabilities through a client-host-server architecture. This allows us to:
- Break down complex problems systematically
- Maintain solution context throughout the process
- Revise and adapt our thinking as needed
- Connect with other tools and data sources when necessary

## Repository Structure

- `docs/`: Documentation and methodology
  - [`methodology.md`](docs/methodology.md): Core Sequential Thinking methodology
  - [`mcp_servers.md`](docs/mcp_servers.md): Detailed explanation of MCP Servers
  - [`sequential_thinking_guide.md`](docs/sequential_thinking_guide.md): Comprehensive usage guide
- `examples/`: Example problems and solutions
  - [`furniture_manufacturing.md`](examples/furniture_manufacturing.md): Complete example with solution
  - [`problem_variations.md`](examples/problem_variations.md): Additional problem scenarios
- `templates/`: Templates for applying the sequential thinking process
  - [`sequential_thinking_template.md`](templates/sequential_thinking_template.md): Template for new problems

## Getting Started

1. Install and set up the [Claude Desktop App](https://anthropic.com/claude)
2. Review the methodology in [`docs/methodology.md`](docs/methodology.md)
3. Understand MCP Servers in [`docs/mcp_servers.md`](docs/mcp_servers.md)
4. Check out the example problem in [`examples/furniture_manufacturing.md`](examples/furniture_manufacturing.md)
5. Use the template from [`templates/sequential_thinking_template.md`](templates/sequential_thinking_template.md) for your own problems

## Using with Claude

When using Claude to solve Linear Programming problems:
1. Access Claude through any of the available interfaces
2. Use the provided templates and examples as reference
3. Leverage the Sequential Thinking MCP for structured problem-solving
4. Follow the comprehensive guide in the documentation

For more information about using Claude, visit:
- [Claude Documentation](https://docs.anthropic.com/claude/docs)
- [Claude API Reference](https://docs.anthropic.com/claude/reference/getting-started-with-the-api)
- [Model Context Protocol Documentation](https://modelcontextprotocol.io/docs)

## Contributing

Contributions are welcome! Please read [`CONTRIBUTING.md`](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [`LICENSE`](LICENSE) file for details.