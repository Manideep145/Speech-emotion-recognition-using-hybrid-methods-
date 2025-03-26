 (using ```mermaid ```)
     graph TD
    A[Speech Input (Audio Files)] --> B(Feature Extraction);
    B --> C{Hybrid Methods};
    C -- MFCCs --> D[Machine Learning Models (SVM, Random Forest, etc.)];
    C -- Spectrograms/Wavelets --> E[Deep Learning Models (CNN, RNN, etc.)];
    D --> F[Emotion Classification (ML)];
    E --> G[Emotion Classification (DL)];
    F --> H[Emotion Result];
    G --> H;
    subgraph "Feature Extraction"
    B[Feature Extraction]
    end
    subgraph "Hybrid Methods"
    C[Hybrid Methods]
    end
    subgraph "Machine Learning Branch"
    D[Machine Learning Models (SVM, Random Forest, etc.)]
    F[Emotion Classification (ML)]
    end
    subgraph "Deep Learning Branch"
    E[Deep Learning Models (CNN, RNN, etc.)]
    G[Emotion Classification (DL)]
    end
    subgraph "Output"
    H[Emotion Result]
    end
