# ConverAIlabs
Sales Call Analysis
This notebook provides an example of how to analyze a sales call recording using a combination of open-source libraries for transcription, speaker diarization, and sentiment analysis. The goal is to extract key insights from the conversation, such as talk time distribution, identified questions, longest monologues, and overall sentiment.

Libraries Used
1.yt-dlp: For downloading audio (though not explicitly used in the provided notebook, it was installed).
2.openai-whisper: For transcribing the audio into text.
3.pyannote.audio: For speaker diarization (identifying who spoke when).
4.torch and torchaudio: Dependencies for pyannote.audio.
5.transformers: For performing sentiment analysis on the transcribed text.


Notebook Structure:-

The notebook is structured into several steps:

1.Installation of Libraries: Installs necessary Python packages.
2.Import Libraries: Imports the required libraries.
3.Upload Audio File: Allows the user to upload an audio file for analysis.
4.Audio Transcription: Uses the Whisper model to transcribe the uploaded audio.
5.Speaker Diarization: Uses pyannote.audio to identify speaker segments in the audio.
6.Combine Transcription and Diarization: Merges the transcription and diarization results to 7.create a transcript with speaker labels.
8.Calculate Talk Time: Calculates the total talk time for each identified speaker and the talk time ratio.
8.Identify Questions: Attempts to identify questions within the transcribed text based on punctuation and common question starters.
9.Identify Longest Monologue: Determines the longest continuous speaking segment for each speaker.
10.Sentiment Analysis: Uses a pre-trained transformer model to analyze the overall sentiment of the conversation.
11.Identify Speaker Roles (Educated Guess): Attempts to assign roles (e.g., Sales Rep, Customer) based on talk time and keywords in the longest monologues.
11.Generate Actionable Insight: Provides a basic actionable insight based on the analysis results.
12.Summarize Analysis: Prints a summary of the key findings.

How to Use:-

1.Run the notebook: Execute each code cell sequentially.
2.Upload your audio file: When prompted, upload the sales call audio file you want to analyze (e.g., in WAV format).
3.Review the output: The notebook will print the transcription with speaker labels, talk time analysis, identified questions, longest monologues, overall sentiment, and an actionable insight.
4.Limitations and Potential Improvements
5.Speaker Identification Accuracy: The speaker role identification is an educated guess based on simple heuristics and may not be accurate for all recordings. More sophisticated methods or manual labeling would be needed for definitive speaker identification.
6.Transcription and Diarization Alignment: The method for combining transcription and diarization is simplified and may not perfectly align the text with the speaker segments, especially in cases of overlapping speech or rapid turn-taking.
7.Sentiment Analysis Granularity: The sentiment analysis is performed on the entire transcript. Analyzing sentiment on a per-speaker or per-segment basis could provide more detailed insights.
8.Actionable Insights: The generated actionable insight is a basic example. More advanced analysis and domain knowledge could be used to generate more specific and valuable insights.
9.Handling Different Audio Formats: The current notebook assumes a WAV file. Adding support for other audio formats would require additional libraries or conversion steps.
10.This notebook serves as a starting point for sales call analysis. It can be extended and improved by incorporating more advanced techniques for each stage of the pipeline.

finally our call quality analyzer build by google colab.
