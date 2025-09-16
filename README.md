# Speaker Diarization 🔊

## Short description 🖊️

End-to-end speaker diarization pipeline answering **“who spoke when”** by combining pyannote (VAD, segmentation, embeddings), clustering (threshold / spectral), and Whisper for transcription. Produces time-stamped RTTM and a labeled transcript.

## Team (～￣▽￣)～

* Ngo Xuan Kien — 23BI14239
* Tran Gia Khanh — 23BI14218
* Ngo Minh Phuoc — 23BI14361
* Nguyen The Khai — 23BI14205

## Key components (one line each) 🗝️

* **Dataset:** VoxConverse (RTTM annotations).
* **Preprocessing:** mono 16 kHz conversion, basic denoising, segmentation.
* **Features:** neural speaker embeddings (pyannote) ± MFCC/log-mel.
* **Clustering:** threshold-based or spectral clustering on embeddings.
* **ASR:** Whisper (tiny) for transcripts.
* **Evaluation:** DER, JER, confusion & overlap analysis.

## Outputs 🤖

* `*.rttm` — standard time-stamped speaker segments.
* `labeled_transcript.txt` — speaker-labeled transcript.
* Visualizations: PCA / t-SNE of embeddings, confusion/distance histograms.

## Evaluation 📏

* Primary metric: **DER** (captures misses, false alarms, confusion).
* System handles overlap via VAD tuning and embedding-clustering design.
* Modular pipeline: VAD → Embedding → Clustering → ASR → Alignment (easy to swap modules).
 
## Important files 📃

* `run_diarization.py` (or notebook) — pipeline entry point
* `requirements.txt` — dependencies (pinned)
* `reports/` — DER and embedding visualizations

## Contact 🤙

See Team section above. Submitted: **September 2025**.
