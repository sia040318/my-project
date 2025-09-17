flowchart TD
    A[Prototype for Recording Noisy Audio<br/>(Microphone + Simple Hearing Aid)] --> B[Data Collection<br/>Noisy & Clean Audio (WAV, 16kHz)]
    B --> C[Data Preprocessing<br/>Segmentation & Normalization]
    C --> D[MetricGAN+ Training<br/>(Teacher Model)<br/>Metrics: PESQ, STOI]
    D --> E[PNNoisy Training<br/>(Student Model)<br/>Optimized for On-Device Use]
    E --> F[Prototype for Deployment<br/>(Hearing Aid + Microchip/Processor)<br/>TFLite/ONNX Model)]
    F --> G[Hearing Aid Real-Time Audio Output<br/>Noisy → Denoised & Amplified Sound]

    %% Optional icons
    classDef device fill:#f9f,stroke:#333,stroke-width:2px;
    class A,F,G device;
    classDef model fill:#bbf,stroke:#333,stroke-width:2px;
    class D,E model;
