## Training Features

- **Early Stopping**: Patience of 6 epochs with best weights restoration
- **Learning Rate Reduction**: Factor of 0.5 with patience of 3 epochs, min_lr=1e-5
- **Regularization**: 
  - Dropout layers (0.2 spatial, 0.5 dense)
  - Label smoothing (0.05)
  - Weight decay (AdamW optimizer)

## Optimizer Configuration

All models use AdamW optimizer with:
- Learning rate: 1e-3
- Weight decay: 1e-3 (BiRNN, BiGRU, Conv1D), 1e-2 (BiLSTM)
- Binary crossentropy loss with label smoothing (0.05)

## Test Set Performance

After training on the IMDB dataset, here are the typical results on the test set:

| Model | Test Loss | Test Accuracy |
|-------|-----------|---------------|
| **Bidirectional RNN** | 0.3341  | 0.8870 |
| **Bidirectional LSTM** | 0.3168  | 0.9004 |
| **Bidirectional GRU** | 0.3034 | 0.9012 |
| **Conv1D** | 0.3229 | 0.8990 |

## Traning vs Validation loss

<Figure size 640x480 with 1 Axes><img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/535f2597-0d93-4069-8a8d-0b217fbd7cae" />
<Figure size 640x480 with 1 Axes><img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/c734d205-5bd3-4f0e-b974-fbffd5de0b33" />
<Figure size 640x480 with 1 Axes><img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/79665c19-c274-4362-9104-7fd930dcbb3a" />
<Figure size 640x480 with 1 Axes><img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/c8386b42-e875-4d21-a01c-5e543af85b1e" />
