## State-Of-The-Art TTS

- 딥러닝 기반 종단간(end-to-end) TTS 시스템은 다음 두 가지 과정으로 구성
    - 텍스트에서 스펙트로그램을 생성하는 Text2Mel 과정 
        - Tacotron2, Transformer 등  
    - 스펙트로그램에서 음성신호를 합성하는 보코더 
        - WaveGlow, WaveNet, WaveRNN, ParallelWaveGAN 등  
- Text2Mel의 출력과 보코더의 입력인 멜 스펙트로그램 정규화 일치 작업 필요  
    - ex) Tacotron2 - WaveNet  
    - ```python
    # Tacotron2 : range [0, 4],  WaveNet : range [0, 1]
    mel = numpy.interp(mel, (0, 4), (0, 1))
      ```