# Memory Vector Pruner

![vector-db](https://img.shields.io/badge/vector--db-blue?style=flat-square) ![memory](https://img.shields.io/badge/memory-blue?style=flat-square) ![rag](https://img.shields.io/badge/rag-blue?style=flat-square)

A utility to intelligently prune irrelevant embeddings from an agent's long-term memory.

## Overview
Memory Vector Pruner is a specialized tool designed to optimize RAG-based systems by cleaning up "noisy" or obsolete vector data. It analyzes embedding relevance over time, allowing AI agents to maintain high-performance long-term memory without the overhead of redundant or low-signal information.

## Features
*   **Relevance Scoring:** Automatically evaluates and ranks embeddings based on access frequency and semantic importance.
*   **Threshold-Based Pruning:** Configurable logic to remove vectors that fall below a specific similarity or utility score.
*   **Context Preservation:** Ensures that core historical data is protected from deletion during cleanup cycles.
*   **Vector DB Integration:** Seamlessly interfaces with popular vector databases to perform in-place memory optimization.

## Installation
Clone the repository and install the necessary dependencies using pip:

```bash
git clone https://github.com/yourusername/memory-vector-pruner.git
cd memory-vector-pruner
pip install -r requirements.txt
```

## Usage
Run the pruner via the CLI by specifying your target database configuration and the pruning threshold.

```bash
python main.py --db-path ./vectors --threshold 0.75 --dry-run
```

Example logic in Python:
```python
from pruner import MemoryOptimizer

optimizer = MemoryOptimizer(database_url="your_db_url")
optimizer.prune(threshold=0.8) # Removes low-relevance vectors
```

## Contributing
We welcome contributions to improve the pruning algorithms and database connectors. Please submit a Pull Request with a clear description of your changes, ensuring that all new code is accompanied by relevant unit tests.

## License
This project is licensed under the [MIT License](LICENSE).