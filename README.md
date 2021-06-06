# Out-of-the-Box Test Sets for Validating Thai Automatic Speech Recognition System
This repository contains a collection of alternative Thai ASR test sets that we use to evaluate our Thai ASR project.  We think it might be useful for your Thai ASR project as well to alternatively use these test sets as out-of-the-box ones. All of the audios in this repo are in 1 channel WAV files, with 16000 samplerate. <br> 

*Some of test sets are collected from Mozilla Common Voice TH and SER dataset from VISTEC-depa.* <br>

We also report word-error-rate results of each test set transcribed by our models. Output transcription of out model can be seen in `output_samples` folder. To keep WER consistent across test sets, we used [ThaiNLP](https://github.com/PyThaiNLP/pythainlp) to tokenize both reference and output transcriptions before calculating WER by [jiwer](https://github.com/jitsi/jiwer/). 
## 1. Download Test Sets
| Test Set | Description | Source | License |
| --- | --- | --- | --- | 
| [CommonVoice2000](https://drive.google.com/file/d/1myysV4yEePSt365op1AvRz8YdgqEaokJ/view?usp=sharing) | A collection of 2000 audios randomly selected from CommonVoiceTH | [Mozilla Common Voice](https://commonvoice.mozilla.org/th) | CC0 1.0 |
| [Male_Voice](https://drive.google.com/file/d/14mQTeThZ4DdjiTXAE_BOXfxcjFbMTpCW/view?usp=sharing) | A collection of 44 audios from 22 male speakers speaking the same sentence  | [VISTEC-depa](https://airesearch.in.th/releases/speech-emotion-dataset/) |CC BY-SA 4.0 |
| [Female_Voice](https://drive.google.com/file/d/1tWy44dm_Nk-qOhjED4fWvPArLmzLEeki/view?usp=sharing) | A collection of 44 audios from 22 female speakers speaking the same sentence as in Male_Voice.| [VISTEC-depa](https://airesearch.in.th/releases/speech-emotion-dataset/) | CC BY-SA 4.0 |
| [Piyabutr_Interview](https://drive.google.com/file/d/1ZJy2IJxmsBaO9co3gfIUowuILf7gHjnz/view?usp=sharing) | A collection of 33 audios from one of Piyabutr’s interviews with somewhat noisy environment.   | |
| [Piyabutr_with_Music_BG](https://drive.google.com/file/d/1hJumoQqLQGq372MwtusjWzzJsnNSE24p/view?usp=sharing) | A collection of 7 audios from a political advertisement clip, a male speaker (Piyabutr Saengkanokkul), with upbeat music on the background.  | |
| [Obodroid](https://drive.google.com/file/d/1g5nujRWk46rDjv9LzJrCA60P2Tnjwl6N/view?usp=sharing) | A collection of 9 audios with clear speech from a male speaker talking about Obodroid’s products. | |
| [Reporter](https://drive.google.com/file/d/18lbI1hhZngaPiDBMmnsgyhuxMRA-L0b8/view?usp=sharing)| A collection of 19 audios from more than 15 Thai reporters. Each audio comes from difference news programs. Length of audios varies from 8 seconds to 1 minute. The topics cover daily news, weather, sport, politic etc.  | |

## 2. Benchmarks
| Model / WER(%) | CommonVoice2000 | Reporter | Piyabutr_Interview | Piyabutr_with_Music_BG | MaleVoice | FemaleVoice | Obodroid | 
| --- | --- | --- | --- | --- | --- | --- | --- | 
| DeepSpeech 300 hrs  | 31.78 | 21.91 | 38.10 | 43.54 | 26.87 | 22.19 | 16.02 |
| DeepSpeech 330 hrs | 32.1 | 21.02 | 35.83 | 42.31 | 28.07 | 29.81 | 11.57| 

* Numbers after the model indicate the size of (private) dataset which the model was trained on.
* The models were decoding with external KenLM (trained on ThaiSum dataset). 

## 3. Contributor 
- All test sets, except CommonVoice2000, were manually transcribed by [Nakhun Chumpolsathien](https://github.com/nakhunchumpolsathien).  