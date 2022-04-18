## Evaluating The Quality of Timbre Transfer when Varying The Quantity of Instruments

In this project, we evaluated the performance of timbre transfer by using wavenet auto-encoders and varying the number of instruments in the target domains. We created the BaHaMe dataset a dataset of audio files with a varying quantity of instruments to perform such an evaluation.

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

To evaluate the performance of timbre transfer, different decoders were trained - each made to output audio with either one, two, or three instruments. The corresponding outputs were then compared to each other by participants in a user study to evaluate the quality of the timbre transfer. Details of training are described in our paper. 


### Example

Here you can hear an example of what is illutrated by our hypothesis. Below are two samples of the transfer, one with one instrument and another with 3 instruments. 

Example 1: 

Here is an audio file from the BaHaMe dataset. It is from the second arrangement and consists just of a flute recording:

<iframe width="100%" height="300" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1114668547&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/pjcasas29" title="Pedro C" target="_blank" style="color: #cccccc; text-decoration: none;">Pedro C</a> · <a href="https://soundcloud.com/pjcasas29/10-dataset-d2-high" title="10 Dataset D2 - High" target="_blank" style="color: #cccccc; text-decoration: none;">10 Dataset D2 - High</a></div>

When using our method to translate the audio with the same melody as above of a harp back to the timbre of a flute, this is the result:

<iframe width="100%" height="300" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1114668187&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/pjcasas29" title="Pedro C" target="_blank" style="color: #cccccc; text-decoration: none;">Pedro C</a> · <a href="https://soundcloud.com/pjcasas29/10dataset-d3-high-1" title="10 Dataset 3 to 2 - High" target="_blank" style="color: #cccccc; text-decoration: none;">10 Dataset 3 to 2 - High</a></div>
 
Example 2: 

Here is another sample from the BaHaMe dataset, again from the second arrangement. It consists of all 3 instruments:

<iframe width="100%" height="300" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1112799637&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/pjcasas29" title="Pedro C" target="_blank" style="color: #cccccc; text-decoration: none;">Pedro C</a> · <a href="https://soundcloud.com/pjcasas29/300-dataset-2-alll" title="300 Dataset 2 - All" target="_blank" style="color: #cccccc; text-decoration: none;">300 Dataset 2 - All</a></div>

This next file is a tranformation of this audio file with the target arrangement as the 3rd arrangement. As you can hear there are some artifacts and errors in this transfer:

<iframe width="100%" height="300" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1112800363&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/pjcasas29" title="Pedro C" target="_blank" style="color: #cccccc; text-decoration: none;">Pedro C</a> · <a href="https://soundcloud.com/pjcasas29/300dataset-2-to-3all" title="300Dataset 2 to 3 - All" target="_blank" style="color: #cccccc; text-decoration: none;">300Dataset 2 to 3 - All</a></div>

In this example, one can hear how when tranfer is performed on a domain with more instruments, the quality of the transfer suffers when compared to an example with fewer instruments.
