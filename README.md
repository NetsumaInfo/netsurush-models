# NetsuRush models

Model files downloaded by the NetsuRush Mobile app. Files are attached to the [releases](../../releases).

| File | Use | Source | License |
|---|---|---|---|
| `face_detection_yunet_2023mar.onnx` | Real face detection | [OpenCV Zoo](https://github.com/opencv/opencv_zoo/tree/main/models/face_detection_yunet) | MIT |
| `face_recognition_sface_2021dec.onnx` | Real face recognition | [OpenCV Zoo](https://github.com/opencv/opencv_zoo/tree/main/models/face_recognition_sface) | Apache-2.0 |
| `anime_face_detect_v1.4_s_w8a16.onnx` | Anime face detection | [deepghs/anime_face_detection](https://huggingface.co/deepghs/anime_face_detection) | MIT |
| `ccip_caformer_24_w8a16.onnx` | Anime character recognition | [deepghs/ccip_onnx](https://huggingface.co/deepghs/ccip_onnx) | OpenRAIL |
| `ccip_metrics.onnx` | Anime character comparison | [deepghs/ccip_onnx](https://huggingface.co/deepghs/ccip_onnx) | OpenRAIL |
| `siglip2_base_image_w8a16.onnx` | Shot search, image side | [qualcomm/SigLIP2](https://huggingface.co/qualcomm/SigLIP2) (base 224) | Apache-2.0 |
| `siglip2_base_text_w8a16.onnx` | Shot search, text side | [qualcomm/SigLIP2](https://huggingface.co/qualcomm/SigLIP2) (base 224) | Apache-2.0 |
| `siglip2_base_w8a16_metadata.json` | Input and output quantization of the two search models | [qualcomm/SigLIP2](https://huggingface.co/qualcomm/SigLIP2) | Apache-2.0 |
| `siglip2_tokenizer.json` | Search text tokenizer | [google/siglip2-so400m-patch16-naflex](https://huggingface.co/google/siglip2-so400m-patch16-naflex) | Apache-2.0 |
| `siglip2_text_vocab_remap.i32` | Tokenizer id to pruned model id (int32, -1 = dropped) | Derived | Apache-2.0 |

`w8a16` files are quantized (8-bit weights, 16-bit activations) for phone NPUs. The search text model keeps only Latin-script tokens: map tokenizer ids through `siglip2_text_vocab_remap.i32` before running it. Quantized weights are stored as integers; results are identical to the original files.
