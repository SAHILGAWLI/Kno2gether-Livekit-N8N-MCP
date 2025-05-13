# Kno2gether-Livekit-N8N-MCP

![Kno2gether LiveKit MCP Integration](https://img.youtube.com/vi/CIYv59aJIv8/0.jpg)

This project is a fork of [basic-mcp](https://github.com/livekit-examples/basic-mcp) that showcases a powerful voice assistant using LiveKit Agents framework and n8n (Nodemation) with Multimodal Control Protocol (MCP) tools integration for external services.

## 🚀 Introducing Kno2gether LiveKit Integration

This project demonstrates how to build a voice AI assistant that can interact with external services through MCP tools. The assistant can understand natural language commands and perform actions using connected services.

### 🌟 Watch Our Tutorial

Learn how to build this project step-by-step in our detailed tutorial:

[![LiveKit Voice AI with n8n MCP Integration Tutorial](https://img.youtube.com/vi/CIYv59aJIv8/0.jpg)](https://www.youtube.com/watch?v=CIYv59aJIv8)

*Click the image above to watch the tutorial on YouTube*

## Features

- **Voice-based interaction** with a helpful AI assistant
- **Integration with MCP tools** from external servers (like n8n)
- **Speech-to-text** using Deepgram for accurate transcription
- **Natural language processing** using OpenAI's GPT-4o
- **Text-to-speech** using OpenAI for natural-sounding responses
- **Voice activity detection** using Silero
- **Real-time communication** powered by LiveKit

## Prerequisites

- Python 3.9+
- API keys for:
  - OpenAI (for LLM and TTS)
  - Deepgram (for STT)
- MCP server endpoint (n8n with MCP node)
- LiveKit server (Cloud or self-hosted)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/Kno2gether-Livekit-N8N-MCP.git
   cd Kno2gether-Livekit-N8N-MCP
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file with your API keys and configuration:
   ```
   OPENAI_API_KEY=your_openai_api_key
   DEEPGRAM_API_KEY=your_deepgram_api_key
   ZAPIER_MCP_URL=your_mcp_server_url
   ```

## Usage

Run the agent with the LiveKit CLI:

```bash
python agent.py console
```

The agent will connect to the specified LiveKit room and start listening for voice commands. It will use the MCP tools from the connected server to perform actions based on user requests.

## Project Structure

- `agent.py`: Main agent implementation and entrypoint
- `mcp_client/`: Package for MCP server integration
  - `server.py`: MCP server connection handlers
  - `agent_tools.py`: Integration of MCP tools with LiveKit agents
  - `util.py`: Utility functions for MCP client

## How It Works

1. **Voice Processing**: LiveKit and Deepgram convert your voice to text with high accuracy
2. **AI Understanding**: OpenAI's GPT-4o processes your requests and determines the appropriate actions
3. **Tool Integration**: MCP provides seamless access to external services through n8n
4. **Natural Response**: OpenAI TTS converts the AI's response to natural-sounding speech
5. **Real-time Communication**: LiveKit handles the WebRTC connection for low-latency audio

## Example Voice Commands

Once connected, you can have natural conversations with the assistant. The specific commands will depend on the MCP tools you've configured, but could include:

- "What's the weather like today?"
- "Send a message to my team about the meeting"
- "Create a new task in my project management tool"
- "Look up information about [topic]"

## Subscribe to Kno2gether

For more AI tutorials and projects like this one, subscribe to our [YouTube channel](https://www.youtube.com/@Kno2gether).

## Acknowledgements

- [LiveKit](https://livekit.io/) for the underlying real-time communication infrastructure
- [OpenAI](https://openai.com/) for GPT-4o and text-to-speech
- [Deepgram](https://deepgram.com/) for speech-to-text
- [Silero](https://github.com/snakers4/silero-vad) for Voice Activity Detection
- [n8n](https://n8n.io/) for workflow automation and MCP integration
- [basic-mcp](https://github.com/livekit-examples/basic-mcp) for the original codebase this project is forked from

## License

This project is licensed under the MIT License - see the LICENSE file for details.