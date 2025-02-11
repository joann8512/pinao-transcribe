# piano-transcribe
Original code is provided by the team from ByteDance [[pdf](https://arxiv.org/pdf/2010.01815.pdf), [code](https://github.com/bytedance/piano_transcription)]  


## Usage

1. Install dependencies:  

```
pip install -r requirements.txt
```
* Different versions of packages may result in errors when running.

2. You may want to change the designated GPU for transcription in `inference.py`  

3. If you have multiple GPUs to run, you can either:  
    - Uncomment lines 58-62 in `piano_transcription_inference/inference.py` to run parallel on multiple GPUs for faster transcription  
    - Run with the original package directly:   
    ```
    pip install piano_transcription_inference
    ```

4. To start transcribing with pre-trained model:  
    - Set the `audio_path` to the directory of audio files, the transcribed result will then all be saved to a new directory `midi`
    ```
    python transcribe.py --audio_path <audio_folder> --output_midi_path ./midi
    ```
    - If running into the error of `audioread.exceptions.NoBackendError`, install ffmpeg with conda:
    ```
    conda install ffmpeg
    ```
