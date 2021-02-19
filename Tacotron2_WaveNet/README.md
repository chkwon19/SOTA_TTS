**Tacotron-2**  
Paper:   [Natural TTS Synthesis By Conditioning Wavenet on Mel Spectogram Predictions](https://arxiv.org/pdf/1712.05884.pdf)  

**WaveNet**  
Paper:   [WaveNet: A Genarative Model For Raw Audio](https://arxiv.org/pdf/1609.03499.pdf)   

**Audio Sample**  
[sample1](https://chkwon19.github.io/Tacotron2_WaveNet/synth12.wav)	[sample2](https://chkwon19.github.io/Tacotron2_WaveNet/synth14.wav)   

```python
# Range [0, 4] is used for training Tacotron2 but WaveNet vocoder assumes [0, 1]
mel = np.interp(mel, (0, 4), (0, 1))
```


