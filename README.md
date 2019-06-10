# EarningsCall_Dataset

This is the segmented earnings conference call dataset of S&P 500 companies in 2017. 

Since the dataset includes text transcripts and corresponding audio recordings, it is too large to put on GitHub. We put a few examples in this repository, and upload our complete dataset on Google Drive, please check the [link](https://drive.google.com/file/d/15wtWZvSJicF_Ur2V45lCyCjNJQ7QfXth/view?usp=sharing) to download the complete dataset.

# Citation

If you use this data in your research please cite the following paper:

Qin, Yu., & Yang, Yi. (2019). What You Say and How You Say It Matters: Predicting Financial Risk Using Verbal and Vocal Cues. Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics.

    @InProceedings{P19-xxxx,
      author =  "Qin, Yu and Yang, Yi",
      title =   "What You Say and How You Say It Matters: Predicting Financial Risk Using Verbal and Vocal Cues",
      booktitle =   "Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
      year =  "2019",
      publisher =   "Association for Computational Linguistics",
      pages =   "xx--xx",
      location =  "Florence , Italy",
      url =   ""
    }

# Annotation Format

Each folder in our dataset represents an earnings conference call; the folders are named as "CompanyName_Date".

In each folder, we put the processed text transcript and segmented audio recordings. As we described in our paper, we only select the most spoken executive (usually the CEO) to avoid interference. 

In the processed text transcript, each line is a sentence of CEO, ordered by time. 

For the segmented audio recordings, they are named as "Speaker_Paragraph_Sentence". Since in our Iterative Forced Alignment (IFA) processing, the whole audio recording is firstly segmented on paragraph level, then the sentence level. The order of segmented audio recordings as from "Speaker_1_1", "Speaker_1_2", "Speaker_1_m<sub>1</sub>" to "Speaker_n_m<sub>n</sub>", where m<sub>x</sub> represents the number of sentences of paragraph x, and n represents the number of paragraphs.

Each line in the text file corresponds to an audio file. And the total number of lines in a text file is the same as the total number of audio files for the same earnings conference call.
    
# Contact
If you have any questions regarding the repo, please contact Yu Qin (<qinyu.gemini@gmail.com>) or create an issue.
