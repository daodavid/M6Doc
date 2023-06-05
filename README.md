# M<sup>6</sup>Doc_Dataset_Release
The M<sup>6</sup>Doc dataset for the research of document layout analysis in Modern Document is now released by the Deep Learning and Visual Computing Lab of South China University of Technology. 

Note: The M<sup>6</sup>Doc dataset can only be used for non-commercial research purposes. For scholars or organizations who want to use the M<sup>6</sup>Doc database, please first fill in this [Application Form](Application_Form/Application-Form-for-Using-M6Doc.docx) and send it via email to us ([lianwen.jin@gmail.com](mailto:lianwen.jin@gmail.com) or [eelwjin@scut.edu.cn](mailto:eelwjin@scut.edu.cn)). When submitting the application form to us, please list or attach 1-2 of your publications in the recent 6 years to indicate that you (or your team) do research in the related research fields of OCR, handwriting analysis and recognition, document image processing, or visual information extraction. At present, this dataset is only freely available to scholars in the above-mentioned fields. We will give you the download link and decompression password after your letter has been received and approved.

## License
The M<sup>6</sup>Doc dataset should be used and distributed under the [Creative Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) License](https://creativecommons.org/licenses/by-nc-nd/4.0/) for non-commercial research purposes.

## M<sup>6</sup>Doc Dataset
The M<sup>6</sup>Doc dataset contains a total of 9,080 modern document images, which are categorized into seven subsets, *i.e.*, scientific article (11\%), textbook (23\%), test paper (22\%), magazine (22\%), newspaper (11\%), note (5.5\%), and book (5.5\%) according to their content and layouts. It contains three formats: PDF (64\%), photographed documents (5\%), and scanned documents (31\%). The dataset includes a total of 237,116 annotated instances. Figure 1 shows annotation samples of M<sup>6</sup>Doc. There are a total of 74 annotation categories in our dataset.

![](img/m6doc_example.png)
Figure 1. Example annotations of the M<sup>6</sup>Doc. Zoom in for better view.

## Dataset Source
The M<sup>6</sup>Doc datasets were collected from various sources, including [arXiv](https://arxiv.org/), the official website of the [Chinese People's Daily](http://paper.people.com.cn/), and [VKontakte](https://vk.com/). The source and composition of different subsets are shown below.

  * The scientific article subset includes articles obtained by searching with the keywords \"Optical Character Recognition\" and \"Document Layout Analysis\" on arXiv. PDF files were then downloaded and converted to images.
  * The textbook subset contains 2,080 scanned document images from textbooks for three grades (elementary, middle, and high school) and nine subjects (Chinese, Math, English, Physics, Chemistry, Biology, History, Geography, and Politics).
  * The test paper subset consists of 2,000 examination papers covering the same nine subjects as the textbook subset.
  * The magazine subset includes 1,000 Chinese and English magazines in PDF format, respectively. The Chinese magazines were sourced from five publishers: Global Science, The Mystery, Youth Digest, China National Geographic, and The Reader. The English magazines were sourced from five American publishers: The New Yorker, New Scientist, Scientific American, The Economist, and Time USA.
  * The newspaper subset contains 500 PDF document images from the Chinese People's Daily and the Wall Street Journal.
  * The note subset consists of students' handwritten notes in nine subjects, including 500 scanned pages.
  * The book subset contains 500 photographed images, which were acquired from 50 books with 10 pages each. Each book has a distinct layout, resulting in considerable diversity in this subset.
 
For a fair evaluation, we divided the dataset into training, validation, and test sets in a ratio of 6:1:3. We also ensured that the different labels were in equal proportions in the three sets. Table \ref{tab2} summarizes the overall frequency and distribution of labels in different sets.

Table 2. M<sup>6</sup>Doc dataset overview.
![](img/m6doc_dataset_review.png)

## Data Annotation
### Label definition
To ensure that the definition of document layout elements is reasonable and traceable, we reviewed relevant information, such as layout knowledge and layout design. We also used knowledge from the book \"Page Design: New Layout \& Editorial Design(2019)\" and referred to YouTube video explanations regarding [magazine](https://www.youtube.com/watch?v=7sSJtScnsjE) and [newspaper](https://www.youtube.com/watch?v=LcsOuGcaqZs) layouts. In most cases, we followed the [Wikipedia](https://www.wikipedia.org) definition. Consequently, we defined 74 detailed document annotation labels. The key factors in selecting these annotation labels include (1) the commonality of annotation labels between different document types, (2) the specificity of labels between different document types, (3) the frequency of labels, and (4) the recognition of independent pages. We first unified the labels between different documents to the maximum extent and then defined the labels for certain document types for differentials. Commonality and specificity ensure that the defined labels can adapt to multiple document types, which implies that a more detailed logical layout analysis for a certain type of document can be performed. It differs from how labels are defined in DocBank, PubLayNet, and DocLayNet, which all ignore defining specific labels for different document types.

