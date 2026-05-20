# Audio Notary 

Audio Notary is an advanced acoustic forensics and speaker verification system built with Flask. The application analyzes uploaded audio files through a multi-layered security pipeline to detect synthetic voice clones (deepfakes), uncover file tampering/splicing anomalies, and verify speaker identity using neural embeddings paired with classic acoustic features.

##  System Architecture

The platform processes audio using a **three-layer defense matrix** to evaluate the authenticity of an audio file:

1. **Layer 1: Metadata & Splice Integrity** — Inspects containers, editing signatures, structural anomalies, and abrupt silence points indicating splicing or stitching.
2. **Layer 2: Biological Feature Analysis** — Measures micro-acoustic biological markers unique to human vocal cords (e.g., Shimmer, Pitch Jitter, Spectral Flatness, and Harmonic-to-Noise Ratio).
3. **Scoring Engine** — Fuses findings into a comprehensive **Weighted Trust Score** and outputs a color-coded security verdict.
4. **Speaker Verification** — Cross-matches speaker identities by ensembling neural embeddings (SpeechBrain ECAPA-TDNN) and timbral baselines (MFCC).

Tech Stack

Core Web & API Layer
Signal Processing & Forensics Layer
Deep Learning & Identity Core


System Features

- Deepfake voice detection
- Audio tampering & splice analysis
- Speaker verification
- Weighted trust scoring
- Neural embedding analysis
- MFCC-based acoustic matching


Installation 

1 Windows

Install the required audio dependency using one of the following methods:

Using Conda (Recommended)
conda install -c conda-forge libsndfile

Linux (Ubuntu/Debian)
sudo apt-get update
sudo apt-get install -y libsndfile1

macOS (Homebrew)
brew install libsndfile

2 Clone and Initialize Virtual Environment
git clone https://github.com/Yashu123403/audio-notary.git
cd audio-notary
python -m venv venv




3 Activate virtual environment
# On macOS/Linux:
source venv/bin/activate
# On Windows:
venv\Scripts\activate

4 Install Project Dependencies
pip install -r requirements.txt

5 Run the Application

Start the local Flask development server:
python app.py

AUTHOR 
YASHU AB
