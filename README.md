# Model Evaluation Workshop
Accuracy scores and leaderboard metrics look impressive—but production-grade AI requires evals that reflect real-world performance, reliability, and user happiness. Traditional benchmarks rarely help you understand how your LLM will perform when embedded in complex workflows or agentic systems. How can you realistically and adequately measure reasoning quality, agent consistency, MCP integration, and user-focused outcomes?

In this practical, example-driven workshop, we'll go beyond standard benchmarks and dive into tangible evaluation strategies using various open-source frameworks like GuideLLM and lm-eval-harness. You'll see concrete examples of how to create custom eval suites tailored to your use case, integrate human-in-the-loop feedback effectively, and implement agent reliability checks that reflect production conditions. Walk away with actionable insights and best practices for evaluating and improving your LLMs, ensuring they meet real-world expectations—not just leaderboard positions!

## Preparing Your System
Follow the below instructions according to your system.

### Red Hat Enterprise Linux system on [RHDP](https://catalog.demo.redhat.com/catalog?search=agentic&item=babylon-catalog-prod%2Fsummit-2025.lb2806-agentic-ai.prod)
NVIDIA GPUs
- NVIDIA drivers are installed, but the NVIDIA container toolkit is needed.

### Install NVIDIA Container Toolkit

```bash
curl -s -L https://nvidia.github.io/libnvidia-container/stable/rpm/nvidia-container-toolkit.repo | sudo tee /etc/yum.repos.d/nvidia-container-toolkit.repo
sudo dnf config-manager --enable nvidia-container-toolkit-experimental
sudo dnf install -y nvidia-container-toolkit podman
sudo nvidia-ctk cdi generate --output=/etc/cdi/nvidia.yaml
```

