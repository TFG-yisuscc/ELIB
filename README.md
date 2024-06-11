# ELIB - Edge LLM Inference Benchmarking Tool
- With the significant success achieved by large language models (LLMs) like ChatGPT and LLaMA, cloud computing-based LLM inference services have consistently presented challenges for users in specific scenarios due to data privacy and latency concerns. Different edge platforms have varying characteristics, making it very challenging to deploy and benchmark LLMs, which require large memory capacity and high computing power.

- To address these challenges, we introduce ELIB (Edge LLM Inference Benchmarking), a comprehensive tool designed to evaluate the overall LLM inference performance of different edge computing platforms. ELIB provides a collection of comprehensive metrics to describe the benchmarking results and offers insights to guide the future work of inference LLMs on edge computing platforms.


## Features
- Cross-Platform Benchmarking: Deploy ELIB on PC, Mobile, and IoT edge platforms.
- Quantized Models: Utilize five carefully quantized models for accurate benchmarking.
- Comprehensive Metrics: Evaluate and analyze performance using a set of comprehensive metrics.
- Practical Insights: Obtain practical insights to guide future developments in LLM inference on edge platforms.

## Advantages
- Simple structure, easy to get started and learning, and decoupled the framework part from the kernel part.
- Defined a KVstorage type for easy caching and management.
- High efficiency, ported most of the kernels in llama.cpp.
- Compatible with multiple LLaMA family model formats.
- Supports CPU and GPU, optimized for Arm.
- Can be deployed on IOT, mobile phones, PC, with acceptable speed.

## How to
Currently, ELIB utilizes the same models as llama.cpp and can download the original models from the llama.cpp project. Additionally, quantized models are available for direct download from HuggingFace [/paiphd/ELIB](https://huggingface.co/paiphd/ELIB/tree/main). The provided quantized models include q4_0, q4_1, q5_0, q5_1, and q8_0. Please put these files in /models folder.

## Compile
```shell
git clone https://github.com/hchenphd/ELIB.git
cd ELIB/cmake
mkdir build
cd build
cmake ..
make
```

## Usage
ELIB can be deployed and used to benchmark LLM inference performance on different edge platforms. Below are the basic usage instructions:

### FLOPS benchmarking
```shell
./flops_matmult -t <threads> -i <iterations>
```

### Throughput and Latency benchmarking
```shell
./throughput_latency -m <model_name> -p <prompt> -ngl <GPU acceleration>
```

### Accuracy 
```shell
./throughput_latency -m <model_name> -p <prompt> -ngl <GPU acceleration>
```

### License
Apache Licens 2.0



