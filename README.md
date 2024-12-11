"""
# Self-hosted AI Starter Kit (CUDA GPU Fork) - On Ubuntu 


1. Install docker - https://docs.docker.com/engine/install/ubuntu/
2. Enable Docker to access the CUDA https://runs-on.com/blog/3-how-to-setup-docker-with-nvidia-gpu-support-on-ubuntu-22/
3. copy the YML file and run: 'docker compose up'

Check with:
' ollama list ' if the models have been dowmloaded. If not you have to run this to pull the models with one line

'docker exec ollama ollama pull nomic-embed-text && docker exec ollama ollama pull llama3.2'

ONLY UPDATED THE DOCKER COMPOSE FILE SO IT WILL INSTALL EVERYTHING


Thanks to 
https://dev.to/ajeetraina/running-ollama-with-docker-compose-and-gpus-lkn
for the YML update
And Deepseek chat for applying it :)

This is a GPU-optimized fork of the **Self-hosted AI Starter Kit**, designed for CUDA-enabled systems. It combines n8n, Ollama, Qdrant, and PostgreSQL to create a powerful local AI development environment.

![n8n.io - Screenshot](https://raw.githubusercontent.com/n8n-io/self-hosted-ai-starter-kit/main/assets/n8n-demo.gif)

### What’s included

✅ **n8n** - Low-code platform with AI workflows  
✅ **Ollama** - GPU-accelerated LLM inference  
✅ **Qdrant** - High-performance vector database  
✅ **PostgreSQL** - Reliable database for data storage  

### What you can build

⭐️ AI Agents for scheduling and automation  
⭐️ Secure document summarization and analysis  
⭐️ Custom Slack bots and private financial analysis  

---

## Installation

### For CUDA GPU users

```bash
git clone https://github.com/HyperUpscale/self-hosted-ai-starter-kit.git
cd self-hosted-ai-starter-kit
docker compose up
```


## ⚡️ Quick Start

1. Open <http://localhost:5678/> in your browser to set up n8n. You’ll only
   have to do this once.
2. Open the included workflow:
   <http://localhost:5678/workflow/srOnR8PAY3u4RSwb>
3. Select **Test workflow** to start running the workflow.
4. If this is the first time you’re running the workflow, you may need to wait
   until Ollama finishes downloading Llama3.2. You can inspect the docker
   console logs to check on the progress.


To open n8n at any time, visit <http://localhost:5678/> in your browser.



### Local AI templates

- [Tax Code Assistant](https://n8n.io/workflows/2341-build-a-tax-code-assistant-with-qdrant-mistralai-and-openai/)
- [Breakdown Documents into Study Notes with MistralAI and Qdrant](https://n8n.io/workflows/2339-breakdown-documents-into-study-notes-using-templating-mistralai-and-qdrant/)
- [Financial Documents Assistant using Qdrant and](https://n8n.io/workflows/2335-build-a-financial-documents-assistant-using-qdrant-and-mistralai/) [Mistral.ai](http://mistral.ai/)
- [Recipe Recommendations with Qdrant and Mistral](https://n8n.io/workflows/2333-recipe-recommendations-with-qdrant-and-mistral/)

## Tips & tricks

### Accessing local files

The self-hosted AI starter kit will create a shared folder (by default,
located in the same directory) which is mounted to the n8n container and
allows n8n to access files on disk. This folder within the n8n container is
located at `/data/shared` -- this is the path you’ll need to use in nodes that
interact with the local filesystem.

**Nodes that interact with the local filesystem**

- [Read/Write Files from Disk](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.filesreadwrite/)
- [Local File Trigger](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.localfiletrigger/)
- [Execute Command](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.executecommand/)

## 📜 License

This project is licensed under the Apache License 2.0 - see the
[LICENSE](LICENSE) file for details.

## 💬 Support

Join the conversation in the [n8n Forum](https://community.n8n.io/), where you
can:

- **Share Your Work**: Show off what you’ve built with n8n and inspire others
  in the community.
- **Ask Questions**: Whether you’re just getting started or you’re a seasoned
  pro, the community and our team are ready to support with any challenges.
- **Propose Ideas**: Have an idea for a feature or improvement? Let us know!
  We’re always eager to hear what you’d like to see next.
