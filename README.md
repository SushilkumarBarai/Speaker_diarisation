# Speaker Diarization using Energy-based Clustering

## Overview
This Python script performs speaker diarization on an audio file, separating it into segments based on speaker changes. Speaker diarization is the process of partitioning an audio recording into homogeneous segments according to the speaker identity. The algorithm used here relies on energy-based feature extraction and K-means clustering.

## Requirements
- Python 3.x
- NumPy
- SciPy
- scikit-learn
- pydub
- matplotlib

Install these dependencies using pip:


## Usage
1. Make sure you have your audio file in WAV format. If not, you may need to convert it to WAV.
2. Replace `'your_audio_file.wav'` in the code with the path to your audio file.
3. Set the `num_speakers` variable to the expected number of speakers in the audio file.
4. Run the script.

The script will output a JSON file containing speaker diarization information. Optionally, it can also display a plot showing speaker labels over time.

## Functionality
1. **load_audio(file_path)**:
   - Loads the audio file and converts it to mono with a 16kHz sampling rate.

2. **extract_features_with_time(chunk, start_time, end_time)**:
   - Extracts energy-based features from audio chunks along with their timestamps.

3. **generate_diarization_json(chunks, labels, features_with_time)**:
   - Generates speaker diarization JSON from clustered labels and time information.

4. **Optional Visualization**:
   - The script can visualize the speaker diarization results using a plot.

## Adjusting Parameters
- You can change the `chunk_length_ms` variable to adjust the duration of each audio chunk.
- Modify the `num_speakers` variable to match the expected number of speakers in your audio file.

## Output
The output JSON file contains the following information for each speaker segment:
- Speaker ID
- Start time
- End time

## Note
This script assumes that speaker changes are correlated with changes in audio energy. Adjustments may be necessary for different types of audio recordings.
