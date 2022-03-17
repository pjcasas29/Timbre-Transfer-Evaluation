## Evaluating The Quality of Timbre Transfer when Varying The Quantity of Instruments

In this paper, we evaluated the performance of timbre transfer by using wavenet auto-encoders and varying the number of instruments in the target domains. We created the BaHaMe dataset a dataset of audio files with a varying quantity of instruments to perform such an evaluation. This dataset can be found here (to be linked).

Using a pre-trained universal encoder, we trained a number of decoders that generate audio which has undergone timbre transfer containing 1 to 3 instruments. These decoders can be found in this [github repository](https://github.com/pjcasas29/Timbre-Transfer-Evaluation/tree/main/Decoders). 

The quality of the transfer was evaluated with a user study in the areas of noise/artifacts, melody preservation, and expected timbre. The questionnaire can be found [here](https://www.jotform.com/form/211346363725050)

We found that when timbre transfer is performed on an audio dataset where the files contain multiple instruments, users report that the quality of the transfer is generally worse in these three areas, particularly in the area of melody preservation

### Dataset

The BaHaMe dataset consists of audio files in wav format and MIDI files, with the audio files having been generated from their respective MIDI files. It is a collection of songs gathered from the [BitMidi website](https://bitmidi.com/). The total length of the songs is approximately 150 minutes. Each song consists of a three part arrangement: a melodic part, a harmonic part which plays chords as accompaniment and a bass part. Four different arrangements are created from each MIDI file (A1 - A4). An arrangement is a selection of different instruments for each of the three parts namely melody, harmony and bass. The instruments for each arrangement are as follows:

| **Arrangement** |   **Melody**  | **Harmony** |   **Bass**   |
|:---------------:|:-------------:|:-----------:|:------------:|
|        1        | Ambient Synth | Dirty Synth | Upright Bass |
|        2        | Flute         | Piano       | Synth Bass   |
|        3        | Harp          | Pad         | Woofer Bass  |
|        4        | Xylophone     | Organ       | Bass Pad     |

### Decoders

To evaluate the performance of timbre transfer, different decoders were trained - each made to output audio with either one, two, or three instruments. The corresponding outputs were then compared to each other by participants in a user study to evaluate the quality of the timbre transfer. Details of training are described in the paper. 



### Samples

Here you can hear some of the samples that were produced by some of these decoders using the BaHaMe dataset. 

<iframe width="100%" height="300" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1114668547&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/pjcasas29" title="Pedro C" target="_blank" style="color: #cccccc; text-decoration: none;">Pedro C</a> · <a href="https://soundcloud.com/pjcasas29/10-dataset-d2-high" title="10 Dataset D2 - High" target="_blank" style="color: #cccccc; text-decoration: none;">10 Dataset D2 - High</a></div>
 
Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```
