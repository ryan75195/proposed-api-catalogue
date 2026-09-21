# Caption & Transcribe

Producing captions for video and transcripts for interviews is manual and slow, and edited transcripts often lose the speaker labels people need.

Caption & Transcribe turns an uploaded audio or video file into a timed transcript with speaker labels. A call to POST /transcribe with a file reference returns { "segments": [{ "start": 0.0, "end": 3.2, "speaker": "A", "text": "..." }], "format": "srt" }.

Limits: transcription accuracy depends on audio quality and speakers; results may need editing and are not a legal record or certified transcript.

This is a proposed design and is not implemented.

Segments carry start and end times relative to the media so they can be emitted as captions or a timed transcript. Output should be reviewed before publication.

A typical caller is a media team adding captions before publishing a talk. Speaker labels and timing make the output directly usable for subtitles.

The format field requests srt or a plain timed list so the caller picks the shape it needs.
