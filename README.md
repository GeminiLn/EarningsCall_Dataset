# What You Say and How You Say It Matters: Predicting Stock Volatility Using Verbal and Vocal Cues

by Yu Qin and Yi Yang, ACL 2019.

## Abstract

Predicting financial risk is an essential task in financial market. Prior research has shown that textual information in a firm's financial statement can be used to predict its stock's risk level. Nowadays, firm CEOs communicate information not only verbally through press releases and financial reports, but also nonverbally through investor meetings and earnings conference calls. There are anecdotal evidences that CEO's vocal features, such as emotions and voice tones, can reveal the firm's performance. However, how vocal features can be used to predict risk levels, and to what extent, is still unknown. To fill the gap, we obtain earnings call audio recordings and textual transcripts for S\&P 500 companies in recent years. We propose a multimodal deep regression model (MDRM) that jointly model CEO's verbal (from text) and vocal (from audio) information in a conference call. Empirical results show that our model that jointly considers verbal and vocal features achieves significant and substantial prediction error reduction. We also discuss several interesting findings and the implications to financial markets. The processed earnings conference calls data (text and audio) are released for readers who are interested in reproducing the results or designing trading strategy.

## About This Repo

This is the segmented earnings conference call dataset of S&P 500 companies in 2017. 

Since the dataset includes text transcripts and corresponding audio recordings, it is too large to put on GitHub. We put a few examples in this repository, and upload our complete dataset on Google Drive, please check the [link](https://drive.google.com/drive/folders/1BKCANORbcmUJKkOkBOghw6uNHPqS_az1?usp=sharing) to download the complete dataset.

The whole dataset is split to five files, please download all the files and unzip them. 

To unzip the dataset under Linux environment, please first use `zip -s0 ACL19_Release.zip --out ACL19_Release_All.zip` to merge the files.
Then use `unzip -q ACL19_Release_all.zip` to unzip the dataset.

## Citation

If you use this data in your research, please cite the following paper:

Qin, Yu., & Yang, Yi. (2019). What You Say and How You Say It Matters: Predicting Stock Volatility Using Verbal and Vocal Cues. Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics.

    @inproceedings{qin-yang-2019-say,
    title = "What You Say and How You Say It Matters: Predicting Stock Volatility Using Verbal and Vocal Cues",
    author = "Qin, Yu  and
      Yang, Yi",
    booktitle = "Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics",
    month = jul,
    year = "2019",
    address = "Florence, Italy",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/P19-1038",
    pages = "390--401",}

## Annotation Format

Each folder in our dataset represents an earnings conference call; the folders are named as "CompanyName_Date".

In each folder, we put the processed text transcript and segmented audio recordings. As we described in our paper, we only select the most spoken executive (usually the CEO) to avoid interference. 

In the processed text transcript, each line is a sentence of CEO, ordered by time. 

For the segmented audio recordings, they are named as "Speaker_Paragraph_Sentence". Since in our Iterative Forced Alignment (IFA) processing, the whole audio recording is firstly segmented on paragraph level, then the sentence level. The order of segmented audio recordings as from "Speaker_1_1", "Speaker_1_2", "Speaker_1_m<sub>1</sub>" to "Speaker_n_m<sub>n</sub>", where m<sub>x</sub> represents the number of sentences of paragraph x, and n represents the number of paragraphs.

Each line in the text file corresponds to an audio file. And the total number of lines in a text file is the same as the total number of audio files for the same earnings conference call.
    
## Contact
If you have any questions regarding the repo, please contact Yu Qin (<qinyu.gemini@gmail.com>) or create an issue.
