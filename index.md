{:.no_toc}
* toc
{:toc}

# TransFace: Unit-Based Audio-Visual Speech Synthesizer for Talking Head Translation
Direct speech-to-speech translation achieves high-quality results through the introduction of discrete units obtained from self-supervised learning. This approach circumvents delays and cascading errors associated with model cascading. However, talking head translation, converting audio-visual speech (i.e., talking head video) from one language into another, still confronts several challenges compared to audio speech: (1) Existing methods invariably rely on cascading, synthesizing via both audio and text, resulting in delays and cascading errors. (2) Talking head translation has a limited set of reference frames. If the generated translation exceeds the length of the original speech, the video sequence needs to be supplemented by repeating frames, leading to jarring video transitions. In this work, we propose a model for talking head translation, \textbf{TransFace}, which can directly translate audio-visual speech into audio-visual speech in other languages. It consists of a speech-to-unit translation model to convert audio speech into discrete units and a unit-based audio-visual speech synthesizer, Unit2Lip, to re-synthesize synchronized audio-visual speech from discrete units in parallel. Furthermore, we introduce a Bounded Duration Predictor, ensuring isometric talking head translation and preventing duplicate reference frames. Experiments demonstrate that our proposed Unit2Lip model significantly improves synchronization (1.601 and 0.982 on LSE-C for the original and generated audio speech, respectively) and boosts inference speed by a factor of $\times$4.35 on LRS2. Additionally, TransFace achieves impressive BLEU scores of 61.93 and 47.55 for Es-En and Fr-En on LRS3-T and 100\% isochronous translations.
# Unit2Lip (Unit-Based Audio-Visual Resynthesis)

## English (training with 29h English corpus)
 
<table>
    <thead>
        <tr>
            <th style="text-align: center">Audio(ori)+Video(ori)</th>
            <th style="text-align: center">Audio(ori)+Video(gen)</th>
            <th style="text-align: center">Audio(gen)+Video(ori)</th>
            <th style="text-align: center">Audio(gen)+Video(gen)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/0_Ao_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/0_Ao_Vg.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/0_Ag_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/0_Ag_Vg.mp4"></video></td>
        </tr>
        <tr>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/1_Ao_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/1_Ao_Vg.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/1_Ag_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/1_Ag_Vg.mp4"></video></td>
        </tr>
        <tr>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/2_Ao_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/2_Ao_Vg.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/2_Ag_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/en/2_Ag_Vg.mp4"></video></td>
        </tr>
    </tbody>
</table>

## Spanish (training with 29h English corpus)

<table>
    <thead>
        <tr>
            <th style="text-align: center">Audio(ori)+Video(ori)</th>
            <th style="text-align: center">Audio(ori)+Video(gen)</th>
            <th style="text-align: center">Audio(gen)+Video(ori)</th>
            <th style="text-align: center">Audio(gen)+Video(gen)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/0_Ao_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/0_Ao_Vg.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/0_Ag_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/0_Ag_Vg.mp4"></video></td>
        </tr>
        <tr>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/1_Ao_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/1_Ao_Vg.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/1_Ag_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/1_Ag_Vg.mp4"></video></td>
        </tr>
        <tr>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/2_Ao_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/2_Ao_Vg.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/2_Ag_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/es/2_Ag_Vg.mp4"></video></td>
        </tr>
    </tbody>
</table>

## French (training with 29h English corpus)

<table>
    <thead>
        <tr>
            <th style="text-align: center">Audio(ori)+Video(ori)</th>
            <th style="text-align: center">Audio(ori)+Video(gen)</th>
            <th style="text-align: center">Audio(gen)+Video(ori)</th>
            <th style="text-align: center">Audio(gen)+Video(gen)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/0_Ao_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/0_Ao_Vg.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/0_Ag_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/0_Ag_Vg.mp4"></video></td>
        </tr>
        <tr>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/1_Ao_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/1_Ao_Vg.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/1_Ag_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/1_Ag_Vg.mp4"></video></td>
        </tr>
        <tr>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/2_Ao_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/2_Ao_Vg.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/2_Ag_Vo.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/unit2lip/fr/2_Ag_Vg.mp4"></video></td>
        </tr>
    </tbody>
</table>

# TransFace (Zero-Shot Speech(A)-To-Speech(AV) Translation)

## Es-En on LRS3-T

<table>
    <thead>
        <tr>
            <th style="text-align: center"></th>
            <th style="text-align: center">Source Speech(A)</th>
            <th style="text-align: center">Target Speech(AV)</th>
            <th style="text-align: center">AVSR+NMT+TTS+Wav2Lip</th>
            <th style="text-align: center">ST+TTS+Wav2Lip</th>
            <th style="text-align: center">S2ST+Wav2Lip</th>
            <th style="text-align: center">TransFace</th>
            <th style="text-align: center">TransFace+bounded</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th style="text-align: center">Sample1</th>
            <td style="text-align: center"><audio controls style="width: 200px;"><source src="case/S2ST/es-en/demo1/source.wav"></audio></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo1/target.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo1/NMT.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo1/ST.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo1/S2ST_wav2lip.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo1/full.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo1/full_bounded.mp4"></video></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th style="text-align: center">Reference/AVSR</th>
            <td>Así que el agua era algo que me asustaba para empezar</td>
            <td>So water was something that scared me to begin with</td>
            <td>So water was something that scared me in the beginning</td>
            <td>So water was something that scared me to begin</td>
            <td>so the water was something that was scaring me to start with</td>
            <td>so the water was something that was scaring me to start with</td>
            <td>so the water was something that was scaring me to start with</td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th style="text-align: center">Sample2</th>
            <td style="text-align: center"><audio controls style="width: 200px;"><source src="case/S2ST/es-en/demo2/source.wav"></audio></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo2/target.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo2/NMT.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo2/ST.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo2/S2ST_wav2lip.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo2/full.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/es-en/demo2/full_bounded.mp4"></video></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th style="text-align: center">Reference/AVSR</th>
            <td>No sabía que realmente tienes que tener control creativo</td>
            <td>I didn't know you actually have to have creative control</td>
            <td>I didn't know that you really have to have creative control</td>
            <td>I didn't know that you really have the creative control</td>
            <td>i didn't know that they had to have the creative control</td>
            <td>i didn't know that they had to have the creative control</td>
            <td>i didn't know that you really have to be creative control</td>
        </tr>
    </tbody>
</table>

## Fr-En on LRS3-T

<table>
    <thead>
        <tr>
            <th style="text-align: center"></th>
            <th style="text-align: center">Source Speech(A)</th>
            <th style="text-align: center">Target Speech(AV)</th>
            <th style="text-align: center">AVSR+NMT+TTS+Wav2Lip</th>
            <th style="text-align: center">ST+TTS+Wav2Lip</th>
            <th style="text-align: center">S2ST+Wav2Lip</th>
            <th style="text-align: center">TransFace</th>
            <th style="text-align: center">TransFace+bounded</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th style="text-align: center">Sample1</th>
            <td style="text-align: center"><audio controls style="width: 200px;"><source src="case/S2ST/fr-en/demo1/source.wav"></audio></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo1/target.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo1/NMT.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo1/ST.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo1/S2ST_wav2lip.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo1/full.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo1/full_bounded.mp4"></video></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th style="text-align: center">Reference/AVSR</th>
            <td>No fuimos considerados la cosa real</td>
            <td>we weren't considered the real thing</td>
            <td>We were not considered the real thing</td>
            <td>We were not considered the real ones</td>
            <td>we were not considered as the real thing</td>
            <td>we were not considered as the real thing</td>
            <td>we were not considered as the real thing</td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th style="text-align: center">Sample2</th>
            <td style="text-align: center"><audio controls style="width: 200px;"><source src="case/S2ST/fr-en/demo2/source.wav"></audio></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo2/target.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo2/NMT.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo2/ST.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo2/S2ST_wav2lip.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo2/full.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/fr-en/demo2/full_bounded.mp4"></video></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th style="text-align: center">Reference/AVSR</th>
            <td>Et tout cela est très important parce que la sécurité publique est pour moi la fonction la plus importante de</td>
            <td>and all of this matters greatly because public safety to me is the most important function of</td>
            <td>all this is very important because public safety is for me the most important function of </td>
            <td>all this is very important because public safety is for me the most important function</td>
            <td>and all this is very important because the public safety is for me the most important function</td>
            <td>and all this is very important because the public safety is for me the most important function of</td>
            <td>and all this is very important because public safety for me is the most important function of</td>
        </tr>
    </tbody>
</table>


## En-Es on LRS3-T
<table>
    <thead>
        <tr>
            <th style="text-align: center"></th>
            <th style="text-align: center">Source Speech(AV)</th>
            <th style="text-align: center">Target Speech(A)</th>
            <th style="text-align: center">TransFace</th>
            <th style="text-align: center">TransFace+bounded</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th style="text-align: center">Sample1</th>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-es/demo1/source.mp4"></video></td>
            <td style="text-align: center"><audio controls style="width: 200px;"><source src="case/S2ST/en-es/demo1/target.wav"></audio></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-es/demo1/s2st.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-es/demo1/s2st_bounded.mp4"></video></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th style="text-align: center">Sample1</th>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-es/demo2/source.mp4"></video></td>
            <td style="text-align: center"><audio controls style="width: 200px;"><source src="case/S2ST/en-es/demo2/target.wav"></audio></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-es/demo2/s2st.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-es/demo2/s2st_bounded.mp4"></video></td>
        </tr>
    </tbody>
</table>



## En-Fr on LRS3-T
<table>
    <thead>
        <tr>
            <th style="text-align: center"></th>
            <th style="text-align: center">Source Speech(AV)</th>
            <th style="text-align: center">Target Speech(A)</th>
            <th style="text-align: center">TransFace</th>
            <th style="text-align: center">TransFace+bounded</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th style="text-align: center">Sample1</th>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-fr/demo1/source.mp4"></video></td>
            <td style="text-align: center"><audio controls style="width: 200px;"><source src="case/S2ST/en-fr/demo1/target.wav"></audio></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-fr/demo1/s2st.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-fr/demo1/s2st_bounded.mp4"></video></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th style="text-align: center">Sample1</th>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-fr/demo2/source.mp4"></video></td>
            <td style="text-align: center"><audio controls style="width: 200px;"><source src="case/S2ST/en-fr/demo2/target.wav"></audio></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-fr/demo2/s2st.mp4"></video></td>
            <td style="text-align: center"><video controls style="width: 200px;"><source src="case/S2ST/en-fr/demo2/s2st_bounded.mp4"></video></td>
        </tr>
    </tbody>
</table>