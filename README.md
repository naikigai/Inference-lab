# Inference-lab

An attempt to learn Inference Engineering

# Together AI

Core requirements (all levels)

- Go, Python or Rust, with typed, tested code shipped via CI/CD
- Durable workflow orchestration: Temporal, Cadence
- Control planes that model state and reconcile it, like Kubernetes controllers/operators and custom reconciliation loops
- Event-driven systems: Kafka, NATS, SQS (not polling or cron)
- Product mindset: internal platforms or APIs used by other engineering teams

What you'd build

- A provisioning state machine: host discovery → GPU driver/CUDA bring-up → health validation → decommission/RMA
- A declarative self-service API: one call to stand up, scale or tear down an inference cluster
- Self-healing: detect bad nodes, drain them, repair, return them to the pool
- Reliability work: idempotency, retries, rollback, drift detection

Nice to have

- Bare-metal provisioning: PXE/iPXE, Redfish/IPMI, BMC
- Networking: VLANs, BGP
- GPU stack: NCCL, CUDA, InfiniBand/RoCE
- Systems programming in Rust or Go


# Let's build GPT: from scratch, in code, spelled out
- https://www.youtube.com/watch?v=kCc8FmEb1nY
- It all started with paper 'Attention is all you need' - https://arxiv.org/abs/1706.03762
- https://huggingface.co/datasets/karpathy/tiny_shakespeare - we are going to build a transformer model that will be trained on shakespeare work
- https://github.com/karpathy/nanogpt - So code for training transformers is here .
- ok there are two file , train.py and model.py - about 300 lines each , which we will use to create a transformer almost as good as gpt 2
- we first read all the text into a string
- then we see how many diff chars are there
- total 65 were there
- then we take those 65 map each char to the integer(in our case, it was mapped to index) , then we have this encoding and decoding which does char to int and vice versa
- In practice however , diff algo are use for this purpose
- For example, SentencePiece by google - https://github.com/google/sentencepiece and tiktoken  - https://github.com/openai/tiktoken
- tiktoken is by openAI. GPT uses it.
- we never feed entire text to transformer all at once , that would be too heavy , instead we train it on chunks
- Chunk_size or block_size or context_size - you will see diff names for this vaiable.
- block_size is what we'll use
- 
