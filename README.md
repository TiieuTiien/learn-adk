# Learn ADK Project

Welcome to the Agent Development Kit (ADK) learning project! This comprehensive tutorial collection will take you from beginner to professional in building AI agents and automating workflows using Google's Agent Development Kit.

> Based on the tutorial: [Agent Development Kit (ADK) Masterclass: Build AI Agents & Automate Workflows (Beginner to Pro)](https://www.youtube.com/watch?v=P4VFL9nIaIA&t=9494s) by @aiwithbrandon

## Table of Contents

- Prerequisites
- Setup
- Learning Path
- Examples Overview
- Key Concepts Covered
- Advanced Patterns
- Additional Resources

## Prerequisites

- Python 3.9+
- Google API Key for Gemini models
- Basic understanding of Python programming
- Familiarity with command line operations

## Setup

1. **Clone the repository** (if applicable) or create the project structure
2. **Create a virtual environment**:
   ```bash
   python -m venv .venv
   
   # Activate the virtual environment
   # macOS/Linux:
   source .venv/bin/activate
   # Windows CMD:
   .venv\Scripts\activate.bat
   # Windows PowerShell:
   .venv\Scripts\Activate.ps1
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up your Google API key**:
   - Get your API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Create `.env` files in each example directory
   - Add your API key: `GOOGLE_API_KEY=your_api_key_here`

## Learning Path

Follow these examples in order to build your ADK expertise progressively:

### **Beginner Level**
1. **01-basic-agent** - Your first ADK agent
2. **02-tool-agent** - Adding tools to extend agent capabilities
3. **03-litellm-agent** - Using LiteLLM for multi-model support

### **Intermediate Level**
4. **04-structured-outputs** - Controlling response formats with Pydantic
5. **05-sessions-and-state** - Managing conversation state and user data
6. **06-persistent-storage** - Long-term memory with database storage

### **Advanced Level**
7. **07-multi-agent** - Coordinating multiple specialized agents
8. **08-stateful-multi-agent** - Advanced multi-agent systems with shared state
9. **09-callbacks** - Intercepting and modifying agent behavior

### **Workflow Agents (Professional Level)**
10. **10-sequential-agent** - Step-by-step processing pipelines
11. **11-parallel-agent** - Concurrent task execution
12. **12-loop-agent** - Iterative refinement workflows

## Examples Overview

### Core Agent Concepts

| Example | Description | Key Features |
|---------|-------------|--------------|
| **Basic Agent** | Simple greeting agent | Foundation concepts, agent structure |
| **Tool Agent** | Web search capabilities | Built-in tools, custom functions |
| **LiteLLM Agent** | Multi-model support | Provider flexibility, dad joke generator |

### Data Management

| Example | Description | Key Features |
|---------|-------------|--------------|
| **Structured Outputs** | Email generator with JSON schema | Pydantic models, data validation |
| **Sessions & State** | User preference management | In-memory sessions, template variables |
| **Persistent Storage** | Reminder system with database | SQLite storage, long-term memory |

### Multi-Agent Systems

| Example | Description | Key Features |
|---------|-------------|--------------|
| **Multi-Agent** | Specialized agent coordination | Sub-agents, agent-as-tool patterns |
| **Stateful Multi-Agent** | Customer service system | Shared state, dynamic routing |
| **Callbacks** | Agent behavior modification | Monitoring, filtering, transformation |

### Workflow Orchestration

| Example | Description | Key Features |
|---------|-------------|--------------|
| **Sequential Agent** | Lead qualification pipeline | Ordered execution, data passing |
| **Parallel Agent** | System monitoring | Concurrent execution, performance optimization |
| **Loop Agent** | LinkedIn post refinement | Iterative improvement, quality control |

## Key Concepts Covered

### **Agent Fundamentals**
- Agent structure and discovery
- Instructions and personality design
- Model selection and configuration
- Environment setup and API keys

### **Tool Integration**
- Built-in Google tools (Search, Code Execution)
- Custom function tools
- Tool limitations and workarounds
- Best practices for tool design

### **State Management**
- Session services (In-memory vs Database)
- State persistence and retrieval
- Template variables in instructions
- Cross-agent state sharing

### **Multi-Agent Patterns**
- Sub-agent delegation model
- Agent-as-tool approach
- Specialized domain expertise
- Query routing and coordination

### **Workflow Orchestration**
- Sequential processing pipelines
- Parallel task execution
- Loop-based iterative refinement
- Exit conditions and control flow

### **Advanced Features**
- Structured input/output schemas
- Callback system for behavior modification
- Multi-model support with LiteLLM
- Production deployment considerations

## Advanced Patterns

### **Agent Architecture Patterns**
- **Single Agent**: Basic functionality with optional tools
- **Multi-Agent**: Specialized agents working together
- **Workflow Agents**: Orchestrated execution patterns
- **Hybrid Systems**: Combining multiple patterns

### **State Management Strategies**
- **Stateless**: Each interaction is independent
- **Session State**: Temporary memory during conversation
- **Persistent State**: Long-term memory across sessions
- **Shared State**: Multiple agents accessing common data

### **Tool Integration Approaches**
- **Built-in Tools**: Google-provided capabilities
- **Custom Functions**: Your own business logic
- **Agent Tools**: Wrapping agents as tools
- **External APIs**: Third-party service integration

## Running Examples

Each example can be run using the ADK CLI:

```bash
cd [example-directory]
adk web
```

Then:
1. Open the web UI (typically http://localhost:8000)
2. Select your agent from the dropdown
3. Start chatting with your agent

Alternative commands:
- `adk run [agent_name]` - Terminal interaction
- `adk api_server` - API server mode

## Production Considerations

### **Database Storage**
- Replace `InMemorySessionService` with `DatabaseSessionService`
- Support for PostgreSQL, MySQL, SQL Server
- Connection pooling and security
- Backup and recovery strategies

### **Security & Compliance**
- API key management
- User authentication and authorization
- Content filtering and safety policies
- Audit logging and monitoring

### **Scalability**
- Load balancing across multiple agents
- Caching strategies for performance
- Resource optimization
- Error handling and recovery

### **Monitoring & Observability**
- Performance metrics and analytics
- Request/response logging
- Agent behavior tracking
- Cost monitoring and optimization

## Additional Resources

### **Official Documentation**
- [ADK Documentation](https://google.github.io/adk-docs/)
- [Sessions and State Management](https://google.github.io/adk-docs/sessions/session/)
- [Multi-Agent Systems](https://google.github.io/adk-docs/agents/multi-agent-systems/)
- [Workflow Agents](https://google.github.io/adk-docs/agents/workflow-agents/)

### **Tool Documentation**
- [Built-in Tools](https://google.github.io/adk-docs/tools/built-in-tools/)
- [Function Tools](https://google.github.io/adk-docs/tools/function-tools/)
- [Callbacks](https://google.github.io/adk-docs/callbacks/)

### **Integration Guides**
- [LiteLLM Integration](https://google.github.io/adk-docs/tutorials/agent-team/#step-2-going-multi-model-with-litellm-optional)
- [Structured Data Exchange](https://google.github.io/adk-docs/agents/llm-agents/#structuring-data-input_schema-output_schema-output_key)

---

## Next Steps

1. **Start with 01-basic-agent** to understand the fundamentals
2. **Progress through each example** following the learning path
3. **Experiment with modifications** to understand the concepts deeply
4. **Build your own agents** combining multiple patterns
5. **Deploy to production** using the advanced concepts learned

Happy building with ADK! 🚀

---

*This project is based on the comprehensive tutorial by @aiwithbrandon. For additional support and community discussions, check out the [ADK documentation](https://google.github.io/adk-docs/) and related resources.*