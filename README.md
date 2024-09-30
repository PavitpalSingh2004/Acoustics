# SIGNAL PROCESSING PROJECT - EE 229

### Project Overview
This project explores the use of impulse response (IR) to generate output audio from an input file using convolution techniques. The project demonstrates audio processing with room impulse response files to simulate different acoustic environments for stereo audio files.

### Key Concepts:
- **Stereo File**: Audio stored with two channels, one for the left ear and one for the right.
- **Input File**: The audio file that needs processing to simulate how it would sound in a given room. Example: *BheegiRegular.wav*.
- **Convolution**: The process of combining an audio input file with a room impulse response (RIR) to simulate how sound propagates in a space.
- **WAV File (.wav)**: Uncompressed, high-quality audio format commonly used for professional recordings.

### Tools and Software:
- **Scilab**: Used for convolution operations and signal processing.
- **FFT (Fast Fourier Transform)**: Used to accelerate convolution by transforming the input file and RIR into the frequency domain.

### Process:
1. **Loading Audio Files**: 
   - Input stereo file (*BheegiRegular.wav*).
   - Room Impulse Response (RIR) file.
   
2. **Convolution with Impulse Response**:
   - Custom Scilab code to perform convolution for each stereo channel using the room impulse response.
   - Faster calculations using built-in FFT-based convolution for more extensive operations.

3. **Normalization and Output**:
   - After processing, the output is normalized to prevent clipping.
   - Example Output Files:
     - *output1.wav* (First second of convolved audio using *BheegiRegular-part.wav*).
  
### Experimental Results:
Various RIR files were used to simulate different environments:

| RIR File                    | Output File               | Observations                                                                 |
|-----------------------------|---------------------------|------------------------------------------------------------------------------|
| *Five_Columns_Long_16k.wav*  | *Output_five_columns.wav*  | Smooth attenuation, clear words with no distinct echo.                       |
| *long_echo_hall_16k.wav*     | *Output_echo_hall.wav*     | Distinct echoes, simulates a large room with consecutive echoes.             |
| *parking_garage_16k.wav*     | *Output_parking.wav*       | Dominant first echo, simulating a parking garage environment.                |

### Future Work:
- **360° Binaural Room Impulse Response (BRIR)**: The next step involves using BRIR and Head-Related Transfer Function (HRTF) files to simulate 3D sound environments for more complex spatial audio.
- **SOFA File Analysis**: Using the SOFA toolbox in MATLAB for spatially oriented acoustic data analysis.

### Sources:
- [Surround Sound in Headphones? HRTF & Binaural Audio Explained](https://audiouniversityonline.com/binaural-audio/)
- [360° Binaural Room Impulse Response (BRIR) Database](https://zenodo.org/records/2641166)
- [SOFA (Spatially Oriented Format for Acoustics)](https://www.sofaconventions.org/mediawiki/index.php/SOFA_(Spatially_Oriented_Format_for_Acoustics))

--- 
