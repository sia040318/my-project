```mermaid
flowchart TD
    A[Prototype for Recording Noisy Audio\n(Microphone + Simple Hearing Aid)] --> B[Data Collection\nNoisy & Clean Audio (WAV, 16kHz)]
    B --> C[Data Preprocessing\nSegmentation & Normalization]
    C --> D[MetricGAN+ Training\n(Teacher Model)\nMetrics: PESQ, STOI]
    D --> E[PNNoisy Training\n(Student Model)\nOptimized for On-Device Use]
    E --> F[Prototype for Deployment\n(Hearing Aid + Microchip/Processor)\nTFLite/ONNX Model]
    F --> G[Hearing Aid Real-Time Audio Output\nNoisy → Denoised & Amplified Sound]

    %% Optional styling
    classDef device fill:#f9f,stroke:#333,stroke-width:2px;
    class A,F,G device;
    classDef model fill:#bbf,stroke:#333,stroke-width:2px;
    class D,E model;
```
