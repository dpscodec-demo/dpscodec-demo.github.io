# Audio Decoding by Inverse Problem Solving

This is the demonstration page of the paper "Audio Decoding by Inverse Problem Solving" with the samples used for the MUSHRA-style listening tests.

## Info

### Abstract

We consider audio decoding as an inverse problem and solve it through diffusion posterior sampling. Explicit conditioning functions are developed for input signal measurements provided by an example of a transform domain perceptual audio codec. Viability is demonstrated by evaluating arbitrary pairings of a set of bitrates and task-agnostic prior models. For instance, we observe significant improvements on piano while maintaining speech performance when a speech model is replaced by a joint model trained on both speech and piano. With a more general music model, improved decoding compared to legacy methods is obtained for a broad range of content types and bitrates. The noisy mean model, underlying the proposed derivation of conditioning, enables a significant reduction of gradient evaluations for diffusion posterior sampling, compared to methods based on Tweedie's mean. Combining Tweedie's mean with our conditioning functions improves the objective performance.

### Reference

Pedro J. Villasana T., Lars Villemoes, Janusz Klejsa, Per Hedelin  (2024). **Audio Decoding by Inverse Problem Solving**.

## MUSHRA items

We evaluate the proposed methodology on Speech (using the VCTK dataset [1]), Piano (using the Supra dataset [2]), and Critical (using the ODAQ dataset [3]) audio signals.

Two MUSHRA-like listening tests were conducted to compare the legacy decoding method (DEC) against the proposed diffusion-based decoding algorithm (INV). The audio signals of both tests were encoded at 16 kb/s. Also included in the tests were a hidden reference and a 3.5 kHz lowpass anchor (LP35).

These items were never seen during training.

### Model Test

This section contains the 9 items used in the first MUSHRA-style listening test.

<html>
<table>

  <tr>
    <th>Item</th>
    <th>REF</th>
    <th>DEC</th>
    <th>INVspeech</th>
    <th>INVjoint</th>
    <th>INVmusic</th>
    <th>LP35</th>
  </tr>

  <tr>
    <td>Speech 1</td>
    <td>
      <audio controls>
        <source src="./ModelTest/REF/p237_298_mic2res0_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/DEC/p237_298_mic2res0_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVspeech/p237_298_mic2res0_dps_speech_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVjoint/p237_298_mic2res0_dps_joint_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVmusic/p237_298_mic2res0_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/LP35/p237_298_mic2res0_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Speech 2</td>
    <td>
      <audio controls>
        <source src="./ModelTest/REF/p269_367_mic2res0_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/DEC/p269_367_mic2res0_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVspeech/p269_367_mic2res0_dps_speech_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVjoint/p269_367_mic2res0_dps_joint_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVmusic/p269_367_mic2res0_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/LP35/p269_367_mic2res0_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Speech 3</td>
    <td>
      <audio controls>
        <source src="./ModelTest/REF/p306_277_mic2res0_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/DEC/p306_277_mic2res0_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVspeech/p306_277_mic2res0_dps_speech_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVjoint/p306_277_mic2res0_dps_joint_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVmusic/p306_277_mic2res0_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/LP35/p306_277_mic2res0_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Piano 1</td>
    <td>
      <audio controls>
        <source src="./ModelTest/REF/ys250pr2232Lres6_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/DEC/ys250pr2232Lres6_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVspeech/ys250pr2232Lres6_dps_speech_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVjoint/ys250pr2232Lres6_dps_joint_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVmusic/ys250pr2232Lres6_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/LP35/ys250pr2232Lres6_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Piano 2</td>
    <td>
      <audio controls>
        <source src="./ModelTest/REF/yt974cv2625Lres29_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/DEC/yt974cv2625Lres29_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVspeech/yt974cv2625Lres29_dps_speech_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVjoint/yt974cv2625Lres29_dps_joint_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVmusic/yt974cv2625Lres29_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/LP35/yt974cv2625Lres29_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Piano 3</td>
    <td>
      <audio controls>
        <source src="./ModelTest/REF/zt739gs4926Lres89_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/DEC/zt739gs4926Lres89_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVspeech/zt739gs4926Lres89_dps_speech_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVjoint/zt739gs4926Lres89_dps_joint_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVmusic/zt739gs4926Lres89_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/LP35/zt739gs4926Lres89_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Critical 1</td>
    <td>
      <audio controls>
        <source src="./ModelTest/REF/01b_trumpet_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/DEC/01b_trumpet_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVspeech/01b_trumpet_L_dps_speech_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVjoint/01b_trumpet_L_dps_joint_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVmusic/01b_trumpet_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/LP35/01b_trumpet_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Critical 2</td>
    <td>
      <audio controls>
        <source src="./ModelTest/REF/04_choral_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/DEC/04_choral_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVspeech/04_choral_L_dps_speech_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVjoint/04_choral_L_dps_joint_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVmusic/04_choral_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/LP35/04_choral_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Critical 3</td>
    <td>
      <audio controls>
        <source src="./ModelTest/REF/27_castanets_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/DEC/27_castanets_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVspeech/27_castanets_L_dps_speech_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVjoint/27_castanets_L_dps_joint_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/INVmusic/27_castanets_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./ModelTest/LP35/27_castanets_L_lp35.wav">
      </audio>
    </td>
  </tr>

</table>
</html>

### Codec Test

This section contains the 10 items used in the second MUSHRA-style listening test.

<html>
<table>

  <tr>
    <th>Item</th>
    <th>REF</th>
    <th>DEC</th>
    <th>INVmusic</th>
    <th>AAC</th>
    <th>Opus</th>
    <th>LP35</th>
  </tr>

  <tr>
    <td>Item 1</td>
    <td>
      <audio controls>
        <source src="./CodecTest/REF/01b_trumpet_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/DEC/01b_trumpet_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/INVmusic/01b_trumpet_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/AAC/01b_trumpet_L_aac_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/Opus/01b_trumpet_L_opus_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/LP35/01b_trumpet_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Item 2</td>
    <td>
      <audio controls>
        <source src="./CodecTest/REF/04_choral_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/DEC/04_choral_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/INVmusic/04_choral_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/AAC/04_choral_L_aac_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/Opus/04_choral_L_opus_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/LP35/04_choral_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Item 3</td>
    <td>
      <audio controls>
        <source src="./CodecTest/REF/11_guitar_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/DEC/11_guitar_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/INVmusic/11_guitar_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/AAC/11_guitar_L_aac_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/Opus/11_guitar_L_opus_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/LP35/11_guitar_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Item 4</td>
    <td>
      <audio controls>
        <source src="./CodecTest/REF/13_glockenspiel_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/DEC/13_glockenspiel_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/INVmusic/13_glockenspiel_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/AAC/13_glockenspiel_L_aac_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/Opus/13_glockenspiel_L_opus_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/LP35/13_glockenspiel_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Item 5</td>
    <td>
      <audio controls>
        <source src="./CodecTest/REF/20c_accordion_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/DEC/20c_accordion_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/INVmusic/20c_accordion_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/AAC/20c_accordion_L_aac_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/Opus/20c_accordion_L_opus_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/LP35/20c_accordion_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Item 6</td>
    <td>
      <audio controls>
        <source src="./CodecTest/REF/21_violin_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/DEC/21_violin_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/INVmusic/21_violin_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/AAC/21_violin_L_aac_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/Opus/21_violin_L_opus_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/LP35/21_violin_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Item 7</td>
    <td>
      <audio controls>
        <source src="./CodecTest/REF/23_jazz_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/DEC/23_jazz_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/INVmusic/23_jazz_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/AAC/23_jazz_L_aac_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/Opus/23_jazz_L_opus_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/LP35/23_jazz_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Item 8</td>
    <td>
      <audio controls>
        <source src="./CodecTest/REF/27_castanets_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/DEC/27_castanets_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/INVmusic/27_castanets_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/AAC/27_castanets_L_aac_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/Opus/27_castanets_L_opus_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/LP35/27_castanets_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Item 9</td>
    <td>
      <audio controls>
        <source src="./CodecTest/REF/DE_Meridian_remix2_LD6_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/DEC/DE_Meridian_remix2_LD6_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/INVmusic/DE_Meridian_remix2_LD6_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/AAC/DE_Meridian_remix2_LD6_L_aac_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/Opus/DE_Meridian_remix2_LD6_L_opus_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/LP35/DE_Meridian_remix2_LD6_L_lp35.wav">
      </audio>
    </td>
  </tr>

  <tr>
    <td>Item 10</td>
    <td>
      <audio controls>
        <source src="./CodecTest/REF/DE_female_speech_music_2_LD9_L_ref.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/DEC/DE_female_speech_music_2_LD9_L_dec_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/INVmusic/DE_female_speech_music_2_LD9_L_dps_music_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/AAC/DE_female_speech_music_2_LD9_L_aac_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/Opus/DE_female_speech_music_2_LD9_L_opus_16kbps.wav">
      </audio>
    </td>
    <td>
      <audio controls>
        <source src="./CodecTest/LP35/DE_female_speech_music_2_LD9_L_lp35.wav">
      </audio>
    </td>
  </tr>

</table>
</html>

## References

<html>
<table>
  <tr>
    <td valign="top">[1]</td>
    <td valign="top">Junichi Yamagishi, Christophe Veaux, Kirsten MacDonald, et al., "CSTR VCTK Corpus: English multi-speaker corpus for CSTR voice cloning toolkit (version 0.92)," University of Edinburgh. The Centre for Speech Technology Research (CSTR), 2019.</td>
  </tr>
  <tr>
    <td valign="top">[2]</td>
    <td valign="top">Zhengshan Shi, Craig Sapp, Kumaran Arul, Jerry McBride, and Julius O Smith III, "SUPRA: Digitizing the Stanford University Piano Roll Archive," in ISMIR, 2019, pp. 517–523.</td>
  </tr>
  <tr>
    <td valign="top">[3]</td>
    <td valign="top">Matteo Torcoli, Chih-Wei Wu, Sascha Dick, Phillip A. Williams, Mhd Modar Halimeh, William Wolcott, Emanuël A. P. Habets, "ODAQ: Open Dataset of Audio Quality," in ICASSP 2024-2024 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP). IEEE, 2024, pp. 836–840.</td>
  </tr>
</table>
</html>

