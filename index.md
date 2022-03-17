## Evaluating The Quality of Timbre Transfer when Varying The Quantity of Instruments

In this paper, we evaluated the performance of timbre transfer by using wavenet auto-encoders and varying the number of instruments in the target domains. We created the BaHaMe dataset a dataset of audio files with a varying quantity of instruments to perform such an evaluation. This dataset can be found here.

Using a pre-trained universal encoder, we trained a number of decoders that generate audio which has undergone timbre transfer containing 1 to 3 instruments. These decoders can be found in this github repository. 

The quality of the transfer was evaluated with a user study in the areas of noise/artifacts, melody preservation, and expected timbre. We found that when timbre transfer is performed on an audio dataset where the files contain multiple instruments, users report that the quality of the transfer is generally worse in these three areas, particularly in the area of melody preservation

### Markdown
 
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

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/pjcasas29/Timbre-Transfer-Evaluation/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
