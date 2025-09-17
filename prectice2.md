```mermaid
flowchart TD
    A[Prototype for Recording Noisy Audio] --> B[Data Collection: Noisy & Clean Audio (WAV 16kHz)]
    B --> C[Data Preprocessing: Segmentation & Normalization]
    C --> D[MetricGAN+ Training (Teacher Model, Metrics: PESQ, STOI)]
    D --> E[PNNoisy Training (Student Model, Optimized for On-Device Use)]
    E --> F[Prototype for Deployment (Hearing Aid + Microchip, TFLite/ONNX)]
    F --> G[Hearing Aid Real-Time Audio Output: Denoised & Amplified Sound]

    classDef device fill:#f9f,stroke:#333,stroke-width:2px;
    class A,F,G device;
    classDef model fill:#bbf,stroke:#333,stroke-width:2px;
    class D,E model;

```
