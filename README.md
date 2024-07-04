# PodBriefs - A Podcast Summarizer

This project automatically summarizes podcast episodes using their RSS feed URLs. By leveraging AI models, it extracts key points and presents a concise summary.

## Project Demo

<div align="center">
   <img src="content/podcast/podcast.gif" width="100%" max-width="800"/>
</div>

### Demo Walkthrough

In the demo, you can see the following steps:

1. Launch the application and navigate to the main screen.
2. Obtain an RSS feed URL for a podcast from [Listen Notes](https://www.listennotes.com) or [Castos](https://castos.com/tools/find-podcast-rss-feed/).
3. Enter the RSS feed URL for the desired podcast episode.
4. Click the "Process a Podcast Feed" button.
5. The application downloads the podcast episode as an MP3 file.
6. The WhisperX model transcribes the audio to text.
7. The ChatGPT 3.5 Turbo model generates a summary from the text.
8. These processes run on the [Modal](https://modal.com) backend using GPU.
9. The summary, along with episode details, guest info, and highlights, is displayed on the [Streamlit](https://streamlit.io) frontend.

Explore the interface and create summaries for your favorite podcasts!

## Features

- **Automated Summarization:** AI-driven process to download, transcribe, and summarize podcast episodes.
- **WhisperX for Transcription:** Converts spoken content into text.
- **ChatGPT 3.5 Turbo for Summarization:** Provides coherent summaries from the transcribed text.
- **Streamlit Frontend:** User-friendly interface displaying summaries, episode details, guest information, and highlights.


## Installation

To run this project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/tekeburak/podcast-summarizer.git
   cd podcast-summarizer

2. Install the required dependencies using pip:
   ```bash
   pip install streamlit modal

3. Deploy backend to Modal:
   ```bash
   modal deploy /content/podcast/podcast_backend.py

4. Run the Streamlit app:
   ```bash
   streamlit run podcast_frontend.py

### Usage Intrustions

1. Access the Streamlit frontend by opening a web browser and navigating to [http://localhost:8501](localhost:8501).
2. On the homepage, you'll find an input field where you can paste the RSS feed URL of the podcast you want to summarize.
3. Click the "Process a Podcast Feed" button to initiate the summarization process.
4. The app will start by downloading the podcast episode in mp3 format and then use the WhisperX model to transcribe the speech to text.
5. Once transcribed, the text data is fed into the ChatGPT 3.5 Turbo model to generate a summary.
6. The summary, along with episode details, guest information, and highlights, will be displayed on the Streamlit interface.

## Contributing

1. Fork the repository.
2. Create a new branch for your feature: `git checkout -b feature-name`.
3. Implement your feature and make necessary changes.
4. Commit and push your changes: `git commit -m "Add feature" && git push origin feature-name`.
5. Submit a pull request detailing the changes you've made.

## License

This project is licensed under the [MIT License](LICENSE).
